# 서비스 노출과 인그레스 (Service Exposure and Ingress)

## 정의

쿠버네티스에서 애플리케이션을 네트워크로 노출할 때, `Service`를 기본 로드밸런싱 단위로 사용하고 HTTP 계층 제어는 `Ingress`로 분리하는 설계 원칙.

## 왜 중요한가?

- 내부 통신과 외부 노출 경계를 분리해 보안/운영 제어가 쉬워진다.
- 트래픽 라우팅, TLS, 도메인 정책을 앱과 분리해 관리할 수 있다.
- 네트워크 변경이 생겨도 앱 배포를 최소화할 수 있다.

## 책 내용 핵심 정리

- 디플로이먼트는 보통 서비스로 노출되며, 서비스가 사실상 TCP 로드밸런서 역할을 한다.
- 서비스는 기본적으로 클러스터 내부 노출이지만 외부 노출도 가능하다.
- HTTP 애플리케이션은 Ingress Controller를 사용해 라우팅/SSL 기능을 추가하는 것이 좋다.

## 실무 포인트

### 1. L4와 L7 역할 분리
- Service는 포트/엔드포인트 매핑(L4)에 집중한다.
- Ingress는 호스트/경로 라우팅, TLS 종료 등 L7 정책에 집중한다.

### 2. 노출 범위 최소화
- 기본은 `ClusterIP`로 두고, 외부 공개가 필요한 경우만 Ingress/LoadBalancer를 연다.
- 관리 포트/내부 API는 외부 노출 대상에서 분리한다.

### 3. 가용성/운영성 설계
- readiness/liveness probe와 Ingress health check 기준을 맞춘다.
- 타임아웃, 재시도, 최대 요청 크기 같은 엣지 정책을 표준화한다.

## 바로 적용 가능한 체크리스트

- [ ] 서비스 노출 정책(내부/외부) 기준 문서를 갖췄다.
- [ ] HTTP 트래픽은 Ingress를 통해 라우팅한다.
- [ ] TLS 인증서 갱신 자동화를 구성했다.
- [ ] Ingress 공통 정책(타임아웃, 보안 헤더)을 템플릿화했다.

## 실무 한 줄

Service는 연결점, Ingress는 정책점이다. 둘을 분리해야 네트워크 운영이 단순해진다.

## 관련 개념

- ClusterIP / NodePort / LoadBalancer
- Ingress Controller
- TLS Termination
- NetworkPolicy

## 출처

- 쿠버네티스 창시자에게 배우는 모범 사례 2판

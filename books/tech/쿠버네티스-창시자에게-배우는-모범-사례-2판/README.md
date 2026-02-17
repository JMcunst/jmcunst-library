# 쿠버네티스 창시자에게 배우는 모범 사례 2판

## Info

| 항목 | 내용 |
|------|------|
| 원제 | Kubernetes Best Practices, 2nd Edition |
| 원서 저자 | Brendan Burns, Eddie Villalba, Dave Strebel, Lachlan Evenson |
| 저자 | 브렌던 번스, 에디 비얄바, 데이브 스트레벨, 라클런 이븐슨 |
| 역자 | 이일웅 |
| 펴낸이 | 전태호 |
| 출판사 | 한빛미디어 |
| 읽은 기간 | 2026-02-16 ~ |
| 평점 | ⭐⭐⭐⭐⭐ (5/5) |

## 한 줄 요약

>

## 이 책을 읽게 된 계기

## 책 요약

### Part 1:

### Part 2:

### Part 3:

## 핵심 키워드

- 이미지 공급망 보안 (Software Supply Chain Security)
- 베이스 이미지 신뢰성
- 이미지 다이제스트 고정 (Digest Pinning)
- SBOM / 이미지 서명 / 취약점 스캔
- 시크릿 인증 관리
- 환경 파라미터화 (Parameterization)
- 퍼시스턴트볼륨 (Persistent Volume)
- 파일 스토리지 vs 블록 스토리지
- 스테이트풀 서비스 운영 전략
- 읽기/쓰기 분리 (Read/Write Split)
- Redis Failover
- 디플로이먼트 중심 서비스 배포
- 서비스 노출 전략 (Service/Ingress)
- 구성 파라미터화 (Helm Values)
- 컴포넌트 상호작용 이해
- 기본 컴포넌트 활용
- 버전 관리
- 코드 리뷰
- 지속적 배포 (Continuous Delivery)

## 인상 깊었던 내용

## 느낀 점

## 인용구

>
> — p.XX

## 추천 대상

-

## 배운 개념들

| # | 개념 | 설명 | 링크 |
|---|------|------|------|
| 0001 | 이미지 관리 모범 사례 | 공급망 공격을 줄이기 위한 베이스 이미지 선택, 빌드 검증, 배포 게이트 | [concepts/0001-image-management-best-practices.md](concepts/0001-image-management-best-practices.md) |
| 0002 | 시크릿 인증 관리 | 시크릿을 코드/이미지에 바인딩하지 않고 환경별로 안전하게 주입하는 원칙 | [concepts/0002-secret-credential-management.md](concepts/0002-secret-credential-management.md) |
| 0003 | 스테이트풀 스토리지 선택 | 파일/블록 스토리지 특성과 상태 관리 복잡도를 고려한 운영 전략 | [concepts/0003-stateful-storage-selection.md](concepts/0003-stateful-storage-selection.md) |
| 0004 | 레디스 읽기/쓰기 분리와 Failover | Service와 Headless Service를 이용한 트래픽 분리와 장애 전환 전략 | [concepts/0004-redis-read-write-split-and-failover.md](concepts/0004-redis-read-write-split-and-failover.md) |
| 0005 | 디플로이먼트 중심 배포 | 대부분의 서비스 워크로드를 Deployment로 표준화해 복제/롤링업데이트를 안정적으로 운영 | [concepts/0005-deployment-for-services.md](concepts/0005-deployment-for-services.md) |
| 0006 | 서비스 노출과 인그레스 | Service로 내부/외부 노출을 제어하고 HTTP 트래픽은 Ingress로 라우팅/TLS를 관리 | [concepts/0006-service-exposure-and-ingress.md](concepts/0006-service-exposure-and-ingress.md) |
| 0007 | 구성 파라미터화와 Helm | 환경별 설정값 분리로 동일 매니페스트 재사용성을 높이고 배포 일관성을 확보 | [concepts/0007-parameterization-and-helm.md](concepts/0007-parameterization-and-helm.md) |
| 0008 | 컴포넌트 상호작용 | Pod, Service, Ingress, Storage, Secret이 어떻게 맞물려 서비스가 동작하는지 구조적으로 이해 | [concepts/0008-kubernetes-component-interactions.md](concepts/0008-kubernetes-component-interactions.md) |
| 0009 | 기본 컴포넌트 활용 | Kubernetes 기본 리소스의 역할 경계를 지키며 조합하는 실전 사용 원칙 | [concepts/0009-core-component-usage-basics.md](concepts/0009-core-component-usage-basics.md) |
| 0010 | 버전 관리 실천 | 변경 이력, 태깅, 브랜치 전략으로 릴리스 추적성과 복구 가능성 확보 | [concepts/0010-version-control-practice.md](concepts/0010-version-control-practice.md) |
| 0011 | 코드 리뷰 실천 | 변경 리스크를 사전 차단하고 팀 지식 공유를 강화하는 리뷰 운영 방식 | [concepts/0011-code-review-practice.md](concepts/0011-code-review-practice.md) |
| 0012 | 지속적 배포 실천 | 자동화된 검증과 단계적 릴리스로 배포 리드타임과 장애 복구 시간을 줄이는 방식 | [concepts/0012-continuous-delivery-practice.md](concepts/0012-continuous-delivery-practice.md) |

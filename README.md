# mungta-argocd-helm
### Chart 구조

| 이름         | 설명                                                     |
| ------------ | -------------------------------------------------------- |
| Chart.yaml   | Chart에 대한 이름, 버전, 설명 등이 정의된 파일           |
| values.yaml  | Chart 설치시 사용할 환경변수를 정의한 파일               |
| templates/   | 설치할 resource 들의 기본 틀을 정의한 manifest yaml 파일 |
| _helpers.tpl | template manifest 파일들에서 공유하는 변수 정의          |

### values.yaml에 정의한 환경변수 사용

- ``replicaCount: 1`` 로 선언했으면 ``{{ .values.replicaCount }}`` 형식으로 사용하시면 됩니다.

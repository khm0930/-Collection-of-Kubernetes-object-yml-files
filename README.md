# Kubernetes YAML Template Repository

## Overview

이 리포지토리는 Kubernetes 리소스들을 정의한 YAML 템플릿 파일들을 포함하고 있습니다. 각 파일은 Kubernetes 클러스터에서 특정 리소스를 생성하거나 관리하는 데 사용됩니다. 이 템플릿들을 통해 다양한 Kubernetes 오브젝트를 쉽게 배포하고 관리할 수 있습니다.

## File Descriptions

### 1. `namespace.yml`
- **Purpose**: 새로운 네임스페이스를 생성합니다.
- **Details**: 클러스터 내에서 리소스들을 논리적으로 분리하여 관리하기 위한 네임스페이스를 정의합니다.

### 2. `Deployment.yml`
- **Purpose**: 애플리케이션 배포를 관리하는 디플로이먼트를 생성합니다.
- **Details**: 특정 애플리케이션의 컨테이너 이미지를 정의하고, 원하는 파드 수와 스케일링 전략을 설정합니다.

### 3. `Service.yml`
- **Purpose**: 파드 간의 네트워크 통신을 관리하는 서비스를 생성합니다.
- **Details**: 클러스터 내에서 파드에 접근할 수 있도록 로드밸런싱 및 서비스 디스커버리를 제공합니다.

### 4. `Configmap.yml`, `Secret.yml`
- **Purpose**: 환경 설정 및 민감한 정보를 관리합니다.
- **Details**: 
  - `Configmap.yml`: 애플리케이션이 필요로 하는 환경 설정을 키-값 쌍으로 저장합니다.
  - `Secret.yml`: 비밀번호, 토큰 등 민감한 정보를 안전하게 저장하고 관리합니다.

### 5. `PVC.yml`, `PV.yml`
- **Purpose**: 스토리지 리소스를 관리합니다.
- **Details**: 
  - `PV.yml`: 클러스터 내에서 사용할 수 있는 물리적 스토리지를 정의합니다.
  - `PVC.yml`: 파드에서 사용할 스토리지를 요청하고 바인딩합니다.

### 6. `HPA.yml`
- **Purpose**: Horizontal Pod Autoscaler를 생성하여 파드의 자동 스케일링을 관리합니다.
- **Details**: CPU 또는 메모리 사용량에 따라 파드의 수를 자동으로 조정하는 설정을 정의합니다.

## Usage

각 YAML 파일은 `kubectl` 명령어를 통해 Kubernetes 클러스터에 적용할 수 있습니다. 예를 들어, `Deployment.yml` 파일을 적용하려면 아래 명령어를 사용합니다:

```bash
kubectl apply -f Deployment.yml

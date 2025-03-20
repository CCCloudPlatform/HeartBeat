# Grafana & Prometheus on Docker

도커 컴포즈를 활용하여 그라파나와 프로메테우스, 프로메테우스 노드 exporter를 실행할 수 있습니다.

여러 사용자가 동일한 환경에서 테스트할 수 있도록 구성하였고, Fast Run 가이드입니다.

---

### 버전 관리

```
HeartBeat/
├── docker-compose.yml
├── .gitignore  # Prometheus 데이터 제외 설정
├── grafana/
│   ├── dashboards/  # JSON 대시보드 파일들
│   │   ├── dashboard-01.json
│   │   ├── dashboard-02.json
│   ├── provisioning/  # 대시보드 및 데이터 소스 프로비저닝
│   |   ├── dashboards/
|   │   │   ├── dashboard.yaml
│   |   ├── datasources/
|   │   │   ├── datasource.yaml
│   ├── volume/  # db등 볼륨으로 충돌 방지를 위해 ignore
├── prometheus/
│   ├── config  # Prometheus 설정 파일
│   |   ├── prometheus.yml  # scrap target과 같은 설정들
│   |   ├── rule.yml  
│   ├── volume  # Prometheus 볼륨
```
---

### 실행 방법

```sh
docker compose up setup
docker compose up -d
```
<img width="434" alt="image" src="https://github.com/user-attachments/assets/32ee3545-476f-4e81-a1b8-034bacd4944e" />

---

### Dashboard 확인

<img width="1661" alt="image" src="https://github.com/user-attachments/assets/3f741e13-2436-4631-bde0-ef5f0fb83c7b" />

---

### 대시보드 파일 export
대시보드 우측 상단에 Export를 누르고 해당 json 파일을 복사하여 .json 파일 업로드
<img width="820" alt="image" src="https://github.com/user-attachments/assets/966cea90-ab0c-4aed-b88b-fb3894d830cf" />



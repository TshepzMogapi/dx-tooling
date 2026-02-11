This repository contains a set of tools and configurations designed to mock or emulate specific production services for local testing and debugging. 

By mimicking the behavior of real cloud infrastructure (AWS, Azure, GCP, etc.) on your local machine, it aims to significantly speed up the "Code → Build → Test" loop.

**⚠️ Important Distinction:**
- While these tools provide high-fidelity API emulation for functional testing, they are not exact replicas of production infrastructure. They are designed to verify application logic, not infrastructure hardness.
- This environment is NOT a substitute for:
    - Load & Performance Testing: Emulators running on a laptop cannot simulate cloud-scale throughput or latency.
    - Security & IAM Audits: Authentication is often simplified or bypassed locally; "Access Granted" here does not guarantee correct IAM policies in the cloud.
    - Production Parity: Some advanced cloud features may be partially implemented or missing entirely.



**Secrets & Environment**
copy env.example -> .env

docker compose --profile "*" down -v --remove-orphans 

Fastest Nuclear Fix

docker compose down -v
docker system prune -f
docker compose build --no-cache
docker compose up -d

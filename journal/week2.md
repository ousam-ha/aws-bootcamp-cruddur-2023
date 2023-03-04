# Week 2 — Distributed Tracing

## Live Class

- Without export env variable : within the shell
- With export : accessible to sub shells

  ```bash
  export HONEYCOMB_API_KEY="nFobH8SePkV73lFambGa5G"
  gp env HONEYCOMB_API_KEY="nFobH8SePkV73lFambGa5G"

  export HONEYCOMB_SERVICE_NAME="cruddur"
  gp env HONEYCOMB_SERVICE_NAME="cruddur"

  ```

  - OTEL : Open Telemetry
  - Never use same docker file for prod and dev

### Xray

```bash
aws xray create-group \
   --group-name "Cruddur" \
   --filter-expression "service(\"backend-flask\")"
```

### Tracing

### Service Maps

## Observability vs Monitoring Explained in AWS

- Current State Of Logging

  1. On-Premise Logs
     - Infrastructure
     - Applications
     - Anti-Virus
     - Firewall
     - etc
  2. Cloud Logs
     - Infrastructure \*\*\*
     - Applications \*\*\*
     - Anti-Virus
     - Firewall
     - etc

- Why logging is shit ?

  - Logging is the act of recording information about an state/activity/object/action.
  - Time consuming
  - Tons of data with no context
  - Needle in the haystack to find things
  - Monoliths vs Services vs Microservices
  - Modern applications are distributed
  - Many more haystacks and many more needles
  - Increase alert fatigue for SOC teams & Application teams (SREs, DevOps)

- Why Observability ?

  - Observability of a system is the ability to observe the behavior/state of the system, and this is dictated by what the system exposes about itself.
  - Decreased alert fatigue for Security Operations Teams
  - Visibility of end2end of logs, metrics & tracing
  - Troubleshoot and resolve things quickly without costing too much money
  - Understand application health
  - Accelerate collaboration between teams
  - Reduce overall operational cost
  - Increase customer satisfaction

- Monitoring vs. Observability : The ability to observe the state of an application is vital to understanding the behavior of an entire system landscape. While monitoring informs you when something goes wrong and where it occurred, observability tells you why something failed.

- Observability has three pillars:

  1. Metrics
  2. Traces
  3. Logs

- AWS Observability Services
  - AWS CloudWatch Logs
  - AWS CloudWatch Metrics
  - AWS X Ray Traces
- Amazon Detective Services

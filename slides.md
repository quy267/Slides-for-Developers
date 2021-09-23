---
theme: default 
background: https://source.unsplash.com/collection/94734566/1920x1080
class: 'text-center'
---

# Scaling Up to 1 Million CCU

## Introduction

---

# What is CCU ?

<style>
h1 {
  text-align: center;
}
</style>

- CCU = Concurrent User
- Total connected users at the same
- CCU is not Request Per Seconds

---

# Agenda

<style>
h1 {
  text-align: center;
}
</style>

- A simple high load system
- Require to reaching a million users
- Monitoring & Logging
- Scenarios Implementation

---

# A simple high load system ?

<style>
h1 {
  text-align: center;
}
</style>

<img src="/simple_high_load_system.png" class="rounded" style="height:50vh;margin-left:20vh"/>

---

# Require to reaching a million users

<style>
h1 {
  text-align: center;
}
</style>

- Multi-AZ
- Elastic Load Balancing between tiers
- Auto Scaling
- Service oriented architecture (SOA)
- Serving content smartly (Amazon S3/CloudFront)
- Caching off DB
- Moving state off tiers that auto-scale

---

<style>
h1 {
  text-align: center;
}
</style>

<img src="/Million_user.png" class="rounded" style="height:50vh"/>

---

# SOA (Service oriented architecture)

<style>
h1 {
  text-align: center;
}
</style>

- Move services into their own tiers
    - Treat them separately
    - Scale them independently
- It offers flexibility and greater understanding of each component

<img src="/SOA.png" class="rounded" style="height:30vh"/>

---

# Database issues?

<style>
h1 {
  text-align: center;
}
</style>

### How can you solve?

- Federation – splitting into multiple DBs based on function
- Sharding – splitting one dataset up across multiple hosts
- Moving some functionality to other types of DBs (NoSQL, Graph)

---

# Database federation

<style>
h1 {
  text-align: center;
}
</style>

- Split up databases by function/purpose
- Harder to do cross-function queries
- Essentially delays sharding/NoSQL
- Won’t help with single huge functions/tables

<img src="/federation.png" class="rounded" style="height:65vh;margin-left:50vh;padding-bottom: 20vh"/>

---

# Monitoring & Logging

<style>
h1 {
  text-align: center;
}
</style>

### Hard to failure recover on distributed system

- Logging system: Elastic Search, Grafana
- Monitoring system: Grafana, Prometheus, AWS cloudwatch
- Distributed Tracing: Jeager, AWS X-RAY


---
title: "7 ways to deploy Node.js"
---

## 7 ways to deploy node.js app

[00:01:14](https://www.youtube.com/watch?v=uEVmD6n8Il0&t=74)

application:

- fast api
- websockets, live connection
- stateless

[00:01:43](https://www.youtube.com/watch?v=uEVmD6n8Il0&t=103)

1. build your own server
  - use your own hardware
  - you own the infrastructure
  - cost of maintenance, electricity, management
  - manual scaling

[00:02:55](https://www.youtube.com/watch?v=uEVmD6n8Il0&t=175)

2. the cloud
  - compute engine = virtual machine
  - low cost upfront
  - manual scaling

[00:04:17](https://www.youtube.com/watch?v=uEVmD6n8Il0&t=257)

3. platform as a service
  - you get node js environment
  - auto configuration (no manual installation of required software)
  - auto-scaling
  - no control over runtime, you get setup, you can't change it

[00:05:55](https://www.youtube.com/watch?v=uEVmD6n8Il0&t=355)

4. docker (container) environment
  - you don't manage whole vm, just containers
  - control over environment
  - auto-scale

[00:06:30](https://www.youtube.com/watch?v=uEVmD6n8Il0&t=390)

5. kubernetes
  - more configuraiton
  - more control over orchestration
  - might be expensive and complicated for small projects

[00:07:05](https://www.youtube.com/watch?v=uEVmD6n8Il0&t=425)

6. cloud functions
  - directly run code in the cloud
  - short lived servers, only when the code is running, not compatible with websockets
  - cold start - first execution slow

[00:08:30](https://www.youtube.com/watch?v=uEVmD6n8Il0&t=510)

7. cloud run
  - like serverless functions, but executes docker
  - can customize environment

[source](https://www.youtube.com/watch?v=uEVmD6n8Il0)

---
title: "Observability and Troubleshotting"
description: ""
date: 2025-01-07
cascade:
  showReadingTime: true
---

#### Notes from the book DevOps for the desperate by Bradley Smith

Observability: Any application should be observable. Know what it is doing internally by analyzing system outputs like:

- Metrics: Data over time. Application's health and performance
- Traces: Track request throw different services.
- Logs:}historical audit trail of events.

Monitoring
Entails recording anayzing and alerting on predefined metrics to understand the current state of a system.

An obeservable system should answer two main questions:
"What?" and "Why?"
"What?" talks about the symptom.
"Why?" asks for the reasons behind the symtom.


Prometheus, alertmanager and grafana
Prometheus
Is a metric collection application that queries metric data.

Alertmanager
Takes alerts from prometheus ad decides where to route them based on some configurable criteria.

Grafana
Provides an esasy to-use interface to create and view dashboards and graphs from the data prometheus provides.

Tips to troubleshooting a problem
- Start simple. Be methodical. The problem is usually human error.
- Build a mental model. Undestanding what the system's role  is and how it interacts with other systems will help you troubleshoot faster.
- Take time developing a theory. Its always worth checking to see if the breadcrumb trail leads any farther.
- Have consister tools across hosts.
- Keep a journal. Keep a high-level account of problems, symptoms, and fixes so you dont forget important details about an issue.
- Know when to ask for help. 



Linux commands that might help

uptime - display how long a host has been running  the number of logged-in-users, and the system load.

top - Information about the system and processes running on that host.


> tools to discover more about a process's interaction with the system.
> - vmstat
> - strace
> - lsof


free - Quick sanity check on system memory by displaying used and available memory at the time it is run. the -h and -m flags  show all output in human-readable format.

vmstat - useful information about processes, memoty, IO, disks, and CPU activity.

ps - If the memory usage is high on the host, you'll want to check all the running processes to find where the memory is being used.


 



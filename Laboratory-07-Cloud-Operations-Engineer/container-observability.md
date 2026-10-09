# Container Observability Report

## Application Logging

Command executed:

```bash
docker logs client-website
```

### HTTP 404 Error Log

```text
172.17.0.1 - - [09/Oct/2026:01:27:09 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
```

### Why Application Logs Matter

Application logs record requests and events that help engineers understand what happened when a problem occurred. They help identify failed requests, investigate errors, and troubleshoot application behavior.

## Real-Time Container Metrics

Command executed:

```bash
docker stats
```

* Container name: `client-website`
* CPU usage: **0.00%**
* Memory usage: **2.746 MiB**
* Memory limit: **1.859 GiB**
* Memory usage percentage: **0.14%**
* Network I/O: **3.96 kB / 5.42 kB**
* Block I/O: **0 B / 12.3 kB**
* PIDs: **2**

### Logs vs. Metrics

Logs describe individual events and requests, while metrics provide numerical measurements of resource usage and system performance over time.

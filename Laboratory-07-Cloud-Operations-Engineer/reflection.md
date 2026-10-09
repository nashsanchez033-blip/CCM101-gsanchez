# Mission Reflection

Checking the host server's resources is important even when containers appear to be running perfectly. A container depends on the host's CPU, memory, disk space, and network resources. If the host runs out of memory or storage, applications may become slow, stop responding, or fail unexpectedly. Monitoring the host helps cloud operations engineers identify potential problems before they affect users.

The `docker logs` command helps troubleshoot application problems by showing the events recorded by a container. If a user cannot log into a web application, I would inspect the logs for failed requests, error messages, authentication problems, or other clues. Logs do not always reveal the complete cause, but they provide useful evidence for further investigation.

Monitoring logs and metrics serves different purposes. Logs describe specific events, such as a successful HTTP request or a 404 error when a page cannot be found. Metrics provide numerical measurements, such as CPU percentage, memory consumption, and network traffic. Using both helps engineers understand what happened and whether the application is using resources efficiently.

Large enterprise companies often use centralized monitoring platforms to manage thousands of containers. Tools such as Prometheus can collect and store metrics, while Grafana can display those measurements through dashboards and alerts. Centralized logging systems can also gather logs from different servers and containers, making it easier for operations teams to investigate problems across a large infrastructure.

My ability to troubleshoot Linux environments is improving through hands-on activities. I am becoming more familiar with commands that check memory, disk capacity, running processes, and container status. I am also learning how to generate HTTP requests, examine application logs, and monitor Docker resource usage. This laboratory helps me understand that cloud operations involves more than deploying applications. Engineers must continuously observe system health, investigate problems using evidence, and respond before small issues become major service disruptions.

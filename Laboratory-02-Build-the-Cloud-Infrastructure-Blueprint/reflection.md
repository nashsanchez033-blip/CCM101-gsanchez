# Mission Reflection

##Mission Reflection

### 1. Which cloud infrastructure component do you think is the most important? Why?

For me, the most important cloud infrastructure component is the **networking resource** because it allows the different parts of a cloud environment to communicate. During the investigation, I found the `enp1s0` interface with the IP address `172.30.1.2`, as well as the `docker0` interface with `172.17.0.1`. Even if a server has enough CPU, RAM, and storage, those resources would be much less useful if the system could not communicate with other devices or services.

### 2. How does Linux support cloud computing?

Linux supports cloud computing by providing a stable and flexible operating system for managing servers and cloud resources. In this laboratory, I used Linux commands such as `lscpu`, `free -h`, `df -h`, `ip a`, and `uname` to investigate the virtual server. Linux also makes it possible to manage system resources, networking, files, and processes through the command line.

### 3. Why is technical documentation important before deploying infrastructure?

Technical documentation is important because it provides a clear record of the infrastructure and the decisions made before deployment. It can help prevent mistakes, make troubleshooting easier, and allow other people to understand how the system is configured. In this laboratory, documenting the server's CPU, RAM, storage, operating system, and network information made the investigation easier to review.

### 4. What new skills did you learn during this laboratory activity?

I learned how to investigate a Linux server using command-line tools and interpret system information. I also learned how to identify cloud infrastructure components, compare services from AWS, Azure, and Google Cloud, create a basic cloud architecture, and organize technical information using Markdown.

### 5. How has your GitHub portfolio improved after completing this mission?

My GitHub portfolio became more organized and meaningful because it now contains documentation of an actual cloud computing laboratory. The files show my investigation results, cloud infrastructure concepts, provider comparison, and reflection. This makes the repository more useful as a record of the skills and activities I completed during the laboratory.

## Overall Reflection

This mission gave me a better understanding of what is happening behind a cloud environment. Instead of only learning definitions, I was able to investigate a real virtual Linux environment and connect the information from the terminal to cloud computing concepts. It also showed me that proper documentation and basic Linux skills are important foundations for working with cloud infrastructure.

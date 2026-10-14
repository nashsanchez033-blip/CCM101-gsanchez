# Mission Reflection

A host-based firewall protects a server by controlling the network traffic that enters and leaves the operating system. Even if an attacker manages to bypass the physical network perimeter, the firewall can still block unauthorized connections to services running on the server. This provides an additional layer of security and helps reduce the chances of a successful attack.

Managing open network ports is important because every exposed port can become a possible entry point for attackers. When unnecessary ports are left open, attackers may discover vulnerable services and attempt to exploit them. Closing unused ports and allowing only the required services helps reduce the server's attack surface.

In a real enterprise environment, leaving a database port such as MySQL port 3306 open to the public internet is dangerous. Attackers could attempt password guessing, exploit database vulnerabilities, or gain unauthorized access to sensitive information. Database services should normally be restricted to trusted application servers or private networks rather than being directly accessible to everyone.

Completing this mission helped me understand that server security requires careful planning and proper configuration. Before this activity, I mainly focused on making applications run successfully. Now, I understand that deploying a working application is not enough because an incorrectly configured server can expose important services to attackers. I also learned why allowing SSH access before activating a firewall is important for preventing accidental lockouts.

My GitHub cloud computing portfolio is becoming more complete as I progress through eight laboratory missions. Each activity demonstrates a different skill, including Linux commands, Docker deployment, cloud storage, monitoring, and security. Having these documented projects helps me track my improvement and shows how my understanding of cloud infrastructure has developed. This laboratory strengthened my confidence in applying basic security practices and encouraged me to be more careful when configuring cloud servers.

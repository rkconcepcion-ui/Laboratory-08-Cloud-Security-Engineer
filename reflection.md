# Mission Reflection — The Cloud Security Engineer

Completing this laboratory activity helped me understand the importance of securing a cloud server using a host-based firewall. I learned that deploying a web application is not enough because the server must also be protected from unauthorized network access. By using Docker, I deployed an Nginx web server and tested its response using the curl command.

A host-based firewall provides an additional layer of protection even if the physical network perimeter is breached. It controls incoming and outgoing traffic directly on the server according to configured rules. This defense-in-depth approach helps reduce the risk of unauthorized connections reaching running services.

Managing open network ports is also important because every exposed port can provide a possible entry point for attackers. By applying a default-deny incoming policy and allowing only necessary services, administrators can reduce the server's attack surface. In this activity, I learned how to allow SSH for remote administration and TCP port 8080 for the web application.

In a real enterprise environment, leaving a database port such as MySQL's port 3306 open to the public internet is dangerous. Attackers could attempt unauthorized logins, exploit software vulnerabilities, or access sensitive information if other security controls are weak. Database access should be restricted to trusted application servers and authorized administrators.

This mission changed my perspective by showing me that a server can become vulnerable when network access is not configured carefully. Security requires deliberate configuration, regular monitoring, and verification rather than simply installing an application.

Finally, having eight completed cloud computing missions in my GitHub portfolio would demonstrate my growing knowledge of cloud infrastructure, deployment, operations, and security. The portfolio also gives me a place to document my commands, screenshots, and lessons learned. Overall, this activity strengthened my understanding that protecting cloud resources requires both technical skills and responsible security practices.

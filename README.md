# EdgeDeploy - Project Abstract

**EdgeDeploy** is a cloud deployment platform inspired by modern hosting providers such as Vercel and Cloudflare Pages. It enables developers to connect a GitHub repository, automatically build their application, and deploy it to a globally accessible hosting environment with minimal configuration. The project demonstrates the core concepts behind modern Platform-as-a-Service (PaaS) solutions by implementing a complete deployment pipeline and content delivery architecture from scratch.

The system begins by authenticating users and allowing them to register projects linked to GitHub repositories. Whenever a deployment is triggered, the platform clones the repository, installs dependencies, executes the build process, and stores the generated static assets. These artifacts are then served through an origin server, forming the foundation for website hosting.

To improve performance and scalability, EdgeDeploy incorporates a simplified Content Delivery Network (CDN). Multiple edge servers cache frequently requested files, reducing latency and minimizing repeated requests to the origin server. Cache management techniques such as Time-to-Live (TTL), Least Recently Used (LRU) eviction, and cache invalidation ensure that newly deployed content is propagated efficiently while maintaining consistency across edge nodes.

The platform also includes a load balancer that distributes incoming traffic among multiple edge servers using routing strategies such as Round Robin and health checks. A rate-limiting layer protects the infrastructure from excessive traffic and abuse by implementing industry-standard algorithms like Fixed Window, Sliding Window, or Token Bucket. Together, these components simulate the architecture used by large-scale cloud hosting providers to achieve high availability, reliability, and efficient resource utilization.

A web-based dashboard allows developers to manage projects, trigger deployments, monitor deployment status, and view analytics such as request counts, cache hit/miss ratios, and deployment history. An administrative interface provides system monitoring, user management, and infrastructure oversight.

The project is implemented using **Node.js**, **Express.js**, **MySQL**, and **Next.js**, with GitHub APIs enabling repository integration and automated deployments. The architecture emphasizes modular design, RESTful APIs, secure authentication using JWT, and scalable backend services.

Beyond being a deployment platform, EdgeDeploy serves as a comprehensive educational project covering backend engineering, distributed systems, DevOps fundamentals, networking, caching, load balancing, authentication, CI/CD automation, and cloud infrastructure. It provides practical exposure to the technologies and architectural principles used in real-world cloud platforms, making it an effective learning experience as well as a functional software system.

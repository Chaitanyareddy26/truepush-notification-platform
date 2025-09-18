# TruePush Notification Platform

### Overview
TruePush Notification Platform is a marketing automation platform that enables businesses to send targeted push notifications, emails, and in‑app messages to customers. It's built using Java, Redis, and integrates campaign analytics to deliver personalized engagement at scale.

### Tech Stack
- **Backend:** Java 17, Spring Boot, Redis, PostgreSQL, Hibernate
- **Messaging:** Redis (Pub/Sub) for real‑time notifications
- **Analytics:** Custom analytics module for campaign performance
- **Containerization:** Docker and Kubernetes for deployment
- **CI/CD:** GitHub Actions for continuous integration and deployment

### Architecture
This project follows a microservices architecture:
- **Notification Service:** Handles the creation and sending of notifications via Redis pub/sub.
- **User Service:** Manages users and their segmentation data.
- **Analytics Service:** Collects and aggregates campaign performance metrics.
- **Gateway:** API gateway for routing requests between services.

### Key Features
- Manage notification templates and campaigns.
- Segment customers based on demographics and activity.
- Schedule one‑off or recurring push notifications.
- Real‑time delivery using Redis channels.
- Capture click‑through and open rates with analytics dashboards.
- Scale with container orchestration.

### Getting Started
1. **Clone the repository:**
   ```bash
   git clone https://github.com/Chaitanyareddy26/truepush-notification-platform.git
   cd truepush-notification-platform
   ```
2. **Configure the environment:**
   - Ensure Redis and PostgreSQL are installed and running.
   - Copy `.env.sample` to `.env` and update database and Redis credentials.
3. **Build and run the services:**
   ```bash
   mvn clean package
   java -jar target/notification-platform-0.0.1-SNAPSHOT.jar
   ```
4. **Using Docker and Kubernetes:**
   - Use the Dockerfile in the `deploy` directory to build images.
   - Deploy to Kubernetes using manifests in `deploy/k8s`.

### My Role & Impact
As a Java engineer on the TruePush project, I built core modules for message dispatch, implemented Redis pub/sub integration, and designed analytics components to monitor campaign performance. I optimized database queries to reduce response times by 30% and implemented automated tests to ensure reliability.

### Contributing
Please see the CONTRIBUTING.md file for guidelines on how to contribute to this project.

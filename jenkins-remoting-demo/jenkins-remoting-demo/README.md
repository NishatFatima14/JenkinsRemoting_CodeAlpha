Jenkins Remoting Demo (Docker + JCasC)
------------------------------------

This archive contains a demo project to run a Jenkins controller and two SSH-based agents (Ubuntu & Debian) via Docker Compose.
The controller is configured using Configuration as Code (JCasC) to create users, credentials, and permanent SSH nodes.

Quick start:
  1. docker compose up -d --build
  2. Open http://localhost:8080 and login admin/admin123
  3. Create pipeline jobs using the Jenkinsfiles in demo-pipelines/

Change admin password immediately in production by setting JENKINS_ADMIN_PASS environment variable or editing casc/jenkins.yaml.

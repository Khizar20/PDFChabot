# PDF Chat Application

## Deployment Requirements
- Docker
- Docker Compose
- AWS EC2 instance

## Setup Instructions
1. Clone the repository
2. Create `.env` file with required variables
3. Run `docker-compose up -d`

## Accessing the Application
- Web interface: http://<ec2-public-ip>
- API docs: http://<ec2-public-ip>:8000/docs

## Environment Variables
- MONGODB_URI
- SECRET_KEY
- GROQ_API_KEY

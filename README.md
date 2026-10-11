# DevOps Task 1 - Git Workflow and Project Baseline

A small Node.js sample application created for Task 1 of the DevOps internship.

## Project Structure

```text
devops-task-1/
├── public/
│   └── index.html
├── .gitignore
├── BRANCHING.md
├── README.md
├── package.json
└── server.js
```

## Prerequisites

- Git
- Node.js 18+ and npm

## Run Locally

Clone the repository:

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd devops-task-1
```

Install dependencies:

```bash
npm install
```

Start the application:

```bash
npm start
```

Open:

http://localhost:3000

## Git Workflow

The project follows a simple branch-based workflow:

- `main` - stable/release-ready code
- `develop` - integration branch for completed features
- `feature/*` - short-lived branches for individual features or changes

Typical flow:

```text
feature/* -> develop -> main
```

See [BRANCHING.md](BRANCHING.md) for details.

## Git Commit Examples

```bash
git add .
git commit -m "feat: add sample Node.js application"
git push origin feature/sample-app
```

## Task Requirements Covered

- README.md
- .gitignore
- Branching notes
- Small sample application
- Git-based project workflow

## Docker Deployment

### Prerequisites
- Docker Desktop installed and running
- Git

### Build Docker Image
```powershell
docker build -t swynex-node-app .
```

### Run the Application
```powershell
docker run --rm -d --name swynex-app -p 3000:3000 swynex-node-app
```

Open your browser at: http://localhost:3000

### Verify the Container
```powershell
docker ps
curl.exe -i http://localhost:3000
```

### Stop the Application
```powershell
docker stop swynex-app
```

### Build and Run Summary
The application runs inside a Docker container using Node.js 20 Alpine.
Port 3000 is mapped from the container to the host machine.
The Docker image can be rebuilt from the included Dockerfile.

# Career Catalyst

> AI-powered job search automation platform to streamline the application process

[![Status](https://img.shields.io/badge/status-in%20development-yellow)](https://github.com/thejollydev/career-catalyst)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)

## 🎯 Project Overview

A comprehensive job search management platform that automates tedious aspects of the job hunt while providing AI-powered insights and suggestions. Built to solve real problems faced during career transitions.

**🚧 Currently in active development - check back soon!**

## ✨ Features (Planned)

- 📝 **Application Tracking** - Comprehensive status management with follow-up scheduling
- 🤖 **AI Resume Customization** - LLM-powered bullet point generation tailored to job descriptions
- 🔍 **Job Scraping** - Automated collection from multiple job boards
- 📊 **Keyword Analysis** - Match your skills against job requirements
- 📅 **Interview Prep** - Organize practice questions and STAR method stories
- 📈 **Analytics Dashboard** - Track response rates and optimize strategy

## 🛠️ Tech Stack

**Backend:**
- FastAPI (REST API framework)
- PostgreSQL (primary database)
- SQLAlchemy (ORM)
- Celery (background task processing)
- Redis (task queue & caching)

**AI/ML:**
- Ollama (local LLM hosting)
- LangChain (LLM integration)
- Custom prompt engineering

**DevOps:**
- Docker & Docker Compose
- GitHub Actions (CI/CD)
- Prometheus metrics
- pytest (testing with 80%+ coverage goal)

## 🏗️ Architecture
```
┌─────────────────────┐
│   FastAPI REST API  │ ← OpenAPI/Swagger docs
└──────────┬──────────┘
           │
    ┌──────┴──────┐
    │             │
┌───▼────┐  ┌────▼────┐
│PostgreSQL│  │  Redis  │
│Database  │  │ Cache   │
└──────────┘  └────┬────┘
                   │
              ┌────▼────┐
              │ Celery  │ ← Background tasks
              │ Workers │
              └────┬────┘
                   │
              ┌────▼────┐
              │  Ollama │ ← LLM inference
              │   LLM   │
              └─────────┘
```

## 🚀 Quick Start (Coming Soon)
```bash
# Clone the repository
git clone https://github.com/thejollydev/career-catalyst.git
cd career-catalyst

# Set up environment
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Run with Docker Compose
docker-compose up -d

# Access API documentation
open http://localhost:8000/docs
```

## 📊 Database Schema

Core tables include:
- `jobs` - Job postings with extracted keywords
- `applications` - Application tracking with status workflow
- `companies` - Company information and metadata
- `contacts` - Networking and referral management
- `resume_versions` - Track customized resumes per application

## 🧪 Testing
```bash
# Run tests with coverage
pytest --cov=app tests/

# Target: 80%+ coverage
```

## 📝 Blog Post

Read about the development process: [Building an AI-Powered Job Search Platform](https://soper.dev) *(coming soon)*

## 🔗 Related Projects

- [JollyLab Infrastructure](https://github.com/thejollydev/jolly-lab-infrastructure) - Homelab hosting this application
- [Homelab Pulse](https://github.com/thejollydev/homelab-pulse) - Monitoring dashboard

## 📫 Contact

- Portfolio: [soper.dev](https://soper.dev)
- LinkedIn: [joseph-soper-dev](https://www.linkedin.com/in/joseph-soper-dev/)
- GitHub: [@thejollydev](https://www.github.com/thejollydev)
- Email: joseph@soper.dev

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

# NyayaMitra - AI Lawyer Assistant 🏛️⚖️

[![AWS](https://img.shields.io/badge/AWS-Bedrock%20%7C%20Lex%20%7C%20Translate-orange)](https://aws.amazon.com/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-green)](https://fastapi.tiangolo.com/)
[![Python](https://img.shields.io/badge/Python-3.9+-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> An AI-powered lawyer assistant that provides legal advice and assistance to people who cannot find relevant lawyers for their cases or face barriers in accessing legal help.

## 🎯 Problem Statement

Many individuals face critical challenges in accessing legal representation:
- Cannot find lawyers who specialize in their specific case type
- Lawyers refuse cases due to low fees or complexity
- Geographic barriers in rural and remote areas
- Financial constraints making legal fees prohibitive
- Urgent legal needs when lawyers are unavailable

**NyayaMitra** bridges this gap by providing AI-powered legal assistance 24/7.

## ✨ Features

- 🤖 **AI-Powered Legal Advice**: Case-specific guidance using Amazon Bedrock
- 💬 **Conversational Interface**: Natural chat experience with Amazon Lex
- 🌐 **Multilingual Support**: English and Hindi via Amazon Translate
- 📄 **Document Analysis**: Upload and analyze legal documents
- 📚 **Legal Research**: Search IPC, labor laws, constitutional provisions
- ⚡ **Instant Responses**: 24/7 availability for legal queries
- 🔒 **Privacy First**: No permanent storage of sensitive information

## 🏗️ Architecture

```
User Interface (React.js)
        ↓
AWS API Gateway
        ↓
FastAPI Backend (EC2/Lambda)
        ↓
    ┌───┴───┐
    ↓       ↓
Amazon      Amazon
Bedrock     OpenSearch
(LLM)       (Vector DB)
```

## 🛠️ Tech Stack

### Backend
- **Framework**: FastAPI (Python)
- **LLM**: Amazon Bedrock (Claude/Titan)
- **Conversational AI**: Amazon Lex
- **Translation**: Amazon Translate
- **Database**: PostgreSQL / DynamoDB
- **Vector DB**: Amazon OpenSearch
- **RAG**: LangChain / LlamaIndex

### Frontend
- **Core**: HTML5, CSS3, JavaScript
- **Framework**: React.js
- **UI Library**: Material-UI / Bootstrap

### AWS Infrastructure
- EC2 / Lambda (Compute)
- API Gateway
- S3 (Storage)
- CloudWatch (Monitoring)
- Secrets Manager

## 📋 Prerequisites

- Python 3.9+
- AWS Account with access to:
  - Amazon Bedrock
  - Amazon Lex
  - Amazon Translate
  - Amazon OpenSearch
- Node.js 16+ (for frontend)
- Git

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/nyayamitra.git
cd nyayamitra
```

### 2. Backend Setup

```bash
cd backend

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Configure AWS credentials
aws configure

# Set environment variables
cp .env.example .env
# Edit .env with your AWS credentials and configuration

# Run the server
uvicorn app.main:app --reload
```

### 3. Frontend Setup

```bash
cd frontend

# Install dependencies
npm install

# Start development server
npm start
```

### 4. Access the Application

- Frontend: http://localhost:3000
- Backend API: http://localhost:8000
- API Docs: http://localhost:8000/docs

## 📁 Project Structure

```
nyayamitra/
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── api/
│   │   ├── core/
│   │   ├── models/
│   │   └── services/
│   ├── requirements.txt
│   └── Dockerfile
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── services/
│   │   └── App.js
│   └── package.json
├── docs/
│   ├── Requirements.md
│   └── Design.md
├── .gitignore
└── README.md
```

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the backend directory:

```env
# AWS Configuration
AWS_REGION=us-east-1
AWS_ACCESS_KEY_ID=your_access_key
AWS_SECRET_ACCESS_KEY=your_secret_key

# Amazon Bedrock
BEDROCK_MODEL_ID=anthropic.claude-v2

# Database
DATABASE_URL=postgresql://user:password@localhost/nyayamitra

# API Configuration
API_HOST=0.0.0.0
API_PORT=8000
```

## 📖 API Documentation

Once the backend is running, visit:
- Swagger UI: http://localhost:8000/docs
- ReDoc: http://localhost:8000/redoc

### Key Endpoints

```
POST /api/v1/chat          - Send legal query
POST /api/v1/document      - Upload document for analysis
GET  /api/v1/session       - Get conversation history
GET  /api/v1/health        - Health check
```

## 🧪 Testing

```bash
# Backend tests
cd backend
pytest

# Frontend tests
cd frontend
npm test
```

## 🚢 Deployment

### AWS Lambda Deployment

```bash
# Package the application
cd backend
pip install -r requirements.txt -t package/
cd package
zip -r ../deployment.zip .
cd ..
zip -g deployment.zip app/*

# Deploy to Lambda (using AWS CLI)
aws lambda update-function-code \
    --function-name nyayamitra-api \
    --zip-file fileb://deployment.zip
```

### Docker Deployment

```bash
# Build Docker image
docker build -t nyayamitra-backend ./backend

# Run container
docker run -p 8000:8000 --env-file .env nyayamitra-backend
```

## 🔒 Security & Privacy

- ✅ End-to-end encryption (HTTPS/TLS)
- ✅ No permanent storage of PII
- ✅ Automatic document deletion after processing
- ✅ AWS Secrets Manager for credentials
- ✅ Compliance with data protection regulations

## ⚠️ Disclaimer

**NyayaMitra is an AI-powered lawyer assistant that provides legal advice and guidance but does not replace a licensed human lawyer.** While the system offers professional-grade legal assistance, users should consult qualified legal professionals for critical legal matters, court representation, or when human judgment is essential.

## 🎯 Target Users

- Individuals without legal representation
- People in rural/remote areas with limited access to lawyers
- Those who cannot afford legal fees
- Self-representing litigants
- Anyone needing quick legal guidance

## 🗺️ Roadmap

- [ ] Voice input/output support
- [ ] Mobile applications (iOS/Android)
- [ ] Multi-jurisdiction support
- [ ] Integration with court filing systems
- [ ] Lawyer referral network
- [ ] Advanced case outcome prediction

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guidelines](CONTRIBUTING.md) first.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Team

- **Project Lead**: [Your Name]
- **Backend Developer**: [Name]
- **Frontend Developer**: [Name]
- **AI/ML Engineer**: [Name]

## 📧 Contact

For questions or support, please contact:
- Email: support@nyayamitra.com
- GitHub Issues: [Create an issue](https://github.com/yourusername/nyayamitra/issues)

## 🙏 Acknowledgments

- Amazon Web Services for AI services
- LangChain community
- Open source legal databases
- All contributors and supporters

---

**Built with ❤️ for accessible justice**

**Hackathon Project** | **AI/ML** | **Legal Tech** | **Social Impact**

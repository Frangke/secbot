# Security Lake Chatbot

AWS Security Lake 데이터를 분석하는 전문 보안 분석 챗봇 시스템입니다.

## Project Structure

```
security-lake-chatbot/
├── app/                    # FastAPI application
│   ├── __init__.py
│   ├── main.py            # FastAPI app entry point
│   ├── api/               # API routes
│   ├── core/              # Core business logic
│   ├── models/            # Data models
│   ├── services/          # Service layer
│   └── templates/         # HTML templates
├── static/                # Static files (CSS, JS)
├── tests/                 # Test files
├── scripts/               # Utility scripts
├── requirements.txt       # Python dependencies
├── .env.example          # Environment variables template
└── config.py             # Configuration management
```

## Quick Setup

### Option 1: Interactive Setup (Recommended)
```bash
python scripts/setup_and_test.py
```
This will guide you through:
- Creating virtual environment
- Installing dependencies  
- Configuring AWS credentials
- Testing connectivity

### Option 2: Manual Setup
1. Create virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Copy and configure environment variables:
```bash
cp .env.example .env
# Edit .env with your AWS credentials and configuration
```

4. Test AWS connectivity:
```bash
python scripts/test_aws_connectivity.py
```

5. Run the application:
```bash
uvicorn app.main:app --reload
```

## Development

- FastAPI backend with HTMX frontend
- Amazon Bedrock Claude 3.5 v1 integration
- AWS Security Lake data analysis
- DynamoDB session management
# Pegasus AI - Advanced AI-Powered Penetration Testing Framework

<p align="center">
  <img src="https://img.shields.io/badge/Version-0.3.2-blue.svg" alt="Version">
  <img src="https://img.shields.io/badge/Python-3.12-green.svg" alt="Python">
  <img src="https://img.shields.io/badge/License-Apache%202.0-yellow.svg" alt="License">
  <img src="https://img.shields.io/badge/Security-CEH%20%7C%20OSCP%20%7C%20OSCE-red.svg" alt="Security">
</p>

## 🦅 About Pegasus AI

Pegasus AI is a cutting-edge, open-source AI-powered cybersecurity framework designed for automated penetration testing and vulnerability assessment. Built with advanced AI agents, it combines the power of large language models with comprehensive security tooling to perform sophisticated security assessments on web applications, APIs, and infrastructure.

## 👨‍⚕️ Author

**Lettu Kes dr. Muhammad Sobri Maulana, S.Kom, CEH, OSCP, OSCE**

- 📧 Email: [muhammadsobrimaulana31@gmail.com](mailto:muhammadsobrimaulana31@gmail.com)
- 🌐 Website: [https://muhammadsobrimaulana.netlify.app](https://muhammadsobrimaulana.netlify.app)
- 🔗 GitHub: [github.com/sobri3195](https://github.com/sobri3195)

### 📱 Connect with Me

- 🎥 YouTube: [@muhammadsobrimaulana6013](https://www.youtube.com/@muhammadsobrimaulana6013)
- 📱 TikTok: [@dr.sobri](https://www.tiktok.com/@dr.sobri)
- 💬 Telegram: [@winlin_exploit](https://t.me/winlin_exploit)
- 👥 WhatsApp Group: [Join Security Community](https://chat.whatsapp.com/B8nwRZOBMo64GjTwdXV8Bl)
- 📝 Blog: [muhammad-sobri-maulana-kvr6a.sevalla.page](https://muhammad-sobri-maulana-kvr6a.sevalla.page/)

## ✨ Key Features

### 🤖 AI-Powered Testing
- **Intelligent Agent System**: Multi-agent architecture for autonomous security testing
- **LLM Integration**: Supports OpenAI, Anthropic, and local models (Ollama, LMStudio)
- **Adaptive Testing**: AI learns and adapts testing strategies based on target responses

### 🎯 Comprehensive Pentesting Capabilities

#### 🌐 Web Application Testing
- **OWASP Top 10 Coverage**: Automated detection of SQL injection, XSS, CSRF, and more
- **Authentication Testing**: Advanced session management and authentication bypass techniques
- **API Security**: REST and GraphQL API vulnerability assessment
- **Business Logic Flaws**: AI-powered detection of complex logic vulnerabilities

#### 🔍 Reconnaissance & Information Gathering
- **Subdomain Enumeration**: Automated subdomain discovery
- **Port Scanning**: Intelligent port and service detection
- **Web Crawling**: Deep web application mapping
- **Technology Detection**: Fingerprinting of frameworks, libraries, and versions

#### 🛡️ Advanced Security Analysis
- **Code Analysis**: Static analysis for security vulnerabilities
- **Secret Detection**: Automated detection of exposed credentials and API keys
- **SSL/TLS Testing**: Certificate and encryption analysis
- **Security Headers**: Comprehensive header security assessment

#### 🎭 MITM & Proxy Features
- **Integrated Caido Proxy**: Built-in MITM proxy for traffic interception
- **Request Manipulation**: Automated request fuzzing and manipulation
- **Response Analysis**: AI-powered response pattern analysis
- **Certificate Management**: Automatic CA certificate generation and trust

### 🐳 Containerized Environment
- **Docker-Based Sandbox**: Isolated testing environment
- **Pre-configured Tools**: Includes Nmap, Nuclei, SQLMap, and 50+ pentesting tools
- **Persistent Workspaces**: Multi-target testing with organized results

### 📊 Reporting & Documentation
- **Automated Reports**: Comprehensive vulnerability reports with proof-of-concepts
- **CVSS Scoring**: Industry-standard vulnerability severity ratings
- **Remediation Guidance**: AI-generated fix recommendations
- **Export Formats**: JSON, HTML, and Markdown report generation

## 🚀 Quick Start

### Prerequisites

- Python 3.12 or higher
- Docker Desktop or Docker Engine
- 4GB+ RAM recommended
- Git

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/sobri3195/pegasus-ai.git
cd pegasus-ai
```

2. **Install dependencies with Poetry**
```bash
# Install Poetry if you haven't already
curl -sSL https://install.python-poetry.org | python3 -

# Install project dependencies
poetry install
```

3. **Configure environment variables**
```bash
# Set your LLM provider (OpenAI, Anthropic, Ollama, etc.)
export PEGASUS_AI_LLM="openai/gpt-4"
export LLM_API_KEY="your-api-key-here"

# Optional: For local models
export LLM_API_BASE="http://localhost:11434"  # Ollama default

# Optional: For web search capabilities
export PERPLEXITY_API_KEY="your-perplexity-key"
```

4. **Run Pegasus AI**
```bash
# Interactive mode with TUI
pegasus-ai --target https://example.com

# Non-interactive mode
pegasus-ai --target https://example.com --non-interactive

# Multiple targets
pegasus-ai --target https://example.com --target https://staging.example.com

# With custom instructions
pegasus-ai --target https://example.com --instruction "Focus on authentication vulnerabilities"
```

## 📖 Usage Examples

### Web Application Penetration Test
```bash
pegasus-ai --target https://example.com
```

### GitHub Repository Security Analysis
```bash
pegasus-ai --target https://github.com/user/repo
pegasus-ai --target git@github.com:user/repo.git
```

### Local Code Analysis
```bash
pegasus-ai --target ./my-project
```

### Domain Penetration Test
```bash
pegasus-ai --target example.com
```

### Multi-Target White-Box Testing
```bash
# Test both source code and deployed application
pegasus-ai --target https://github.com/user/repo --target https://example.com

# Test multiple environments
pegasus-ai --target ./source-code --target https://staging.example.com --target https://prod.example.com
```

### Custom Testing Instructions
```bash
# Focus on specific vulnerability types
pegasus-ai --target example.com --instruction "Focus on IDOR and XSS vulnerabilities"

# Provide test credentials
pegasus-ai --target https://example.com --instruction "Use credentials: admin:password123 to access the application"

# Target specific endpoints
pegasus-ai --target https://api.example.com --instruction "Focus on /api/users and /api/admin endpoints"
```

## 🛠️ Development

### Setup Development Environment
```bash
# Install development dependencies
make setup-dev

# Run code formatting
make format

# Run linting
make lint

# Run type checking
make type-check

# Run security checks
make security

# Run all checks
make check-all

# Run tests
make test

# Run tests with coverage
make test-cov
```

### Project Structure
```
pegasus-ai/
├── pegasus_ai/
│   ├── agents/          # AI agent implementations
│   ├── interface/       # CLI and TUI interfaces
│   ├── llm/            # LLM integration and configuration
│   ├── runtime/        # Docker runtime and sandboxing
│   ├── telemetry/      # Logging and tracing
│   └── tools/          # Pentesting tools and actions
├── containers/         # Docker configuration
├── tests/             # Test suite
├── pyproject.toml     # Project configuration
└── Makefile          # Development commands
```

## 🎓 Training & Resources

### Video Tutorials
Visit my [YouTube Channel](https://www.youtube.com/@muhammadsobrimaulana6013) for comprehensive tutorials on:
- Setting up Pegasus AI
- Advanced penetration testing techniques
- Security best practices
- Real-world vulnerability demonstrations

### Community Support
Join our [WhatsApp Community](https://chat.whatsapp.com/B8nwRZOBMo64GjTwdXV8Bl) to:
- Get help with installation and usage
- Share security findings (responsibly)
- Discuss penetration testing methodologies
- Connect with other security professionals

## 💝 Support the Project

If you find Pegasus AI useful, please consider supporting the development:

### ☕ Buy Me a Coffee
- 🔗 [Lynk.id - muhsobrimaulana](https://lynk.id/muhsobrimaulana)
- 🔗 [Trakteer.id](https://trakteer.id/g9mkave5gauns962u07t)
- 🔗 [Nyawer.co](https://nyawer.co/MuhammadSobriMaulana)
- 🔗 [KaryaKarsa](https://karyakarsa.com/muhammadsobrimaulana)

### 🛍️ Products & Services
- 🔗 [Gumroad Store](https://maulanasobri.gumroad.com/)

Your support helps maintain and improve Pegasus AI! 🙏

## 📋 Configuration

### Environment Variables

| Variable | Description | Required | Default |
|----------|-------------|----------|---------|
| `PEGASUS_AI_LLM` | LLM model to use (e.g., 'openai/gpt-4') | ✅ Yes | - |
| `LLM_API_KEY` | API key for LLM provider | ✅ Yes* | - |
| `LLM_API_BASE` | Custom API base URL for local models | ❌ No | - |
| `PERPLEXITY_API_KEY` | API key for Perplexity web search | ❌ No | - |
| `PEGASUS_AI_IMAGE` | Custom Docker image for sandbox | ❌ No | Official image |

*Not required if using local models with `LLM_API_BASE`

### Supported LLM Providers

- **OpenAI**: `openai/gpt-4`, `openai/gpt-3.5-turbo`
- **Anthropic**: `anthropic/claude-3-opus`, `anthropic/claude-3-sonnet`
- **Ollama**: `ollama/llama2`, `ollama/codellama`
- **LMStudio**: Set `LLM_API_BASE` to your LMStudio endpoint
- **Azure OpenAI**: `azure/gpt-4`
- And many more via LiteLLM integration

## 🔧 Advanced Features

### Custom Agent Instructions
Fine-tune the AI agent's behavior with custom instructions:
```bash
pegasus-ai --target example.com --instruction "
- Focus on authentication and authorization vulnerabilities
- Test for IDOR in user profile endpoints
- Check for SQL injection in search functionality
- Use the following test accounts: user1:pass1, admin:admin123
"
```

### Persistent Workspaces
All scan results are saved in organized workspaces:
```
agent_runs/
└── <run-name>/
    ├── vulnerabilities/     # Discovered vulnerabilities
    ├── reports/            # Generated reports
    ├── evidence/           # Proof-of-concept screenshots
    └── notes/             # Agent analysis notes
```

### Tool Integration
Pegasus AI integrates with industry-standard tools:
- **Nmap**: Port scanning and service detection
- **Nuclei**: Template-based vulnerability scanning
- **SQLMap**: Automated SQL injection exploitation
- **Subfinder**: Subdomain enumeration
- **FFuf**: Web fuzzing
- **Katana**: Web crawling
- **TruffleHog**: Secret detection
- **Semgrep**: Static code analysis
- **And many more...**

## 🔒 Security & Responsible Use

### ⚠️ Legal Disclaimer
Pegasus AI is designed for **authorized security testing only**. You must have explicit permission to test any target system. Unauthorized access to computer systems is illegal.

### Best Practices
1. **Authorization**: Always obtain written permission before testing
2. **Scope**: Stay within the defined testing scope
3. **Disclosure**: Follow responsible disclosure practices
4. **Data**: Handle discovered vulnerabilities and data responsibly
5. **Compliance**: Comply with all applicable laws and regulations

### Target Recommendations
- Test on your own systems
- Use bug bounty platforms (HackerOne, Bugcrowd, etc.)
- Practice on intentionally vulnerable applications (DVWA, WebGoat, etc.)
- Use isolated lab environments

## 🤝 Contributing

We welcome contributions! Please see our contribution guidelines:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make your changes and add tests
4. Ensure all tests pass: `make test`
5. Run code quality checks: `make check-all`
6. Commit your changes: `git commit -m 'Add amazing feature'`
7. Push to the branch: `git push origin feature/amazing-feature`
8. Open a Pull Request

## 📄 License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- OpenAI, Anthropic, and other LLM providers for making AI accessible
- The open-source security community for their amazing tools
- All contributors and supporters of Pegasus AI

## 📞 Contact & Support

- **Email**: [muhammadsobrimaulana31@gmail.com](mailto:muhammadsobrimaulana31@gmail.com)
- **Telegram**: [@winlin_exploit](https://t.me/winlin_exploit)
- **WhatsApp Group**: [Join Community](https://chat.whatsapp.com/B8nwRZOBMo64GjTwdXV8Bl)
- **Website**: [muhammadsobrimaulana.netlify.app](https://muhammadsobrimaulana.netlify.app)

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/sobri3195">Dr. Muhammad Sobri Maulana</a>
</p>

<p align="center">
  <strong>🔐 Stay Secure, Test Responsibly 🔐</strong>
</p>

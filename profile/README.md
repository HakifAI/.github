# HakifAI Aptos AI Agent

<div align="center">
  <img src="https://github.com/HakifAI/aptos-agent-fe/blob/5939aea4fc3436144f17b1bdd09e5438cc05670e/public/logo.svg" alt="HakifAI Logo" width="250"/>
  
  **Conversational AI interface for Aptos blockchain. Execute DeFi operations, manage wallets, and trade tokens through natural language chat.**
  
  🌐 **[Try Live Demo](https://ai.hakifi.xyz)** | 📖 [Documentation](#-documentation) | 🚀 [Quick Start](#-quick-start)
  
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
  [![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
  [![Next.js](https://img.shields.io/badge/Next.js-000000?logo=next.js&logoColor=white)](https://nextjs.org/)
  [![NestJS](https://img.shields.io/badge/NestJS-E0234E?logo=nestjs&logoColor=white)](https://nestjs.com/)
  [![Aptos](https://img.shields.io/badge/Aptos-000000?logo=aptos&logoColor=white)](https://aptos.dev/)
</div>

## 🚀 Overview

HakifAI Aptos AI Agent is a sophisticated blockchain interface that revolutionizes DeFi interaction through conversational AI. Built for the Aptos ecosystem, it enables users to perform complex DeFi operations, manage digital assets, and execute transactions using natural language commands.

The project demonstrates cutting-edge integration of AI agents with blockchain technology, providing an intuitive interface that makes DeFi accessible to users of all technical backgrounds.

### 🎯 What Makes This Special

- **Natural Language DeFi**: Execute complex blockchain operations through simple conversation
- **Multi-Modal AI**: Supports text, voice, and visual interaction methods
- **Secure by Design**: Enterprise-grade security with encrypted wallet management
- **Full-Stack Integration**: Seamless connection between AI, blockchain, and user interface
- **Real-Time Market Data**: Live integration with DEXs and market data providers

## 🏗️ Architecture

The project consists of three integrated components working in harmony:

```mermaid
graph TB
    A[User Interface] --> B[Frontend - Next.js]
    B --> C[Backend API - NestJS]
    C --> D[AI Agent - LangGraph.js]
    D --> E[Aptos Blockchain]
    
    B --> F[Wallet Integration]
    C --> G[PostgreSQL Database]
    D --> H[DEX Protocols]
    
    subgraph "Frontend Features"
        I[Chat Interface]
        J[Portfolio Management]
        K[Transaction History]
        L[Real-time Notifications]
    end
    
    subgraph "Backend Services"
        M[Authentication]
        N[Wallet Management]
        O[Market Data API]
        P[Transaction Processing]
    end
    
    subgraph "AI Capabilities"
        Q[Natural Language Processing]
        R[Blockchain Operations]
        S[Smart Routing]
        T[Risk Assessment]
    end
```

### 🤖 [AI Agent Core](./aptos-agent/)
- **LangGraph.js-powered** conversational AI with ReAct pattern
- **7 specialized tools** for comprehensive blockchain operations
- **Advanced subgraph workflows** for complex multi-step transactions
- **Multi-network support** (Mainnet, Testnet, Devnet)
- **Context-aware responses** with transaction history understanding

### 🎨 [Frontend Application](./aptos-agent-fe/)
- **Next.js 14** React application with modern UI/UX
- **Multi-wallet integration** supporting major Aptos wallets
- **Real-time chat interface** with streaming responses
- **Interactive portfolio management** and transaction visualization
- **Mobile-responsive design** for seamless cross-device experience

### ⚙️ [Backend API](./aptos-ai-agent-be/)
- **NestJS** microservices architecture with PostgreSQL
- **Multi-provider authentication** (Wallet, OAuth, JWT)
- **Encrypted wallet management** with secure key storage
- **Real-time market data** integration and DEX routing
- **Comprehensive API documentation** with Swagger/OpenAPI

## ✨ Key Features

### 🗣️ Conversational DeFi
- **Smart Contract Interaction**: Execute token swaps, transfers, and DeFi operations through chat
- **Portfolio Management**: Check balances, track performance, and analyze holdings via natural language
- **Market Intelligence**: Get real-time market data, price alerts, and trading insights
- **Transaction Planning**: Interactive confirmations with gas estimation and risk assessment

### 🔐 Advanced Security
- **Multi-Wallet Support**: Connect Petra, Pontem, Martian, and other Aptos wallets
- **Encrypted Storage**: Military-grade encryption for private key and sensitive data protection
- **Transaction Verification**: Multi-layer validation before executing any blockchain operation
- **Session Management**: Secure JWT-based authentication with automatic session refresh

### 📊 Professional Trading Tools
- **DEX Aggregation**: Integration with PancakeSwap, Cellana, Hyperion, and other major DEXs
- **Smart Order Routing**: Automatic route optimization for best prices and minimal slippage
- **Gas Optimization**: Real-time gas estimation with cost optimization strategies
- **MEV Protection**: Advanced protection against frontrunning and sandwich attacks

### 💼 Portfolio & Analytics
- **Real-Time Tracking**: Live asset tracking across all supported tokens and protocols
- **Transaction History**: Detailed analytics with categorization and performance metrics
- **P&L Analysis**: Comprehensive profit/loss tracking with tax reporting features
- **Market Insights**: Advanced charting and trend analysis with AI-powered recommendations

## 🛠️ Technology Stack

### Core Technologies
- **AI Framework**: LangGraph.js, LangChain, GPT-4/Claude Sonnet
- **Frontend**: Next.js 14, React 19, Tailwind CSS, TypeScript
- **Backend**: NestJS, PostgreSQL, Prisma ORM, Redis
- **Blockchain**: Aptos Labs SDK, TypeScript SDK, Multi-wallet adapters

### Infrastructure & DevOps
- **Authentication**: JWT, OAuth2, Passport.js, Wallet signature verification
- **Database**: PostgreSQL with Prisma ORM, Redis for caching
- **Deployment**: Docker containers, Kubernetes orchestration
- **Monitoring**: Comprehensive logging, error tracking, and performance monitoring

### External Integrations
- **Market Data**: CoinGecko, CoinMarketCap APIs
- **DEX Protocols**: PancakeSwap, Cellana, Hyperion DEX integration
- **Wallet Providers**: Petra, Pontem, Martian, and other Aptos wallets

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ (recommended: 20+)
- PostgreSQL 14+ 
- Yarn or pnpm package manager
- Aptos CLI (optional, for advanced development)

### 1. Clone Repository
```bash
git clone https://github.com/HakifAI/hakifAI-hackathon.git
cd hakifAI-hackathon
```

### 2. Setup Backend Service
```bash
cd aptos-ai-agent-be
yarn install

# Copy and configure environment
cp .env.example .env
# Edit .env with your database and API credentials

# Initialize database
yarn db:generate
yarn db:migrate
yarn db:seed

# Start backend service
yarn start:dev
```

### 3. Setup AI Agent
```bash
cd ../aptos-agent
yarn install

# Configure environment
cp .env.example .env
# Add your AI API keys (Anthropic/OpenAI)

# Start AI agent (choose one method)
langgraph studio  # Recommended: Opens LangGraph Studio
# OR
yarn dev          # Alternative: Direct development mode
```

### 4. Setup Frontend Application
```bash
cd ../aptos-agent-fe
yarn install

# Configure environment
cp .env.example .env
# Set API endpoints and network configuration

# Start frontend
yarn dev
```

### 5. Access Your Application
- **Frontend Interface**: http://localhost:3000
- **Backend API**: http://localhost:3001
- **API Documentation**: http://localhost:3001/api/docs
- **LangGraph Studio**: http://localhost:2024

## 📋 Environment Configuration

### Backend Configuration (aptos-ai-agent-be/.env)
```env
# Database Configuration
DATABASE_URL="postgresql://username:password@localhost:5432/aptos_agent"

# Security
JWT_SECRET="your-super-secret-jwt-key-min-32-chars"
ENCRYPTION_KEY="your-encryption-key-for-wallet-data"

# Aptos Network
APTOS_NETWORK="testnet"  # or "mainnet", "devnet"
APTOS_RPC_URL="https://api.testnet.aptoslabs.com/v1"

# OAuth Providers
GOOGLE_CLIENT_ID="your-google-oauth-client-id"
GOOGLE_CLIENT_SECRET="your-google-oauth-client-secret"
TWITTER_CLIENT_ID="your-twitter-oauth-client-id"
TWITTER_CLIENT_SECRET="your-twitter-oauth-client-secret"

# External APIs
COINMARKETCAP_API_KEY="your-coinmarketcap-api-key"
COINGECKO_API_KEY="your-coingecko-api-key"
```

### AI Agent Configuration (aptos-agent/.env)
```env
# AI Model APIs (choose one or both)
ANTHROPIC_API_KEY="your-anthropic-claude-api-key"
OPENAI_API_KEY="your-openai-gpt-api-key"

# Aptos Configuration
APTOS_NETWORK="testnet"
APTOS_RPC_URL="https://api.testnet.aptoslabs.com/v1"

# Database
MONGODB_URI="mongodb://localhost:27017/aptos-agent"

# Security
JWT_SECRET="same-as-backend-jwt-secret"

# Optional: External APIs
TAVILY_API_KEY="your-tavily-search-api-key"
```

### Frontend Configuration (aptos-agent-fe/.env)
```env
# API Endpoints
NEXT_PUBLIC_API_URL="http://localhost:3001"
NEXT_PUBLIC_LANGGRAPH_API_URL="http://localhost:2024"

# Aptos Network
NEXT_PUBLIC_APTOS_NETWORK="testnet"
NEXT_PUBLIC_APTOS_RPC_URL="https://api.testnet.aptoslabs.com/v1"

# Authentication
NEXT_PUBLIC_JWT_SECRET="same-as-backend-jwt-secret"

# Optional: Analytics and Monitoring
NEXT_PUBLIC_ANALYTICS_ID="your-analytics-tracking-id"
```

## 🔧 Advanced Configuration

### Supported AI Models
The agent supports multiple language models with different capabilities:

#### Anthropic Claude (Recommended)
- **Claude-3.5-Sonnet**: Best balance of performance and cost
- **Claude-3-Haiku**: Fastest responses, lower cost
- **Claude-3-Opus**: Highest capability for complex operations

#### OpenAI GPT
- **GPT-4o**: Latest model with vision capabilities
- **GPT-4-Turbo**: High performance for complex reasoning
- **GPT-3.5-Turbo**: Cost-effective for simple operations

### Network Configuration
```typescript
// Custom network configuration
export const NETWORK_CONFIG = {
  mainnet: {
    rpcUrl: "https://api.mainnet.aptoslabs.com/v1",
    explorerUrl: "https://explorer.aptoslabs.com",
    chainId: 1
  },
  testnet: {
    rpcUrl: "https://api.testnet.aptoslabs.com/v1", 
    explorerUrl: "https://explorer.aptoslabs.com",
    chainId: 2
  },
  devnet: {
    rpcUrl: "https://api.devnet.aptoslabs.com/v1",
    explorerUrl: "https://explorer.aptoslabs.com",
    chainId: 32
  }
};
```

## 📚 Documentation

### Core Documentation
- 📖 [AI Agent Documentation](./aptos-agent/README.md) - Detailed agent architecture and tools
- 🎨 [Frontend Documentation](./aptos-agent-fe/README.md) - UI components and user interface guide
- ⚙️ [Backend Documentation](./aptos-ai-agent-be/README.md) - API endpoints and service architecture

### API Documentation
- 🔧 [Interactive API Docs](http://localhost:3001/api/docs) - Swagger/OpenAPI documentation (when running)
- 📋 [Authentication Guide](./docs/authentication.md) - OAuth and wallet authentication flows
- 🔐 [Security Best Practices](./docs/security.md) - Security implementation guide

### Development Guides
- 🛠️ [Development Setup](./docs/development.md) - Detailed development environment setup
- 🧪 [Testing Guide](./docs/testing.md) - Testing strategies and best practices
- 🚀 [Deployment Guide](./docs/deployment.md) - Production deployment instructions

## 🧪 Development & Testing

### Running Comprehensive Tests
```bash
# Backend unit and integration tests
cd aptos-ai-agent-be
yarn test              # Unit tests
yarn test:e2e          # End-to-end tests
yarn test:cov          # Coverage report

# AI Agent tests
cd ../aptos-agent
yarn test              # Tool and workflow tests
yarn test:int          # Integration tests

# Frontend tests
cd ../aptos-agent-fe
yarn test              # Component tests
yarn test:e2e          # End-to-end tests
```

### Development Tools
```bash
# Code quality
yarn lint              # ESLint checking
yarn lint:fix          # Auto-fix linting issues
yarn format            # Prettier formatting
yarn type-check        # TypeScript checking

# Database management
yarn db:studio         # Open Prisma Studio
yarn db:reset          # Reset database
yarn db:seed           # Seed test data
```

### Docker Development
```bash
# Full stack with Docker Compose
docker-compose up --build

# Individual service containers
docker build -t hakifai-frontend ./aptos-agent-fe
docker build -t hakifai-backend ./aptos-ai-agent-be
docker build -t hakifai-agent ./aptos-agent

# Production deployment
docker-compose -f docker-compose.prod.yml up -d
```

## 🚀 Production Deployment

### Environment Setup
1. **Database**: PostgreSQL 14+ with connection pooling
2. **Redis**: For session storage and caching
3. **Load Balancer**: Nginx or similar for traffic distribution
4. **SSL/TLS**: Certificates for secure connections
5. **Environment Variables**: Secure storage for API keys and secrets

### Deployment Checklist
- [ ] Database migrations completed
- [ ] Environment variables configured
- [ ] SSL certificates installed
- [ ] Load balancer configured
- [ ] Monitoring and logging setup
- [ ] Backup systems in place
- [ ] Security scanning completed

## 🤝 Contributing

We welcome contributions from the community! Here's how to get started:

### Getting Started
1. **Fork the repository** on GitHub
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Make your changes** following our coding standards
4. **Add tests** for new functionality
5. **Commit your changes**: `git commit -m 'Add amazing feature'`
6. **Push to your branch**: `git push origin feature/amazing-feature`
7. **Open a Pull Request** with a clear description

### Development Guidelines
- **TypeScript First**: All code should be properly typed
- **Test Coverage**: Maintain >80% test coverage for new features
- **Documentation**: Update relevant documentation for changes
- **Code Style**: Follow ESLint and Prettier configurations
- **Commit Messages**: Use conventional commits format

### Code Review Process
1. All changes require review from at least one maintainer
2. Automated tests must pass before merging
3. Security-sensitive changes require additional review
4. Breaking changes require version bump and migration guide

## 🔐 Security & Privacy

### Security Measures
- **Encryption at Rest**: All sensitive data encrypted using AES-256
- **Transport Security**: TLS 1.3 for all communications
- **Input Validation**: Comprehensive validation using Zod schemas  
- **Rate Limiting**: DDoS protection and API abuse prevention
- **Audit Logging**: Comprehensive logging of all security-relevant events

### Privacy Protection
- **Data Minimization**: Only collect necessary user data
- **Consent Management**: Clear opt-in for data collection
- **Right to Deletion**: Users can request complete data removal
- **Anonymization**: Personal data anonymized in analytics

### Wallet Security
- **Non-Custodial**: Private keys never leave user's device
- **Secure Storage**: Hardware wallet support for enhanced security
- **Transaction Verification**: Multi-step verification for all transactions
- **Session Management**: Automatic session expiration and cleanup

## 📊 Performance & Monitoring

### Performance Optimization
- **Caching Strategy**: Multi-layer caching for optimal performance
- **Database Optimization**: Query optimization and connection pooling
- **CDN Integration**: Static asset delivery optimization
- **Code Splitting**: Lazy loading for faster initial page loads

### Monitoring & Analytics
- **Real-time Monitoring**: Server health and performance metrics
- **Error Tracking**: Comprehensive error logging and alerting
- **User Analytics**: Privacy-compliant usage analytics
- **Transaction Monitoring**: Blockchain operation success rates

## 🆘 Support & Community

### Getting Help
- 🐛 **[Report Issues](https://github.com/HakifAI/hakifAI-hackathon/issues)** - Bug reports and feature requests
- 💬 **[Discord Community](https://discord.gg/hakifai)** - Real-time community support
- 📧 **[Email Support](mailto:support@hakifi.xyz)** - Direct technical support
- 📖 **[Documentation](./docs/)** - Comprehensive guides and tutorials

### Community Resources
- 🌐 **[Official Website](https://hakifi.xyz)** - Project information and updates
- 📱 **[Twitter](https://twitter.com/HakifAI)** - Latest news and announcements
- 💼 **[LinkedIn](https://linkedin.com/company/hakifai)** - Professional updates
- 📺 **[YouTube](https://youtube.com/@hakifai)** - Tutorials and demos

### External Resources
- 📖 [Aptos Developer Documentation](https://aptos.dev/)
- 💬 [Aptos Discord Community](https://discord.gg/aptoslabs)
- 🛠️ [LangGraph Documentation](https://langchain-ai.github.io/langgraphjs/)
- 🔧 [Next.js Documentation](https://nextjs.org/docs)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Third-Party Licenses
- LangGraph.js: MIT License
- Aptos TypeScript SDK: Apache 2.0
- Next.js: MIT License
- NestJS: MIT License

## 🏆 Acknowledgments

### Built With Love By
Special thanks to the HakifAI team and the broader Aptos community for their support and contributions.

### Team
- **AI/ML Engineers**: Conversational AI and LangGraph development
- **Blockchain Developers**: Aptos integration and smart contract interaction
- **Frontend Engineers**: React/Next.js user interface development  
- **Backend Engineers**: NestJS API and database architecture
- **DevOps Engineers**: Infrastructure and deployment automation

### Special Thanks
- **Aptos Labs**: For the incredible blockchain infrastructure
- **LangChain Team**: For the powerful AI agent framework
- **Open Source Community**: For the tools and libraries that made this possible

---

<div align="center">
  <strong>🚀 Revolutionizing DeFi through Conversational AI 🚀</strong><br>
  <em>Making blockchain accessible to everyone, one conversation at a time</em><br><br>
  
  **⭐ Star this repo if you find it useful! ⭐**
</div> 

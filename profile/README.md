# HakifAI Aptos AI Agent

<div align="center">
  <img src="https://github.com/HakifAI/aptos-agent-fe/blob/5939aea4fc3436144f17b1bdd09e5438cc05670e/public/logo.svg" alt="HakifAI Logo" width="250"/>
  
  **Conversational AI interface for Aptos blockchain. Execute DeFi operations, manage wallets, and trade tokens through natural language chat.**
  
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
  [![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
  [![Next.js](https://img.shields.io/badge/Next.js-000000?logo=next.js&logoColor=white)](https://nextjs.org/)
  [![NestJS](https://img.shields.io/badge/NestJS-E0234E?logo=nestjs&logoColor=white)](https://nestjs.com/)
  [![Aptos](https://img.shields.io/badge/Aptos-000000?logo=aptos&logoColor=white)](https://aptos.dev/)
</div>

## 🚀 Overview

HakifAI Aptos AI Agent is a sophisticated hackathon project that revolutionizes blockchain interaction through conversational AI. Built for the Aptos ecosystem, it enables users to perform complex DeFi operations, manage digital assets, and execute transactions using natural language commands.

The project demonstrates cutting-edge integration of AI agents with blockchain technology, providing an intuitive interface that makes DeFi accessible to users of all technical backgrounds.

## 🏗️ Architecture

The project consists of three integrated components:

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
    end
    
    subgraph "Backend Services"
        L[Authentication]
        M[Wallet Management]
        N[Market Data]
    end
    
    subgraph "AI Capabilities"
        O[Natural Language Processing]
        P[Blockchain Operations]
        Q[Smart Routing]
    end
```

### 🤖 [AI Agent Core](./aptos-agent/)
- **LangGraph.js-powered** conversational AI with ReAct pattern
- **7 specialized tools** for comprehensive blockchain operations
- **Advanced subgraph workflows** for complex multi-step transactions
- **Multi-network support** (Mainnet, Testnet, Devnet)

### 🎨 [Frontend Application](./aptos-agent-fe/)
- **Next.js 14** React application with modern UI/UX
- **Multi-wallet integration** supporting major Aptos wallets
- **Real-time chat interface** with streaming responses
- **Interactive portfolio management** and transaction visualization

### ⚙️ [Backend API](./aptos-ai-agent-be/)
- **NestJS** microservices architecture with PostgreSQL
- **Multi-provider authentication** (Wallet, OAuth, JWT)
- **Encrypted wallet management** with secure key storage
- **Real-time market data** integration and DEX routing

## ✨ Key Features

### 🗣️ Conversational DeFi
- Execute token swaps through natural language
- Check balances and portfolio performance via chat
- Get real-time market data and analytics
- Transfer tokens with interactive confirmations

### 🔐 Secure Wallet Management
- Connect multiple Aptos-compatible wallets
- Encrypted private key storage and management
- Multi-signature transaction support
- Secure authentication with wallet signatures

### 📊 Advanced Trading
- Integration with major DEXs (PancakeSwap, Cellana, Hyperion)
- Smart routing for optimal trade execution
- Real-time gas estimation and cost optimization
- Slippage protection and MEV resistance

### 💼 Portfolio Analytics
- Comprehensive asset tracking across tokens
- Transaction history with detailed analytics
- Performance metrics and profit/loss tracking
- Market insights and trend analysis

## 🛠️ Technology Stack

- **AI Framework**: LangGraph.js, LangChain, GPT-4/Claude
- **Frontend**: Next.js 14, React 19, Tailwind CSS, TypeScript
- **Backend**: NestJS, PostgreSQL, Prisma ORM, Redis
- **Blockchain**: Aptos Labs SDK, TypeScript SDK
- **Authentication**: JWT, OAuth2, Passport.js
- **Infrastructure**: Docker, Kubernetes, CI/CD

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- PostgreSQL 14+
- Yarn or pnpm
- Aptos CLI (optional)

### 1. Clone Repository
```bash
git clone <repository-url>
cd hakifAI-hackathon
```

### 2. Setup Backend
```bash
cd aptos-ai-agent-be
yarn install
cp .env.example .env
# Configure your environment variables
yarn db:migrate
yarn db:seed
yarn start:dev
```

### 3. Setup AI Agent
```bash
cd ../aptos-agent
yarn install
cp .env.example .env
# Configure your API keys
langgraph studio  # or yarn dev
```

### 4. Setup Frontend
```bash
cd ../aptos-agent-fe
yarn install
cp .env.example .env
# Configure your environment variables
yarn dev
```

### 5. Access Application
- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:3001
- **AI Agent Studio**: http://localhost:2024

## 📋 Environment Configuration

### Required Environment Variables

#### Backend (.env)
```env
DATABASE_URL="postgresql://username:password@localhost:5432/aptos_agent"
JWT_SECRET="your-super-secret-jwt-key"
APTOS_NETWORK="testnet"
GOOGLE_CLIENT_ID="your-google-client-id"
GOOGLE_CLIENT_SECRET="your-google-client-secret"
```

#### AI Agent (.env)
```env
ANTHROPIC_API_KEY="your-anthropic-key"
APTOS_NETWORK="testnet"
MONGODB_URI="mongodb://localhost:27017/aptos-agent"
JWT_SECRET="your-jwt-secret"
```

#### Frontend (.env)
```env
NEXT_PUBLIC_API_URL="http://localhost:3001"
NEXT_PUBLIC_APTOS_NETWORK="testnet"
NEXT_PUBLIC_JWT_SECRET="your-jwt-secret"
```

## 📚 Documentation

- 📖 [AI Agent Documentation](../aptos-agent/README.md)
- 🎨 [Frontend Documentation](../aptos-agent-fe/README.md)
- ⚙️ [Backend Documentation](../aptos-agent-be/README.md)
- 🔧 [API Documentation](http://localhost:3001/api/docs) (when running)

## 🧪 Development

### Running Tests
```bash
# Backend tests
cd aptos-ai-agent-be && yarn test

# AI Agent tests
cd aptos-agent && yarn test

# Frontend tests
cd aptos-agent-fe && yarn test
```

### Docker Deployment
```bash
# Build all services
docker-compose up --build

# Or individual services
docker build -t hakifai-frontend ./aptos-agent-fe
docker build -t hakifai-backend ./aptos-ai-agent-be
```

## 🤝 Contributing

We welcome contributions! Please see our contributing guidelines:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Development Guidelines
- Follow TypeScript best practices
- Write comprehensive tests for new features
- Update documentation for API changes
- Use conventional commits for clear history

## 🔐 Security

- All private keys are encrypted at rest
- Multi-layer authentication and authorization
- Input validation and sanitization
- Rate limiting and DDoS protection
- Regular security audits and updates

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support & Resources

- 📖 [Aptos Documentation](https://aptos.dev/)
- 💬 [Aptos Discord](https://discord.gg/aptoslabs)
- 🐛 [Report Issues](https://github.com/your-org/hakifAI-hackathon/issues)
- 📧 [Contact Team](mailto:team@hakifai.com)

## 🏆 Hackathon Credits

Built with ❤️ for the Aptos Hackathon by the HakifAI team.

### Team Members
- AI Engineer
- Blockchain Developer  
- Frontend Developer
- Backend Developer

---

<div align="center">
  <strong>Revolutionizing DeFi through Conversational AI</strong><br>
  <em>Making blockchain accessible to everyone</em>
</div> 

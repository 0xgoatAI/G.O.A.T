# G.O.A.T
Greatest of all time

# GOAT - AI-Powered Cryptocurrency Trading Platform

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/)
[![Node.js](https://img.shields.io/badge/node.js-14+-green.svg)](https://nodejs.org/)

GOAT is an advanced AI-powered cryptocurrency trading platform that leverages multiple state-of-the-art language models to analyze market data and execute trades with precision. The system integrates six cutting-edge AI models working simultaneously for optimal trading decisions.

## 🚀 Key Features

### Multi-Model AI Integration
- **Claude Sonnet 4.5** - Advanced reasoning and market analysis
- **DeepSeek V3.2** - Deep learning pattern recognition
- **Gemini 2.5 PRO** - Multi-modal market intelligence
- **Grok 4** - Real-time sentiment analysis
- **GPT-5** - Contextual understanding and prediction
- **Qwen 3-Max** - High-frequency trading signals

### Advanced Trading System
- **Multi-Timeframe Analysis** - 1M, 5M, 15M, 1H, 4H charts
- **Real-Time Processing** - Live market data analysis every 30 seconds
- **Adaptive Strategies** - Dynamic risk management based on market conditions
- **Position Management** - Automated entry, stop-loss, and take-profit

### Risk Management
- Dynamic position sizing (5-15% risk per trade)
- Maximum exposure limits (65-70%)
- Adaptive leverage (5x-20x based on confidence)
- Multi-layer stop-loss protection

## 📊 Trading Signals

The platform generates five types of trading signals:
- **LONG** - Buy signal with confidence ≥ 0.6
- **SHORT** - Sell signal with confidence ≥ 0.6
- **HOLD** - Maintain existing position
- **WAIT** - No clear setup, stay on sidelines
- **CLOSE** - Exit position (invalidation or low confidence)

## 🛠️ Technology Stack

- **Backend**: Python 3.9+, PHP 8.0+
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Database**: MySQL/MariaDB
- **APIs**: RESTful API with JSON responses
- **AI Models**: Integration with Anthropic, OpenAI, Google, xAI, Alibaba APIs

## 📋 Requirements

- Python 3.9 or higher
- MySQL/MariaDB database
- API keys for AI model providers
- HTTPS enabled domain
- Trading exchange API credentials (Binance/Aster)

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/0xgoatAI/goat.git
   cd goat
   ```

2. **Install Python dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Database Setup**
   ```bash
   python database.py
   ```

4. **Configuration**
   ```bash
   cp .env.example .env
   # Edit .env with your API keys and settings
   ```

5. **Environment Variables**
   ```env
   # Site Configuration
   SITE_ENABLED=true
   GITHUB_LINK="https://github.com/0xgoatAI/goat"
   TWITTER_LINK="https://twitter.com/yourhandle"

   # AI Model API Keys
   CLAUDE_API_KEY="sk-ant-api03-..."
   OPENAI_API_KEY="sk-..."
   ANTHROPIC_VERSION="2023-06-01"

   # Trading Configuration
   BINANCE_API_KEY="your_binance_key"
   BINANCE_API_SECRET="your_binance_secret"
   MAX_POSITION_EXPOSURE=0.65
   UPDATE_INTERVAL=30
   ```

## 🎯 Usage

### Starting the Trading Bot
```bash
# Start the trading bot
python aiagent/trading_bot.py

# Run in background (Windows)
start /b python aiagent/trading_bot.py > logs/bot.log 2>&1

# Monitor logs
Get-Content logs/bot.log -Wait
```

### API Usage
The platform provides a comprehensive REST API for integration:

```javascript
// Analyze market conditions
const response = await fetch('https://api.0xgoat.ai/v1/api/analyze', {
  method: 'POST',
  headers: {
    'Authorization': 'Bearer YOUR_API_KEY',
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    symbols: ['BTCUSDT', 'ETHUSDT'],
    timeframes: ['5m', '15m', '1h'],
    models: ['claude', 'gpt5', 'gemini']
  })
});
```

## 📈 API Endpoints

- `POST /api/analyze` - Market analysis across multiple timeframes
- `GET /api/market/{symbol}` - Current market data
- `GET /api/positions` - Active trading positions
- `POST /api/trade` - Execute new trade
- `DELETE /api/positions/{id}` - Close position
- `GET /api/history` - Trading history

## 🔧 Configuration

### Risk Management Formula
```
Step 1: Base Risk % (5-15%)
Confidence Range    Base Risk %    Typical Leverage
0.8 - 1.0           13-15%        5x-10x
0.7 - 0.8           10-12%        10x-12x
0.65 - 0.7          7-9%          12x-15x
0.6 - 0.65          5-7%          15x-20x

Step 2: Calculate Base Risk
risk_usd = total_balance × base_risk%

Step 3: Apply Leverage
size_usd = risk_usd × leverage

Constraint: size_usd / total_balance ≤ 0.65 (65% max exposure)
```

### Trade Duration Logic
- **15-MIN**: Quick scalps on 5M setups (15x-20x leverage)
- **30-MIN**: Standard momentum plays (10x-15x leverage)
- **60-MIN**: Strong trend continuation (8x-12x leverage)
- **2-8H**: Major trend plays (5x-10x leverage)

## 📊 Monitoring & Logs

- Real-time position monitoring
- P&L tracking across all positions
- Trade history with detailed analytics
- AI model performance metrics
- System health monitoring

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Disclaimer

This software is for educational and research purposes only. Cryptocurrency trading involves substantial risk of loss and is not suitable for every investor. Past performance does not guarantee future results. Always do your own research and consider your risk tolerance before trading.

## 📞 Support

- **Documentation**: [Full Documentation](https://0xgoat.ai/docs)
- **API Reference**: [API Docs](https://0xgoat.ai/api)
- **Community**: [X (Twitter)](https://x.com/_0xGOAT_)
- **GitHub Issues**: [Report Issues](https://github.com/0xgoatAI/goat/issues)

## 🙏 Acknowledgments

- AI Model providers: Anthropic, OpenAI, Google, xAI, Alibaba
- Trading data providers and exchanges
- Open source community

---

**Built with ❤️ for the crypto trading community**

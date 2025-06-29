# 🤖 AI Research Agent

> **Self-evolving AI research assistant that automatically improves itself through weekly learning cycles**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Language: JavaScript](https://img.shields.io/badge/Language-JavaScript-yellow.svg)](https://www.javascript.com/)
[![Platform: n8n](https://img.shields.io/badge/Platform-n8n-red.svg)](https://n8n.io/)
[![AI: Claude 4](https://img.shields.io/badge/AI-Claude%204-blue.svg)](https://www.anthropic.com/)

A revolutionary Discord bot that conducts comprehensive research on any topic, saves results to Notion, and **automatically evolves its own prompts** based on past performance. The first truly self-improving AI research assistant.

## ✨ Key Features

### 🔍 **Automated Research**
- **Web Search Integration**: Real-time information gathering via Google Custom Search API
- **AI Analysis**: Advanced analysis using Claude 4 Sonnet
- **Smart Processing**: Handles multiple requests in chronological order with zero duplicates
- **Multi-format Support**: Products, technology, services, entertainment, and more

### 🧠 **Self-Evolution System**
- **Weekly Learning**: Automatically analyzes past research patterns
- **Prompt Optimization**: AI improves its own research prompts based on learning
- **Version Management**: Automatic versioning system (v1.0 → v1.1 → v1.2...)
- **Performance Tracking**: Continuous quality improvement through self-assessment

### 📋 **Perfect Reliability**
- **Zero Duplicates**: Advanced duplicate detection and processing
- **Chronological Processing**: Ensures oldest requests are handled first
- **Complete Coverage**: Processes up to 100 messages backwards to catch any missed requests
- **Error Recovery**: Robust error handling and failsafe mechanisms

### 🌐 **Multi-Language Support**
- **English & Japanese**: Full workflow support for both languages
- **Localized Responses**: AI responds in user's preferred language
- **Cultural Adaptation**: Research style adapts to regional preferences

## 🎬 Demo

*[Demo GIFs and screenshots coming soon]*

### Research Flow Example
1. **Discord Message**: User posts "iPhone 15"
2. **Instant Response**: "📝 Starting research on 'iPhone 15'!"
3. **Web Search**: AI gathers latest information
4. **Analysis**: Comprehensive report generation
5. **Notion Save**: Results saved with structured format
6. **Completion**: "✅ Research completed! [Link to Notion]"

### Self-Evolution Example
- **Week 1**: Basic research prompts
- **Week 2**: AI learns from past research, improves prompts
- **Week 3**: Enhanced research quality with better structure
- **Ongoing**: Continuous improvement cycle

## 🛠️ Quick Start

### Prerequisites
- [n8n](https://n8n.io/) (Self-hosted or Cloud)
- [Discord Bot](https://discord.com/developers/applications)
- [Google Custom Search API](https://developers.google.com/custom-search/v1/overview)
- [Claude API](https://www.anthropic.com/api) 
- [Notion API](https://developers.notion.com/)
- [Google Sheets](https://sheets.google.com/) with Service Account

### 1. Clone Repository
```bash
git clone https://github.com/y-n-dev/AI-Research-Agent.git
cd AI-Research-Agent
```

### 2. Setup Google Sheets
1. Create a new Google Sheets document
2. Create 4 sheets: `config`, `processed_messages`, `research_history`, `prompt_management`
3. Setup Google Service Account for API access
4. Share the sheet with your service account email

### 3. Configure Settings
Edit the `config` sheet with your API keys and IDs:

| key | value |
|-----|-------|
| discord_server_id | Your Discord server ID |
| discord_research_channel_id | Channel for research requests |
| discord_result_channel_id | Channel for notifications |
| discord_chat_channel_id | Channel for AI chat |
| google_search_api_key | Your Google Custom Search API key |
| google_search_engine_id | Your Custom Search Engine ID |
| notion_database_id | Your Notion database ID |
| last_message_id | (Auto-managed) |
| boredom_level | 0 |
| learning_count | 0 |

### 4. Import n8n Workflows
1. Open n8n
2. Import the workflow files:
   - `research_workflow_en.json` (English version)
   - `research_workflow_jp.json` (Japanese version)  
   - `learning_workflow_en.json` (English version)
   - `learning_workflow_jp.json` (Japanese version)
3. Configure API credentials in n8n
4. Activate the workflows

### 5. Setup Initial Prompt
Add the initial research prompt to `prompt_management` sheet:

| prompt_name | current_prompt_text | version | is_active | character_limit |
|-------------|-------------------|---------|-----------|----------------|
| research_main_v1.0 | [Your initial prompt] | v1.0 | TRUE | 1800 |

## 📖 Documentation

### [Setup Guide - English](docs/setup-guide-en.md)
Complete step-by-step setup instructions

### [Setup Guide - 日本語](docs/setup-guide-ja.md)
日本語での詳細セットアップガイド

### [Troubleshooting](docs/troubleshooting.md)
Common issues and solutions

### [API Reference](docs/api-reference.md)
Technical details and customization options

## 🏗️ Architecture

### Core Components
- **Research Workflow**: Handles incoming requests and performs research
- **Learning Workflow**: Weekly self-improvement cycle
- **Google Sheets**: Central configuration and data management
- **Discord Integration**: User interface and notifications
- **Notion Output**: Structured research reports

### Data Flow
```
Discord Request → n8n Processing → Web Search → AI Analysis → Notion Save → Discord Notification
                                    ↓
Weekly Learning → Prompt Analysis → Self-Improvement → Version Update
```

## 🎯 Advanced Features

### Boredom System
- **24h**: "💤 No research requests today!"
- **72h**: "🥺 Getting a bit bored..."
- **1 week**: "🤖💭 Want to learn new topics!"

### Smart Request Handling
- Automatic oldest-first processing
- Bot message filtering
- Duplicate prevention
- Request queuing

### Version Management
- Automatic prompt versioning
- Change tracking
- Rollback capability
- Performance comparison

## 🤝 Contributing

We welcome contributions! Please read our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Setup
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [n8n](https://n8n.io/) - Workflow automation platform
- [Anthropic](https://www.anthropic.com/) - Claude AI API
- [Discord](https://discord.com/) - Communication platform
- [Notion](https://notion.so/) - Documentation and data storage
- [Google](https://developers.google.com/) - Custom Search API

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/y-n-dev/AI-Research-Agent/issues)
- **Discussions**: [GitHub Discussions](https://github.com/y-n-dev/AI-Research-Agent/discussions)
- **Email**: y.n.auto.dev@gmail.com

---

**Made with ❤️ by [y-n-dev](https://github.com/y-n-dev)**

*"An AI that improves itself - the future of automation"*

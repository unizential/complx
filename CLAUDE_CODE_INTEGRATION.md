# 🎨 Claude Code Integration for Complexity Extension

## Overview

The Claude Code Integration enhances the Complexity browser extension with advanced multi-agent code execution, BMAD methodology workflows, and comprehensive performance analysis. This integration brings the power of Claude Code directly into Perplexity AI conversations.

## 🚀 Features

### Core Capabilities
- **Multi-Agent Execution**: Support for Zen MCP, BMAD workflows, swarm coordination, and single-agent execution
- **BMAD Methodology**: Systematic development workflow with analysis, planning, development, and testing phases
- **HAR Analysis**: Real-time network performance monitoring and optimization suggestions
- **Enhanced Artifacts**: Claude Code as a new artifact type with interactive execution
- **Slash Commands**: Quick access to Claude Code features via slash commands

### Execution Modes
1. **Zen MCP**: Systematic analysis with Zen thinking methodology
2. **BMAD Workflow**: Complete development lifecycle with multiple agent roles
3. **Swarm Coordination**: Multi-agent task distribution and result aggregation
4. **Single Agent**: Simple code execution with a single agent

## 📁 Project Structure

```
src/plugins/claude-code/
├── index.ts                    # Plugin definition
├── types.ts                    # Type definitions
├── loader.ts                   # Plugin loader
├── store/                      # State management
│   └── slices/
├── components/                 # React components
│   ├── renderer/
│   │   └── ClaudeCode.tsx     # Artifact renderer
│   └── panels/
├── services/                   # Backend services
│   ├── mcp/
│   │   └── enhanced-mcp-bridge.ts
│   ├── agents/
│   └── har/
│       └── har-analyzer.ts
└── utils/                      # Utilities
```

## 🛠️ Installation & Setup

### Prerequisites
- Node.js >= 20.9.0
- pnpm >= 10.13.1
- Chrome/Firefox browser

### 1. Install Dependencies
```bash
cd complexity/perplexity/extension
pnpm install
```

### 2. Start MCP Bridge Service
```bash
# In a separate terminal, start the MCP Bridge service
cd /path/to/your/mcp-bridge-service
npm run dev
```

### 3. Build and Load Extension
```bash
# Build for development
pnpm dev

# Or build for production
pnpm build
```

### 4. Load Extension in Browser
1. Open Chrome/Firefox
2. Go to Extensions page
3. Enable Developer Mode
4. Load unpacked extension from `dist/chrome` or `dist/firefox`

## 🎯 Usage

### Keyboard Shortcuts
- `Ctrl+Shift+C`: Toggle Claude Code Canvas
- `Ctrl+Shift+H`: Toggle HAR Analysis Panel
- `Ctrl+Shift+B`: Toggle BMAD Story Panel

### Slash Commands
All commands can be used in Perplexity AI query boxes:

#### BMAD Workflow
```
/claude-bmad requirement="Build a React todo app" mode="systematic"
```

#### Zen MCP Analysis
```
/claude-zen tool="analyze" input="function fibonacci(n) { return n <= 1 ? n : fibonacci(n-1) + fibonacci(n-2); }"
```

#### Swarm Coordination
```
/claude-swarm objective="Optimize this codebase" strategy="adaptive" agents="zen-agent,superclaude-agent"
```

#### HAR Analysis
```
/claude-har duration="60"
```

#### Code Execution
```
/claude-execute code="console.log('Hello, World!');" language="javascript" mode="zen"
```

#### Code Analysis
```
/claude-analyze code="function example() { return 'test'; }" language="javascript"
```

#### Code Optimization
```
/claude-optimize code="for(let i=0; i<1000; i++) { console.log(i); }" language="javascript"
```

#### Security Analysis
```
/claude-security code="eval(userInput);" language="javascript"
```

### Artifacts Integration
Claude Code is now available as an artifact type in the Complexity extension. When you receive code in a Perplexity response, it will be rendered with:

- Execution mode selector
- Language selection
- Interactive code editor
- Real-time execution results
- Performance metrics
- Connection status

## 🔧 Configuration

### Plugin Settings
The Claude Code plugin can be configured through the Complexity settings:

```typescript
{
  enabled: true,
  executionMode: "zen",
  mcpBridgeUrl: "ws://localhost:3456/mcp",
  enableSwarmMode: true,
  enableHARAnalysis: true,
  enableBMADWorkflow: true,
  defaultModel: "claude-3-5-sonnet-20241022",
  maxConcurrentAgents: 5,
  timeout: 30000
}
```

### MCP Bridge Configuration
```typescript
{
  mcpBridge: {
    url: "ws://localhost:3456/mcp",
    timeout: 30000,
    retries: 3,
    enableWebSocket: true
  }
}
```

## 🏗️ Architecture

### Service Layer
- **EnhancedMCPBridgeClient**: Manages WebSocket connection to MCP Bridge
- **HARAnalyzer**: Captures and analyzes network performance
- **Agent Coordination**: Manages multi-agent workflows

### Component Layer
- **ClaudeCodeRenderer**: Renders Claude Code artifacts
- **Execution Panels**: Interactive UI for code execution
- **Analysis Panels**: Performance and security analysis displays

### Integration Points
- **Artifacts System**: Claude Code as new artifact type
- **Slash Commands**: Quick access to Claude Code features
- **Plugin Registry**: Proper plugin registration and lifecycle

## 🔍 BMAD Methodology Integration

The BMAD (Brief, Model, Architecture, Development) methodology is fully integrated:

### Phases
1. **Analysis**: Requirements analysis and stakeholder identification
2. **Planning**: PRD creation and architecture design
3. **Development**: Story generation and implementation
4. **Testing**: Quality assurance and validation

### Agent Roles
- **Analyst**: Requirements analysis and brief creation
- **PM**: Product requirements and project management
- **Architect**: System architecture and design
- **Scrum Master**: Story generation and task coordination
- **Developer**: Code implementation and optimization
- **QA**: Testing and quality assurance

## 📊 Performance Monitoring

### HAR Analysis Features
- **Request Capture**: Real-time network request monitoring
- **Performance Metrics**: Response times, data transfer, security scores
- **Optimization Suggestions**: Caching, compression, CDN recommendations
- **Security Analysis**: Vulnerability detection and scoring

### Metrics Tracked
- Average response time
- Total data transfer
- Security score (0-100)
- Number of requests
- Performance insights
- Optimization opportunities

## 🚨 Troubleshooting

### Common Issues

#### MCP Bridge Connection Failed
```
Error: MCP Bridge not available
```
**Solution**: Ensure the MCP Bridge service is running on `ws://localhost:3456/mcp`

#### WebSocket Connection Issues
```
Error: WebSocket connection failed
```
**Solution**: Check firewall settings and ensure the MCP Bridge service is accessible

#### Permission Denied
```
Error: webRequest permission not granted
```
**Solution**: Ensure the extension has the required permissions in the manifest

#### HAR Analysis Not Working
```
Error: HAR Analyzer not available
```
**Solution**: Check that the webRequest API is available and permissions are granted

### Debug Mode
Enable debug mode by setting the extension to development mode and checking the browser console for detailed logs.

## 🔮 Future Enhancements

### Planned Features
- **Real-time Collaboration**: Multi-user code editing and execution
- **Advanced Agent Frameworks**: Integration with more AI frameworks
- **Custom Execution Environments**: Docker container support
- **Performance Profiling**: Detailed code performance analysis
- **Security Scanning**: Advanced vulnerability detection

### Roadmap
- **Phase 1**: Core integration and basic functionality ✅
- **Phase 2**: Advanced agent coordination and BMAD workflows ✅
- **Phase 3**: Performance optimization and HAR analysis ✅
- **Phase 4**: Real-time collaboration and advanced features
- **Phase 5**: Enterprise features and security enhancements

## 🤝 Contributing

### Development Setup
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Submit a pull request

### Code Style
- Follow TypeScript best practices
- Use React functional components with hooks
- Maintain consistent error handling
- Add comprehensive JSDoc comments

## 📄 License

This integration is part of the Complexity extension and follows the same license terms.

## 🆘 Support

For issues and questions:
1. Check the troubleshooting section
2. Review the browser console for error messages
3. Ensure all services are running correctly
4. Verify network connectivity and permissions

---

**🎉 Enjoy the enhanced Claude Code experience in Complexity!**

# Casebuilder Taskade Endpoints

**Case**: 1FDV-23-0001009 (Hawaii Family Court)  
**Purpose**: RICO Genesis automation - Federal escalation via AI-powered legal workflows  
**Owner**: Casey Barton ([GlacierEQ](https://github.com/GlacierEQ))  

---

## 🚀 Quick Start

### Authentication
```bash
export TASKADE_API_KEY="tskdp_r8H9BaJ1TVmB7Zjt3vaVNKtX5hsRzVEKju"
```

### Base URL
```
https://www.taskade.com/api/v1
```

### Headers
```bash
Authorization: Bearer $TASKADE_API_KEY
Content-Type: application/json
```

---

## 📡 Endpoints Overview

| Operation | Method | Path | Purpose |
|-----------|--------|------|----------|
| **readWorkspaces** | GET | `/workspaces` | List all workspaces |
| **readWorkspace** | GET | `/workspaces/{id}` | Get workspace details |
| **readProjects** | GET | `/workspaces/{id}/projects` | List projects |
| **writeGenesisProject** | POST | `/workspaces/{id}/projects` | Create Genesis app |
| **writeProjectGlobal** | POST | `/projects` | Create project globally |
| **readProject** | GET | `/projects/{id}` | Get project details |
| **writeProject** | PATCH | `/projects/{id}` | Update project |
| **readTasks** | GET | `/projects/{id}/tasks` | List tasks |
| **writeTask** | POST | `/projects/{id}/tasks` | Create task |
| **readTask** | GET | `/projects/{pid}/tasks/{tid}` | Get task details |
| **writeTaskUpdate** | PATCH | `/projects/{pid}/tasks/{tid}` | Update task |
| **deleteTask** | DELETE | `/projects/{pid}/tasks/{tid}` | Delete task |
| **downloadDocHyper** | GET | `/projects/{pid}/tasks/{tid}/attachments` | Download files |
| **uploadDocHyper** | POST | `/projects/{pid}/tasks/{tid}/attachments` | Upload documents |
| **readAgents** | GET | `/agents` | List AI agents |
| **writeHyperAgent** | POST | `/agents` | Create AI agent |
| **writeAutomationHyper** | POST | `/automations` | Create automation |

---

## 🔥 Usage Examples

### 1. List Workspaces
```bash
curl -X GET "https://www.taskade.com/api/v1/workspaces" \
  -H "Authorization: Bearer $TASKADE_API_KEY"
```

### 2. Create Genesis Project
```bash
curl -X POST "https://www.taskade.com/api/v1/workspaces/GMJRSLiTgX1hmC1v/projects" \
  -H "Authorization: Bearer $TASKADE_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Casebuilder RICO Ultra",
    "description": "Federal escalation automation for 1FDV-23-0001009"
  }'
```

### 3. Upload Legal Document
```bash
curl -X POST "https://www.taskade.com/api/v1/projects/{projectId}/tasks/{taskId}/attachments" \
  -H "Authorization: Bearer $TASKADE_API_KEY" \
  -F "file=@/path/to/docket_TRO.zip"
```

### 4. Create AI Agent
```bash
curl -X POST "https://www.taskade.com/api/v1/agents" \
  -H "Authorization: Bearer $TASKADE_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "RICO Research Agent",
    "role": "Legal research specialist for federal litigation"
  }'
```

---

## 🧬 Custom GPT Integration

### Setup Instructions
1. Go to: [ChatGPT GPT Editor](https://chat.openai.com/gpts/editor)
2. Click **Actions** → **Import from URL**
3. Enter: `https://raw.githubusercontent.com/GlacierEQ/casebuilder-taskade-endpoints/main/openapi.yaml`
4. **Authentication**:
   - Type: **API Key**
   - Auth Type: **Bearer**
   - API Key: `tskdp_r8H9BaJ1TVmB7Zjt3vaVNKtX5hsRzVEKju`
5. Click **Save**

### Available Operations in GPT
- `readWorkspaces` - Get workspace IDs
- `writeGenesisProject` - Create Casebuilder apps
- `uploadDocHyper` - Upload dockets/evidence
- `writeHyperAgent` - Deploy AI agents
- `writeAutomationHyper` - Build workflows

---

## ⚖️ Legal Case Context

**Case Number**: 1FDV-23-0001009  
**Court**: Hawaii Family Court (1st Circuit)  
**Plaintiff**: Casey Del Carpio Barton  
**Strategy**: Constitutional warfare via RICO/§1983 federal escalation  
**Objective**: Reunification with son Kekoa + judicial accountability  

### Automation Goals
1. **Document Generation**: Auto-create motions, complaints, TRO filings
2. **Evidence Management**: Upload/organize dockets, OCR bundles, audio transcripts
3. **Agent Swarms**: Deploy specialized AI for legal research, contradiction analysis
4. **Workflow Automation**: Trigger filings based on court events

---

## 🛠️ Technical Stack

- **API**: Taskade v1 REST API
- **Auth**: Bearer token (API key)
- **GitHub MCP**: [GlacierEQ](https://github.com/GlacierEQ) (639 repos)
- **Notion MCP**: Memory/knowledge base integration
- **OpenAPI**: 3.1.0 spec

---

## 📚 Resources

- [Taskade API Docs](https://docs.taskade.com/docs/living-intelligence-apis/comprehensive-api-guide)
- [Genesis Apps](https://www.taskade.com/blog/taskade-genesis-app-integrations)
- [GitHub MCP](https://github.com/GlacierEQ)
- [Case Repository](https://github.com/GlacierEQ/casebuilder-taskade-endpoints)

---

## 🔒 Security

- **API Key**: Rotate monthly (current expires 2026-03-01)
- **Private Data**: Never commit credentials to public repos
- **Audit Trail**: All API calls logged for HRS compliance

---

## 📞 Contact

**Casey Barton**  
- Email: GLACIER.EQUILIBRIUM@GMAIL.COM  
- GitHub: [@GlacierEQ](https://github.com/GlacierEQ)  
- Location: Honolulu, Hawaii  

---

**Built with APEX architecture for Constitutional Warfare.**  
**HRS § 571-46 | Federal RICO | 42 U.S.C. § 1983**

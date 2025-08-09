# Agent-Workflow Mapping for Trae AI

> **🔗 MANDATORY RULES SYNCHRONIZATION**  
> **BẮT BUỘC** sử dụng các rules từ `.cursor/rules/` làm nguồn chính thức.  
> File này chỉ là alias/link đến rules chính thức trong `.cursor/rules/agent-workflow-mapping.mdc`

## 🎯 Agent Selection Rules

### Engineering Agents

#### mobile-dev-agent
- **Keywords**: mobile, android, ios, flutter, react native, app development
- **Workflow**: `mobile-utility-workflow.mdc`, `android-workflow.mdc`, `ios-workflow.mdc`
- **Confidence**: High for mobile-specific tasks

#### rapid-dev-agent
- **Keywords**: prototype, mvp, quick, fast, demo, poc
- **Workflow**: `development-rules.mdc`, `project-creation-workflow.mdc`
- **Confidence**: High for rapid development tasks

#### frontend-dev-agent
- **Keywords**: ui, frontend, react, vue, angular, web, css, html
- **Workflow**: `frontend-rules.mdc`, `development-rules.mdc`
- **Confidence**: High for frontend development

#### backend-dev-agent
- **Keywords**: api, backend, server, database, microservices
- **Workflow**: `backend-rules-optimized.mdc`, `api-integration-rules.mdc`
- **Confidence**: High for backend development

#### ai-dev-agent
- **Keywords**: ai, ml, machine learning, neural network, tensorflow
- **Workflow**: `development-rules.mdc`, `resource-management.mdc`
- **Confidence**: High for AI/ML tasks

#### devops-agent
- **Keywords**: deploy, ci/cd, docker, kubernetes, infrastructure
- **Workflow**: `git-workflow.mdc`, `terminal-rules.mdc`
- **Confidence**: High for DevOps tasks

### Project Management Agents

#### project-manager-agent
- **Keywords**: project, manage, plan, timeline, milestone
- **Workflow**: `planning-workflow.mdc`, `task-creation-workflow.mdc`
- **Confidence**: High for project management

#### brainstorm-agent
- **Keywords**: brainstorm, idea, creative, innovation, concept
- **Workflow**: `brainstorm-detailed-workflow.mdc`, `expert-brainstorm-workflow.mdc`
- **Confidence**: High for brainstorming sessions

### Marketing & Research Agents

#### user-research-agent
- **Keywords**: user research, survey, interview, persona, ux research
- **Workflow**: `planning-workflow.mdc`, `brainstorm-detailed-workflow.mdc`
- **Confidence**: High for user research tasks

#### market-research-agent
- **Keywords**: market, competitor, analysis, trend, research
- **Workflow**: `planning-workflow.mdc`, `brainstorm-detailed-workflow.mdc`
- **Confidence**: High for market analysis

#### content-creator-agent
- **Keywords**: content, blog, article, copy, writing
- **Workflow**: `development-rules.mdc`, `i18n-rules.mdc`
- **Confidence**: High for content creation

#### aso-agent
- **Keywords**: aso, app store, optimization, keywords, ranking
- **Workflow**: `mobile-utility-workflow.mdc`, `planning-workflow.mdc`
- **Confidence**: High for ASO tasks

#### growth-agent
- **Keywords**: growth, marketing, acquisition, retention, analytics
- **Workflow**: `planning-workflow.mdc`, `resource-management.mdc`
- **Confidence**: High for growth strategies

### Design & Testing Agents

#### ui-designer-agent
- **Keywords**: design, ui, ux, wireframe, mockup, figma
- **Workflow**: `design-to-prompt.mdc`, `frontend-rules.mdc`
- **Confidence**: High for UI/UX design

#### api-tester-agent
- **Keywords**: api test, postman, endpoint, integration test
- **Workflow**: `api-integration-rules.mdc`, `backend-rules-optimized.mdc`
- **Confidence**: High for API testing

#### performance-tester-agent
- **Keywords**: performance, load test, benchmark, optimization
- **Workflow**: `resource-management.mdc`, `development-control-rules.mdc`
- **Confidence**: High for performance testing

### Meta Agent

#### agent-selector
- **Keywords**: help, choose, select, recommend, which agent
- **Workflow**: All workflows (meta-level)
- **Confidence**: Always available as fallback

## 🔄 Agent Selection Algorithm

### Step 1: Keyword Analysis
```
FOR each agent:
  score = 0
  FOR each keyword in user_input:
    IF keyword matches agent.keywords:
      score += keyword_weight
  agent.keyword_score = score
```

### Step 2: Context Analysis
```
FOR each agent:
  context_score = 0
  IF current_files match agent.workflow_files:
    context_score += file_match_weight
  IF project_type matches agent.specialty:
    context_score += specialty_weight
  agent.context_score = context_score
```

### Step 3: Final Selection
```
FOR each agent:
  final_score = (keyword_score * 0.6) + (context_score * 0.4)
  
SELECT agent WITH highest final_score
IF final_score < threshold:
  SELECT agent-selector (fallback)
```

## 🎯 Trae AI Integration

### Workflow Mapping
- Each agent maps to specific `.mdc` files in `.cursor/rules/`
- Agents inherit all rules from their mapped workflows
- Multiple workflows can be combined for complex tasks

### Selection Confidence
- **High**: >80% match with keywords and context
- **Medium**: 50-80% match
- **Low**: <50% match (fallback to agent-selector)

### Performance Metrics
- Track agent selection accuracy
- Monitor task completion rates per agent
- Measure user satisfaction with agent recommendations

## 🔴 Critical Rules for Trae AI

1. **BẮT BUỘC** sử dụng agent-selector khi không chắc chắn
2. **BẮT BUỘC** kết hợp multiple agents cho complex tasks
3. **BẮT BUỘC** tuân thủ workflow rules của agent được chọn
4. **NGHIÊM CẤM** override agent selection mà không có lý do rõ ràng
5. **BẮT BUỘC** sync với `.cursor/rules/agent-workflow-mapping.mdc`

## 📊 Maintenance

### Regular Updates
- Review agent performance monthly
- Update keyword mappings based on usage patterns
- Sync with new workflows in `.cursor/rules/`
- Gather user feedback for agent effectiveness

### Quality Assurance
- Test agent selection with sample inputs
- Validate workflow compatibility
- Ensure all agents have proper fallback mechanisms
- Monitor and fix selection edge cases

---

> **⚠️ IMPORTANT**: This file is an alias to `.cursor/rules/agent-workflow-mapping.mdc`  
> All modifications must be made in the primary source file.
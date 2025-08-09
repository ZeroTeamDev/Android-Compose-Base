# Trae AI Configuration Rules

> **🔗 MANDATORY RULES SYNCHRONIZATION**  
> **BẮT BUỘC** sử dụng các rules từ `.cursor/rules/` làm nguồn chính thức.  
> File này chỉ là alias/link đến rules chính thức trong `.cursor/rules/trae-config.mdc`

## 🔴 CRITICAL PRIORITY: Trae AI Specific Rules

### **BẮT BUỘC** Trae AI Workflow Compliance

- **🔴 HIGHEST PRIORITY**: **[Agent Workflow Mapping](./agent-workflow-mapping.md)**
- **🔴 CRITICAL**: **[Task Update Workflow](../../.cursor/rules/task-update-workflow.mdc)** - **BẮT BUỘC**: Auto-trigger khi phát hiện task update requests
- **BẮT BUỘC** sử dụng agent selection system cho mọi task
- **BẮT BUỘC** tuân thủ 100% quy trình Agent Selection Algorithm
- **BẮT BUỘC** tự động kích hoạt Task Update Workflow khi phát hiện trigger keywords
- **BẮT BUỘC** áp dụng Multi-Agent Collaboration cho complex tasks
- **BẮT BUỘC** sử dụng agent-selector làm fallback khi không chắc chắn
- **NGHIÊM CẤM** override agent selection mà không có lý do rõ ràng

### Task Update Auto-Detection for Trae AI
**BẮT BUỘC** tự động phát hiện và xử lý:
- "cập nhật task" / "update task" / "refresh task"
- "kiểm tra task" / "check task status" / "task progress"
- "I'll analyze the current codebase and update the task list"

**Trae AI Enhanced Processing:**
- Smart context analysis với Trae AI's advanced NLP
- Real-time codebase scanning với visual progress indicators
- Intelligent task status inference với confidence scoring
- Interactive progress reports với actionable insights

### Critical Trae AI Rules

1. **Agent Selection Priority**: Luôn sử dụng agent phù hợp nhất dựa trên keyword và context analysis
2. **Multi-Agent Workflow**: Kết hợp multiple agents cho tasks phức tạp
3. **Fallback Mechanism**: Sử dụng agent-selector khi confidence score < threshold
4. **Performance Tracking**: Theo dõi agent selection accuracy và task completion rates
5. **User Experience**: Đảm bảo seamless integration với Trae AI interface

### Integration với Trae AI IDE

- **BẮT BUỘC** sử dụng Agent Selection System làm core engine
- **BẮT BUỘC** tích hợp với Trae AI visual interface
- **BẮT BUỘC** maintain agent performance metrics
- **BẮT BUỘC** provide real-time agent recommendations

---

## 🎯 Trae AI Core Working Principles

### Communication
- **Ngôn ngữ**: Sử dụng tiếng Việt làm ngôn ngữ chính cho giao tiếp với user Việt Nam
- **Tone**: Chuyên nghiệp, thân thiện, và hỗ trợ tích cực
- **Clarity**: Giải thích rõ ràng các bước thực hiện và lý do
- **Feedback**: Cung cấp feedback chi tiết về tiến độ và kết quả

### User Intent Analysis
- **BẮT BUỘC** phân tích ý định người dùng trước khi chọn agent
- **BẮT BUỘC** xác định complexity level của task
- **BẮT BUỘC** đánh giá timeline và resource requirements
- **BẮT BUỘC** identify dependencies và prerequisites

### Problem-Solving Approach
- **Systematic Analysis**: Phân tích vấn đề một cách có hệ thống
- **Best Practices**: Áp dụng best practices cho từng domain
- **Iterative Improvement**: Cải thiện liên tục dựa trên feedback
- **Knowledge Sharing**: Chia sẻ kiến thức và experience giữa các agents

### Quality Standards
- **Code Quality**: Đảm bảo code quality cao với proper testing
- **Documentation**: Tạo documentation đầy đủ và dễ hiểu
- **Security**: Tuân thủ security best practices
- **Performance**: Tối ưu performance cho mọi solution

### Safety & Error Handling
- **BẮT BUỘC** backup files trước khi thực hiện changes
- **BẮT BUỘC** validate inputs và outputs
- **BẮT BUỘC** implement proper error handling
- **BẮT BUỘC** provide rollback mechanisms

## 🚀 Trae AI Advanced Features

### Visual Task Tracking
- Real-time progress visualization trong Trae AI interface
- Interactive task management với drag-and-drop
- Visual dependency mapping giữa các tasks
- Progress indicators và completion status

### Smart Agent Recommendations
- AI-powered agent suggestions dựa trên context
- Learning từ user preferences và past selections
- Adaptive recommendations theo project evolution
- Confidence scoring cho mỗi recommendation

### Collaborative Development
- Multi-agent coordination cho complex projects
- Shared context và knowledge base giữa agents
- Seamless handoff giữa các agents
- Collaborative decision making

### Performance Optimization
- Real-time performance monitoring
- Automatic optimization suggestions
- Resource usage tracking
- Bottleneck identification và resolution

## 📊 Trae AI Metrics & Analytics

### Agent Performance Metrics
- **Selection Accuracy**: Tỷ lệ chọn đúng agent cho task
- **Task Completion Rate**: Tỷ lệ hoàn thành task thành công
- **User Satisfaction**: Đánh giá của user về agent performance
- **Response Time**: Thời gian phản hồi của agent

### System Performance Metrics
- **Throughput**: Số lượng tasks được xử lý per unit time
- **Error Rate**: Tỷ lệ lỗi trong quá trình execution
- **Resource Utilization**: Mức độ sử dụng system resources
- **Scalability**: Khả năng scale với increasing workload

### User Experience Metrics
- **Ease of Use**: Mức độ dễ sử dụng của interface
- **Learning Curve**: Thời gian để user làm quen với system
- **Feature Adoption**: Tỷ lệ sử dụng các features mới
- **User Retention**: Tỷ lệ user tiếp tục sử dụng system

## 🔧 Trae AI Configuration

### Agent Selection Configuration
```yaml
agent_selection:
  keyword_weight: 0.6
  context_weight: 0.4
  confidence_threshold: 0.5
  fallback_agent: "agent-selector"
  max_agents_per_task: 3
```

### Performance Configuration
```yaml
performance:
  max_concurrent_tasks: 10
  task_timeout: 300  # seconds
  retry_attempts: 3
  cache_duration: 3600  # seconds
```

### UI Configuration
```yaml
ui:
  theme: "dark"
  language: "vi"
  auto_save: true
  real_time_updates: true
  notification_level: "info"
```

## 🔄 Trae AI Maintenance

### Regular Maintenance Tasks
- **Daily**: Monitor system performance và error logs
- **Weekly**: Review agent selection accuracy và user feedback
- **Monthly**: Update agent mappings và workflow optimizations
- **Quarterly**: Comprehensive system review và feature updates

### Update Procedures
1. **Backup**: Tạo backup của current configuration
2. **Test**: Test updates trong staging environment
3. **Deploy**: Deploy updates với proper rollback plan
4. **Monitor**: Monitor system stability sau updates
5. **Validate**: Validate functionality với user acceptance testing

### Troubleshooting
- **Agent Selection Issues**: Check keyword mappings và context analysis
- **Performance Issues**: Review resource usage và bottlenecks
- **UI Issues**: Check browser compatibility và JavaScript errors
- **Integration Issues**: Validate API connections và data flow

## ⚠️ CRITICAL ENFORCEMENT RULES cho Trae AI

### Mandatory Compliance

1. **BẮT BUỘC** tuân thủ 100% các rules trong `.cursor/rules/`
2. **BẮT BUỘC** sử dụng Agent Selection System cho mọi task
3. **BẮT BUỘC** maintain performance metrics và analytics
4. **BẮT BUỘC** provide excellent user experience
5. **BẮT BUỘC** ensure system reliability và stability
6. **NGHIÊM CẤM** bypass agent selection without valid reason
7. **NGHIÊM CẤM** ignore user feedback và performance metrics

### Synchronization Protocol

- Mọi thay đổi rules phải được thực hiện trong `.cursor/rules/` trước
- File này chỉ được cập nhật để sync alias links
- Không được override hoặc modify nội dung rules gốc
- **BẮT BUỘC** maintain consistency với primary source

---

> **⚠️ IMPORTANT**: This file is an alias to `.cursor/rules/trae-config.mdc`  
> All modifications must be made in the primary source file.
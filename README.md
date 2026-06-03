# agent_eval_lite
> Lightweight General task-execution Agent Evaluation Benchmark | 轻量化桌面智能体评测基准项目

## DESCRIPTION | 项目简介
The project is a **lightweight agent evaluation lite benchmark**, without any enterprise internal raw data, tasks or private resources.
Based on OSWorld public benchmark methodology and reshaped public resources tasks, the project aims to build **120 self-built simulated desktop tasks**.
It builds a complete implementable universal task-execution agent evaluation system adapted to hybrid automated and manual assessment for desktop-based Agents.

本项目为**合规自研Lite版Agent评测作品集**，无任何企业内部原始数据、内部任务与私有素材；
依托OSWorld公开基准方法论，融合公开资料改写任务，本项目计划构建 **120条全自建仿真桌面任务**，搭建完整可落地的通用任务执行型Agent评测体系，适配桌面端Agent自动化+人工混合测评。

**Resources of tasks**: `self built simulated tasks/ reshaped public task resources`. Comply with compliance specifications for independent dataset production throughout the entire process.

所有任务统一标注来源：`自建仿真任务 / 公开资料改写任务`，全程遵循独立数据集生产合规规范。

## Outputs | 项目核心产出
### 1. Evaluation Framework｜评测体系框架
- Capability classification framework for general Agent, covering desktop browsing, document editing, code debugging, terminal operation & cross-software collaboration
- Failure taxonomy of Agent, including positioning error, instruction misunderstanding & multi-step logic breakdown

- 通用Agent能力维度划分框架，覆盖桌面浏览、文档编辑、代码调试、终端操作、跨软件协同等能力项
- Agent失败模式分类Taxonomy，归纳操作定位错误、指令理解偏差、多步骤逻辑断裂等故障类目

### 2. Standard Rubric System｜标准化Rubric评分规范
- **6-dimensional quantified rubric** with 0~3 scoring rules & typical case samples for each score tier
- Unified scoring standard to reduce annotator discrepancy and support horizontal comparison among multiple Agents

- **6维度量化Rubric打分表**，配套0~3分锚点定义 + 各档位典型样例
- 统一人工打分口径，消除标注分歧，可直接用于Agent效果横向对比

### 3. Evaluation Dataset｜评测数据集（120条自建任务）
- Self-developed desktop task set with user prompt, environment config, pass criteria & reference answer for every case
- **Dual evaluation pipeline**: automatic file/content verification + fine-grained manual rubric scoring

- 全量自建桌面仿真任务集，每条包含：自然语言用户指令、初始环境素材、任务成功判定标准、标准答案
- 支持**自动校验+人工复核双链路评估**：自动化脚本做文件/内容校验，Rubric做人工细粒度打分

### 4. Data Production & QC Specification｜数据生产&质量管控规范
- Central task table to manage ID, category, difficulty, source tag and verification rules
- Standard SOP & QC checklist to regulate full-cycle development of custom evaluation tasks

- 任务数据总母表：统一管理任务ID、分类、难度、来源标注、校验规则
- 标准化任务生成SOP文档 + 质检Checklist，规范自建任务生产全流程质量管控

### 5. Supplementary Documents｜配套文档
Including dataset construction report, framework specification & project portfolio description

评测集建设报告书、评测体系说明书、项目作品集说明文档

## Compliance Rules｜合规说明
1. ❌ No internal annotated data, confidential screenshots, model outputs, private tools or client materials from any company
2. ❌ No reproduction of unreleased proprietary task details
3. ✅ Only adopt universal evaluation methodology: task decomposition, rubric design, QC rules & failure analysis
4. ✅ All test cases marked strictly:【Self-built Simulation】/【Public Resource Adapted】

1. ❌ 不使用任何公司原始标注数据、内部任务截图、内部模型输出、私有工具链与客户素材
2. ❌ 不复刻未对外公开的企业任务细节
3. ✅ 仅复用通用方法论能力：任务拆解、Rubric设计、质检规范、失败案例归纳、项目流程管控
4. ✅ 全部测试任务严格标注来源：【自建仿真任务】/【公开资料改写任务】

## 目录结构参考
```
agent_eval_lite/
  README.md
  data/
    tasks_master.xlsx   # 任务母表xlsx
    tasks_master.csv    # 任务母表csv
    office/      # 文档类任务
    coding/      # 代码类任务
    web/         # 网页类任务
    tools/       # 工具使用类任务
    multimodal/  # 多模态类任务
  rubrics/
    agent_rubric.md    # 评测维度
    failure_taxonomy.md       # 故障分类目录
    task_quality_checklist.md   # 任务完成质量检查清单
  scripts/        # 各类任务校验脚本
    generate_office_data.py    
    score_office.py
    score_coding.py
    analyze_task_distribution.py
  examples/       # 示例数据
    calibrated_outputs/
  reports/        # 生成评测报告
    agent_eval_system_design.md   # 评测体系设计报告
    dataset_building_report.md   # 数据集建设报告
  docs/
    daily_log.md   
```

## Quick Start｜如何使用
1. Clone repository
```bash
git clone https://github.com/jpeng5808-star/agent_eval_lite.git
```
2. Load dataset and perform automated/manual evaluation with rubric docs
3. Extend new tasks following official specification under /docs


1. 克隆仓库
```bash
git clone https://github.com/jpeng5808-star/agent_eval_lite.git
```
2. 调用评测集：加载dataset内任务，结合Rubric文档开展Agent自动化/人工测评
3. 参考docs内规范，基于现有规则拓展新增自建评测任务

## License
MIT

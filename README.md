# workbench-architect

`workbench-architect` 是一个面向 Codex 的工作台需求与提示词架构 Skill。

它会先通过对话或用户资料还原真实工作流，输出工作台定义卡；内容确认后生成三套与业务适配、具有完整设计深度的界面方向供用户选择；最后生成可在当前平台执行或复制到其他 Agent 平台的自包含搭建提示词。

## 核心流程

1. 提炼目标用户、真实流程、痛点、数据和交付环境。
2. 确认第一版范围、核心闭环和不做事项。
3. 输出工作台定义卡并等待确认。
4. 根据业务内容生成三套实质不同的界面方向。
5. 用户选择或混合界面方案，形成视觉规范卡。
6. 生成包含数据、交互、视觉、技术和验收标准的搭建提示词。

## 安装到 Codex

```powershell
python -X utf8 "$env:USERPROFILE\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" `
  --repo dorlarosendo434-hub/workbench-architect `
  --path . `
  --name workbench-architect
```

安装后重新打开 Codex，或在下一轮对话中调用：

```text
使用 $workbench-architect，帮我梳理需要什么工作台并生成可直接搭建的提示词。
```

## 使用许可

本项目采用自定义的“个人创作者使用许可”。它不是允许商业化转售的开源许可证。

允许：

- 独立创作者免费使用本 Skill。
- 使用生成的工作台管理自己的内容创作、付费商单、收入和个人创作业务。
- 为个人学习、研究、教学或非营利目的修改和使用。
- 在完整保留许可声明的前提下免费分享或分发。

禁止：

- 出售、出租或收费授权本 Skill 或生成的工作台。
- 提供付费代搭建、白标交付、订阅、SaaS 或托管服务。
- 将其主要功能包装为收费产品、课程交付物或商业服务。
- 删除、隐藏或改写非商业化声明。

需要商业化转售或收费服务授权时，必须先取得版权所有者的单独书面许可。完整条款见 [LICENSE.md](LICENSE.md)。

## 文件结构

```text
workbench-architect/
├── SKILL.md
├── LICENSE.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── discovery.md
    ├── delivery-options.md
    ├── prompt-blueprint.md
    └── visual-directions.md
```

## 免责声明

本项目按现状提供，不承诺适用于特定用途。许可声明用于明确作者的授权意图，不构成针对具体司法辖区或纠纷的法律意见。


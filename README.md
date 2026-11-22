# Agent Skills

可复用的 AI 编程工作流。第一项把代码实现与累计改动的验证放在两个阶段。

| Skill | 用途 |
| --- | --- |
| [implement-with-ci](skills/implement-with-ci/SKILL.md) | 实现需求、审查 diff，并按项目规则暂存。等用户要求验证或推送时，再检查整批改动。 |
| [ci-check](skills/ci-check/SKILL.md) | 按改动风险选择检查，必要时启动服务并实测受影响的接口。也可以单独调用。 |

## 安装

在目标项目下运行，同时安装两个 Skill。

```sh
npx skills add yyh12366/skill --skill implement-with-ci ci-check
```

## 使用

1. `使用 $implement-with-ci 实现这个需求，最后我会统一验证。`
2. 完成一批改动后，`使用 $ci-check 验证这批累计改动。`

验证范围和 Git 操作遵循用户指示及目标项目规则。

## 来源与许可

流程受到 [Matt Pocock 的工程 Skills](https://github.com/mattpocock/skills) 启发。测试取舍参考 [Test Value](https://github.com/tt-a1i/test-value)。

本仓库使用 [MIT 许可证](LICENSE)。第三方声明见 [THIRD_PARTY_NOTICES](THIRD_PARTY_NOTICES)。

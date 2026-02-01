以下是目前国际上最通用的 Git 提交前缀及其含义，我为你分类整理好了：

### 1. 代码开发类 (最常用)

| **前缀关键词**    | **含义**               | **适用场景**                                     | **示例**                                           |
| ------------ | -------------------- | -------------------------------------------- | ------------------------------------------------ |
| **feat**     | **新功能** (Feature)    | 开发了一个新的功能模块                                  | `git commit -m "feat: 添加CosyVoice2语音合成支持"`       |
| **fix**      | **修复** (Fix)         | 修复了一个 Bug                                    | `git commit -m "fix: 解决ASR模型显存溢出问题"`             |
| **refactor** | **重构** (Refactor)    | 代码更改，但**既不修复 Bug 也不添加新功能**（如重命名变量、移动文件、简化逻辑） | `git commit -m "refactor: 将后端代码移动至 src/backend"` |
| **perf**     | **性能** (Performance) | 提高代码性能的更改                                    | `git commit -m "perf: 优化推理速度，延迟降低20ms"`          |

### 2. 项目维护类

|**前缀关键词**|**含义**|**适用场景**|**示例**|
|---|---|---|---|
|**chore**|**杂务** (Chore)|构建过程或辅助工具的变动，不影响源代码（如修改 .gitignore，配置 CI/CD）|`git commit -m "chore: 更新 .gitignore 忽略模型权重文件"`|
|**build**|**构建**|修改构建系统或外部依赖（如 requirements.txt, setup.py）|`git commit -m "build: 添加 pipreqs 依赖"`|
|**ci**|**集成**|修改 CI 配置文件和脚本|`git commit -m "ci: 配置 GitHub Actions 自动测试"`|
|**revert**|**回退**|撤销之前的某次提交|`git commit -m "revert: 撤销上一版本的端口修改"`|

### 3. 文档与格式类

|**前缀关键词**|**含义**|**适用场景**|**示例**|
|---|---|---|---|
|**docs**|**文档** (Documentation)|仅修改了文档（README, 文档字符串）|`git commit -m "docs: 更新 README 添加模型下载链接"`|
|**style**|**格式** (Style)|**不影响代码运行**的格式修改（空格、分号、空行、PEP8 格式化）|`git commit -m "style: 修正 main.py 代码缩进"`|
|**test**|**测试** (Test)|添加缺失的测试或更正现有的测试|`git commit -m "test: 添加翻译接口的单元测试"`|

---

### 标准格式建议

一个完美的Commit Message通常遵循这个公式：

```
<type>(<scope>): <subject>
```

- **type**: 就是上面的关键词 (feat, fix, refactor...)。
- **scope**: (可选) 影响的范围，比如 `(asr)`, `(backend)`, `(ui)`。
- **subject**: 简短的描述，使用祈使句（"添加..." 而不是 "添加了..."）。
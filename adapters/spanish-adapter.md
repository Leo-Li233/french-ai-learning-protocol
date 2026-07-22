# 西班牙语适配器 / Spanish Adapter

> 西班牙语与法语同属罗曼语族，形态相似度高，AI 的西班牙语回答质量通常略好于法语。适配调整较小。

---

## 一、可信度矩阵调整

| 任务类型 | 法语可信度 | 西班牙语可信度 | 调整原因 |
|---|---|---|---|
| 动词变位验证 | 95%+ | 95%+ | 规则客观，调整微小 |
| 基础语法纠错 | 90%+ | 92%+ | 西班牙语训练数据略多于法语 |
| 固定搭配查询 | 75-85% | 80-90% | 西班牙语母语者更多，AI 训练更好 |
| 近义词辨析 | 70-80% | 75-85% | 同上 |
| 文化典故解释 | 50-65% | 60-75% | 西班牙文化相关内容 AI 表现更好 |
| 文学修辞分析 | 40-55% | 50-65% | 西班牙文学语料相对丰富 |

**总体调整：**所有可信度区间的上限可上调 5-10%。

---

## 二、错误类型本地化实例

### 错误类型1：规则过度泛化

**法语实例：** Il faut que tu sois courageux（虚拟式）
**西班牙语实例：** Es necesario que seas valiente（虚拟式）

注意：西班牙语中"Es necesario que"等表达也强制使用虚拟式，AI 同样可能错误使用直陈式。

### 错误类型2：搭配错误

**法语实例：** prendre une décision
**西班牙语实例：** tomar una decisión

注意：西班牙语中"做决定"也是固定搭配"tomar una decisión"，AI 可能错误生成"hacer una decisión"。

### 错误类型3：文化语境误判

**法语实例：** 正式信函结尾用 "Cordialement"
**西班牙语实例：** 正式信函结尾用 "Atentamente" 或 "Cordialmente"

注意：西班牙语中"Besos"等同于法语的"Bisous"，同样不可用于正式场合。

### 错误类型4：语域混淆

**法语实例：** "du coup" 不应出现在学术写作
**西班牙语实例：** "o sea" 不应出现在学术写作

注意：西班牙语中"o sea"（相当于"就是说"）是典型口语标记。

### 错误类型5：训练数据偏见

**法语实例：** information 在英语中不可数，被错误迁移到法语（可数）
**西班牙语实例：** información 在西班牙语中可数（la información, las informaciones）

注意：西语中也存在类似的英语-西语规则迁移错误。

---

## 三、提问模板术语替换

将法语协议中的以下术语替换为西班牙语对应概念：

| 法语术语 | 西班牙语对应 |
|---|---|
| 虚拟式 (le subjonctif) | 虚拟式 (el subjuntivo) |
| 条件式 (le conditionnel) | 条件式 (el condicional) |
| 复合过去时 (le passé composé) | 简单过去时 (el pretérito indefinido) |
| 未完成过去时 (l'imparfait) | 未完成过去时 (el pretérito imperfecto) |
| 介词搭配 (les prépositions) | 介词搭配 (las preposiciones) |
| 听写 (la dictée) | 听写 (el dictado) |
| 完形填空 (les points à compléter) | 完形填空 (completar espacios) |

---

## 四、西班牙语特有的 AI 优势

相比法语，西班牙语 AI 辅助有以下优势：

1. **训练数据更丰富**：西班牙语母语者约 5 亿，远超法语（约 3 亿）
2. **拼写更规则**：西班牙语发音与拼写高度对应，AI 在语音相关任务上表现更好
3. **语法变体较多**：AI 在拉美西语和西班牙西语之间需要切换，能力受限
4. **特殊字符**：ñ, á, é, í, ó, ú, ü 等特殊字符处理 AI 表现良好

---

## 五、西班牙语特有的 AI 局限

1. **拉美西语 vs 西班牙西语**：AI 可能混淆两者，特别是在使用 "vosotros" vs "ustedes"
2. **时态使用**：西语的简单过去时（preterito indefinido）和过去未完成时（preterito imperfecto）区分比法语更微妙
3. **ser vs estar**：AI 在这两个"是"动词的区分上偶有错误

---

## 六、推荐的 AI 工具

| 角色 | 推荐 | 备注 |
|---|---|---|
| 战术层 | 豆包、ChatGPT | 西语日常问答 |
| 战略层 | Claude、GPT-4 | 西语深度分析 |
| 文化类查询 | GPT-4 | 拉美 vs 西班牙文化差异 |
| 语法检查 | LanguageTool + AI 配合 | 专业语法检查工具 |

---

## 许可

CC-BY 4.0

# AI 错误案例集 / AI Error Cases

> 本文件整理了一学期间发现并验证的 AI 错误案例，按五类错误类型分组。
> 每个案例含：原问题、AI 错答、正确答案、验证来源、错误类型标签。

---

## 类型 1：语法规则过度泛化 (Rule Over-generalization)

### 案例 1.1：虚拟式强制语式

- **原问题**："Il faut que tu es courageux" 这句话对吗？
- **AI 错误回答**："这句话是对的。Il faut que 后面接直陈式，所以用 es。"
- **正确答案**：错误。Il faut que 后面必须接虚拟式，正确为 "Il faut que tu sois courageux"。
- **验证来源**：《法语现代语法》第12章虚拟式部分 + DeepSeek 交叉验证 + 老师确认
- **错误类型**：语法规则过度泛化
- **分析**：AI 将"il faut"的字面含义（"需要"是一种事实）与语法规则混淆。这是典型错误——AI 不理解"表达必要性"在法语语法中强制触发虚拟式。

### 案例 1.2：条件式与直陈式

- **原问题**："Si j'avais le temps, je vais au cinéma" 这句话对吗？
- **AI 错误回答**："这句话是对的。"
- **正确答案**：错误。Si + 未完成过去时，主句应当用条件式，正确为 "Si j'avais le temps, j'irais au cinéma"。
- **验证来源**：《法语现代语法》+ 老师确认
- **错误类型**：语法规则过度泛化
- **分析**：AI 没有识别"Si + 未完成过去时"的固定模式对主句语式的强制要求。

---

## 类型 2：例句拼接错误 (Collocation Mismatch)

### 案例 2.1：固定搭配

- **原问题**：请用法语翻译"做一个决定"
- **AI 错误回答**：faire une décision
- **正确答案**：prendre une décision
- **验证来源**：Larousse 词典在线版 + 法语助手确认
- **错误类型**：例句拼接错误
- **分析**：AI 知道"faire"="做"、"décision"="决定"，将二者字面拼接。但法语中"做决定"的固定搭配是"prendre une décision"。

### 案例 2.2：动词搭配

- **原问题**：用法语表达"犯了一个错误"
- **AI 错误回答**：faire une faute
- **正确答案**：commettre une faute
- **验证来源**：法语助手 + 老师确认
- **错误类型**：例句拼接错误
- **分析**：AI 倾向于使用"faire + 名词"的通用结构，但"commettre une faute"才是正确搭配。

---

## 类型 3：文化语境误判 (Pragmatic Mismatch)

### 案例 3.1：信函结尾用语

- **原问题**：帮我写一封给法国大学教授的邮件结尾
- **AI 错误回答**：Bisous, [你的名字]
- **正确答案**：应使用 "Cordialement" 或 "Respectueusement" 等正式结尾
- **验证来源**：法语商务信函写作规范 + 老师确认
- **错误类型**：文化语境误判
- **分析**："Bisous"是亲密朋友/家人间的用语，用在给教授的信函中属于严重失礼。AI 不能理解社交距离和语用规范。

### 案例 3.2：口语化程度

- **原问题**：帮我用法语写一段问候朋友的生日消息
- **AI 错误回答**：Cher ami, je vous souhaite un excellent anniversaire. Cordialement.
- **正确答案**：Joyeux anniversaire mon ami ! J'espère que tu passes une super journée. Bisous.
- **验证来源**：法语母语朋友反馈
- **错误类型**：文化语境误判
- **分析**：AI 在"问候朋友"这种非正式场景中仍然使用正式语体（cher、vous、cordialement），不符合法语母语者之间的日常交流习惯。

---

## 类型 4：语域混淆 (Register Confusion)

### 案例 4.1：学术写作中的口语化

- **原问题**：帮我把这段口语转写成学术法语：Je pense que c'est super important. Du coup il faut faire attention.
- **AI 错误回答**：Je pense que c'est très important, du coup il faut faire attention.
- **正确答案**：Il apparaît essentiel de souligner que...（去掉"Je pense"、"du coup"等口语元素）
- **验证来源**：法语学术写作指南 + DeepSeek 交叉验证
- **错误类型**：语域混淆
- **分析**："du coup"是典型的口语填充词，不应出现在学术写作中。AI 虽然做了词汇层面的替换（super → très），但没有识别并移除口语标记。

### 案例 4.2：商务邮件中的学术化

- **原问题**：帮我写一封简单的法语商务邮件确认会议时间
- **AI 错误回答**：Nous avons l'honneur de vous informer que la réunion sera tenue le 15 juin...
- **正确答案**：Je vous confirme notre rendez-vous du 15 juin à 14h. Cordialement.
- **验证来源**：法语商务沟通指南
- **错误类型**：语域混淆
- **分析**：AI 把商务邮件写得过于学术化（"avons l'honneur"等），显得不自然。

---

## 类型 5：训练数据偏见 (Training Data Bias)

### 案例 5.1：英语规则错误迁移

- **原问题**：法语中 "information" 是可数还是不可数？
- **AI 错误回答**：不可数，和英语一样，用 "some information"
- **正确答案**：法语中 "information" 是可数名词，"une information, des informations"
- **验证来源**：Larousse 词典 + 《法语现代语法》
- **错误类型**：训练数据偏见
- **分析**：英语 "information" 不可数（不能说 an information），AI 将英语语法规则错误迁移到法语。这是因为英语在训练数据中占比远高于法语。

### 案例 5.2：英语词序影响

- **原问题**：请用法语表达"我喜欢这本书"
- **AI 错误回答**：J'aime ce livre. （这个本身正确）
- 但在更复杂的句子里：AI 经常按英语的语序 "I like this book very much" 生成 "J'aime beaucoup ce livre"（正确）vs "J'aime ce livre beaucoup"（错误）
- **正确答案**：法语否定句中，"pas" 应当放在动词后，但 AI 在处理 "I don't like this book" 时偶有生成 "Je ne pas aime ce livre"（错误），正确为 "Je n'aime pas ce livre"
- **验证来源**：法语语法规则
- **错误类型**：训练数据偏见
- **分析**：英语否定句中 "not" 放在动词后（"I do not like"），AI 偶有将这一语序错误应用到法语否定结构中。

---

## 错误统计摘要

基于一学期观察：
- 类型 1（语法规则过度泛化）：约 8 次
- 类型 2（例句拼接错误）：约 12 次
- 类型 3（文化语境误判）：约 5 次
- 类型 4（语域混淆）：约 7 次
- 类型 5（训练数据偏见）：约 3 次

**总错误发现次数：约 35 次**（来自约 200+ 次 AI 对话，错误率约 17%）

## 错误识别能力的变化

- 初期（前四周）：面对 AI 故意加入错误的回答，识别率约 40%
- 中期（第 5-12 周）：识别率约 60-70%
- 后期（最后四周）：识别率约 85%

这一变化反映了**AI 元认知能力**的实质性提升。

## 许可

CC-BY 4.0

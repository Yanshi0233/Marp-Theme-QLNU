---
marp: true
theme: qlnu
paginate: true
math: latex
---

<!-- _class: lead -->

![校徽](./images/qlnu.png)

# Marp模板主题

## QLNU

**制作者 Yanshi0233**
齐鲁师范学院·生命科学学院·生物信息学
2024/11/19

---

<!-- _class: dir -->

1. 使用介绍
2. 代码样式
3. 图片
4. 其他


---

<!-- _class: title -->

# 这是<br />一个标题

内容

![校徽 logo](./images/qlnu.png)

---

<!-- _header: 使用介绍 -->

+ Marp是一个基于Markdown格式的PPT生成器。它与LaTex和传统的Markdown编辑器类似，但是支持自定义主题。为了便于齐鲁师范学院学生和教师使用，编者设计开发了此QLNU主题。

+ 要使用此主题，需要在VSCode中注册`./themes/qlnu.css`，或者您可以重命名并使用您自己的设置。

+ 此主题使用MIT开源协议。



---

<!-- _header: 代码样式 -->

这是Python代码块示例。

```python
from transformers import AutoModelForMaskedLM, AutoTokenizer
model = AutoModelForMaskedLM.from_pretrained("cl-tohoku/bert-base-japanese-whole-word-masking")
tokenizer = AutoTokenizer.from_pretrained("cl-tohoku/bert-base-japanese-whole-word-masking")

inputs = tokenizer.encode_plus("私はとても[MASK]です。", return_tensors='pt')
outputs = model(**inputs)
tokenizer.convert_ids_to_tokens(outputs.logits[0][1:-1].argmax(axis=-1))
```

或者同样可以使用`行内代码块`。


---

<!-- _header: 数学公式 -->

$$ I_{xx}=\int\int_Ry^2f(x,y)\cdot{}dydx $$

$$
f(x) = \int_{-\infty}^\infty
    \hat f(\xi)\,e^{2 \pi i \xi x}
    \,d\xi
$$

您可以直接在Markdown中使用$\LaTeX$格式的数学公式。

---

<!-- _header: 图片 -->

您可以直接使用Markdown标记在您的文档中插入图片。

![w:300 center](./images/kenkyu_woman_seikou.png)



---

<!-- _header: 其他 -->

您可以使用**着重号**显示加粗标记，使用*倾斜符*表示倾斜，~~删除线~~等（PDF导出似乎不支持倾斜和删除线，主题的作者正在想办法解决）。

似乎不支持Markdown的上标和下标，不过可以使用行内公示$2^2$,H$_2$O，用以编写上下标。

> 另外，您还可以在这里插入脚注。
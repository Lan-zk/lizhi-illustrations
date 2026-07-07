# 生图提示词模板

每张图单独生成。根据文本内容替换变量，不要把多张图拼在一起。

```text
Generate one standalone 16:9 horizontal Chinese concept-explanation illustration.

Visual DNA:
Pure white background. Minimalist black hand-drawn line art. Slightly wobbly pen lines. Lots of empty white space. Sparse red/orange/blue handwritten Chinese annotations. Clean absurd product-sketch feeling. No gradients, no shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no cute mascot poster, no children's illustration, no realistic UI.

Recurring IP character required:
Lizhi, a small compact lop-eared rabbit with a pale cream (#efe3c5) dominant body, softened light brown (#a79282) broad irregular patches, predominantly light-brown floppy ears, a broad light-brown eye-area marking extending toward the ear base, dark round-dot eyes, a clearly visible small rabbit nose, and a distinct three-part rabbit mouth. Keep the forehead center, muzzle, chest, belly, and most legs pale cream. The markings must be stable, organic, and asymmetrical, never random tiny dots, polka dots, stripes, or symmetrical patterns. Lizhi must perform the core conceptual action, not decorate the scene. Make Lizhi blank, dull, calm, serious, deadpan, and slightly absurd, not cute.

Theme:
{解析配图主题}

Structure type:
{结构类型：定义图 / 对比图 / 进程图 / 关系图 / 张力图 / 问答链 / 层次图 / 隐喻图}

Core idea:
{这张图要表达的核心意思}

Composition:
{具体画面：Lizhi 在哪里、正在做什么、主要物件是什么、信息如何流动}

Suggested elements:
{元素1} / {元素2} / {元素3} / {元素4}

Chinese handwritten labels:
{标注词1} / {标注词2} / {标注词3} / {标注词4} / {可选标注词5}

Color use:
Black for main line art, labels, objects, structure, and Lizhi's eyes/necessary line details. Pale cream (#efe3c5) and softened light brown (#a79282) only for Lizhi's body and fixed markings. Orange for main flow/path/arrows. Red only for key warnings/problems/results. Blue only for secondary notes or feedback/system state.

Constraints:
One image explains only one core structure. Keep the main subject around 40%-60% of the canvas. Preserve at least 35% blank white space. Use at most 5-8 short handwritten Chinese labels. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, or dense explainer. Do not copy prior examples or reuse known case compositions unless explicitly requested; invent a fresh visual metaphor for this specific text. It should be clear but not instructional, interesting but not childish, strange but clean.
```

## 图像编辑提示

去掉左上角标题：

```text
Edit the provided image. Remove only the handwritten title "{要删除的文字}" and its underline from the top-left corner. Fill that area with the same clean white background, matching the surrounding blank paper. Preserve everything else exactly: characters, labels, paths, line style, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

增强怪诞感：

```text
Regenerate this illustration with the same core meaning and simple layout, but make Lizhi more central to the conceptual action. Lizhi should be doing the strange work that explains the idea, not standing beside the diagram. Keep Lizhi recognizable as the pale-cream and light-brown lop-eared rabbit, and keep the scene clean, sparse, hand-drawn, and not cute.
```

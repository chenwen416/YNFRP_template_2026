# 云南省基础研究计划项目申请书 LaTeX 模板（2027 版）
版本号: ver.260613

> 非官方模板。请最终以云南省科技厅系统、官方 Word 模板和当年申报通知为准。
 如果你使用本模板撰写的基金申请获得资助，欢迎发邮件告知作者。
一封简短的感谢邮件即可，这将是对作者整理和维护本模板的最好鼓励。

## 1. 模板作者与版权声明

本模板由 **陈文（Wen Chen）** 根据官方《省基础研究计划项目申请书撰写提纲（2027版）》整理和改写为 LaTeX 模板。

- 作者：陈文（Wen Chen）
- 单位：中国科学院云南天文台（Yunnan Observatories, Chinese Academy of Sciences）
- 邮箱：chenwen@ynao.ac.cn

本模板仅作为个人学习、科研写作和排版参考。使用本模板进行基金申请时，可能存在未通过系统上传、格式审查或形式审查的风险。任何使用者应自行核对官方模板、官方系统要求、当年申报通知和依托单位管理部门要求，并自行承担由使用本模板造成的一切风险。作者不对格式审查结果、项目申报结果、系统兼容性、字体版权、文件上传问题或其他任何后果承担责任。

**使用本模板即视为自动认可上述免责声明。**

如果你使用本模板撰写的基金申请获得资助，欢迎发邮件告诉作者一声，表达感谢即可。

## 2. 第三方参考文献格式文件说明

本模板中的参考文献排版使用了 `gbt7714` 系列 BibTeX 样式文件，来源为：

- GB/T 7714 BibTeX Style
- 原作者：Zeping Lee `<zepinglee AT gmail.com>`
- 项目地址：`https://github.com/zepinglee/gbt7714-bibtex-style`
- 许可协议：LaTeX Project Public License, version 1.3c or later

如果项目中包含以下文件：

```text
gbt7714.sty
gbt7714-numerical.bst
gbt7714-author-year.bst
```

请保留其原始版权和许可说明，不要删除原作者的版权声明。若不希望在本模板项目中分发这些第三方文件，可以删除本地副本，并依赖 Overleaf / TeX Live 自带的 `gbt7714` 包；但需自行确认编译环境中已经安装该包。

## 3. 文件结构建议

推荐项目目录结构如下：

```text
main.tex
ynfund2027.sty
ynfund2027-frontmatter.tex
ynfund2027-attachments.tex
ref.bib
README.md

sections/
  01_lixiang.tex
  02_yanjiuneirong.tex
  03_1_jichu_kexingxing.tex
  03_2_gongzuotiaojian.tex
  03_3_zaichengdan.tex
  03_4_yiwancheng.tex
  04_1_ai.tex
  04_2_other.tex

imgs/
  example_figure.pdf
  example_figure.png

fonts/
  times.ttf
  timesbd.ttf
  timesi.ttf
  timesbi.ttf
  方正仿宋GBK.ttf
  方正小标宋简体.ttf
  方正楷体GBK.ttf
  方正黑体GBK.ttf
  方正黑体简体.ttf
```

说明：

- `main.tex`：主文件，一般不需要频繁修改。
- `ynfund2027.sty`：模板格式文件，包含页面、字体、页码、标题、表格等格式设置。
- `ynfund2027-frontmatter.tex`：固定前置内容，例如“附件6”、题名、“一、信息表格”、“二、正文”等。
- `ynfund2027-attachments.tex`：固定后置内容，例如“三、个人简历”、“四、附件”和附件材料表。
- `sections/`：正文填写区。日常写作时主要编辑这里的文件。
- `imgs/`：图像文件夹，建议所有图片统一放在这里。
- `ref.bib`：参考文献数据库。

## 4. 编译方式

建议使用 **XeLaTeX** 编译。

如果使用参考文献，推荐编译顺序为：

```text
XeLaTeX -> BibTeX -> XeLaTeX -> XeLaTeX
```

在 Overleaf 中：

1. 打开项目设置；
2. Compiler 选择 `XeLaTeX`；
3. 主文件选择 `main.tex`；
4. 点击 Recompile；
5. 如果参考文献未更新，可使用 “Recompile from scratch”。

## 5. 字体说明

本模板尽量模拟官方 Word 模板中的字体设置：

- 题名：方正小标宋简体，二号；
- 一级标题：方正黑体简体，三号；
- 正文：方正仿宋 GBK，三号；
- 提纲标题：方正楷体 GBK，三号；
- 页码和英文/数字：Times New Roman。

**请注意：字体文件可能受版权保护。请确保你对上传到 Overleaf 或本地使用的字体文件拥有合法使用权。不要公开分发没有授权的商业字体文件**。

## 5A. 字体版权与非商业使用免责声明

本模板为非官方 LaTeX 模板，仅供个人学习、科研写作、非商业性基金申请排版和个人内部参考使用，严禁将本模板、由本模板改造得到的模板、或与本模板配套使用的字体文件用于任何商业活动、商业分发、收费服务、培训销售、模板售卖、商业代写、商业排版服务或其他营利性用途。

本模板可能需要调用用户自行准备的字体文件，例如 Times New Roman 以及方正仿宋、方正小标宋、方正黑体、方正楷体等字体。上述字体文件可能受各自权利人版权、商标权、授权协议或其他知识产权条款保护。本模板作者不提供、不分发、不授权任何商业字体文件，也不对任何字体文件的来源、授权状态、可用范围或合法性作出保证。使用者应自行确认其所使用字体文件的授权范围，并确保其在本地计算机、Overleaf 或其他编译环境中使用这些字体的行为符合相关字体授权协议和法律法规。

若使用者未经授权上传、复制、传播、分发、嵌入、转售或以其他方式使用受版权保护的字体文件，或将本模板及相关字体用于商业活动，由此产生的任何版权纠纷、商业侵权、法律责任、经济损失、行政处罚或第三方索赔，均由使用者自行承担。本模板作者陈文（中国科学院云南天文台，Yunnan Observatories, CAS）不承担任何直接或间接责任。

使用、复制、修改或继续传播本模板，即视为使用者已经阅读、理解并同意本字体版权与非商业使用免责声明。

## 6. 如何填写正文

日常写作时，建议只编辑 `sections/` 文件夹中的文件。

例如：

```text
sections/01_lixiang.tex
sections/02_yanjiuneirong.tex
sections/03_1_jichu_kexingxing.tex
...
```

在这些文件中直接写正文即可，不需要再手动套用 `\YNFixedPara{...}` 命令。模板已经设置了默认正文格式：

- 中文为方正仿宋 GBK 三号；
- 英文、数字为 Times New Roman；
- 段首自动缩进两个字符；
- 段间距为 0。

示例：

```latex
本项目拟围绕射电星高精度VLBI天体测量开展研究，重点解决近场参考源筛选、相位参考误差控制和轨道运动拟合等问题。

第二段直接另起一段书写即可。一般不需要手动添加 \quad、\hspace 或全角空格。
```

## 7. 插入参考文献

在 `ref.bib` 中加入 BibTeX 条目，例如：
**可使用ADS导出BibTex条目**

```bibtex
@ARTICLE{2023MNRAS.524.5357C,
       author = {{Chen}, Wen and {Zhang}, Bo and {Zhang}, Jingdong and {Yang}, Jun and {Xu}, Shuangjing and {Sun}, Yan and {Mai}, Xiaofeng and {Shu}, Fengchun and {Wang}, Min},
        title = "{VLBI Astrometry of radio stars to link radio and optical celestial reference frames. I. HD 199178 \& AR Lacertae}",
      journal = {\mnras},
     keywords = {radio continuum: stars, astrometry, parallaxes, proper motions, reference systems, Astrophysics - Solar and Stellar Astrophysics, Astrophysics - Astrophysics of Galaxies, Astrophysics - Instrumentation and Methods for Astrophysics},
         year = 2023,
        month = oct,
       volume = {524},
       number = {4},
        pages = {5357-5367},
          doi = {10.1093/mnras/stad1214},
archivePrefix = {arXiv},
       eprint = {2304.10886},
 primaryClass = {astro-ph.SR},
       adsurl = {https://ui.adsabs.harvard.edu/abs/2023MNRAS.524.5357C},
      adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}
```

正文中引用：

```latex
已有VLBI天体测量工作表明，射电星可以用于连接射电和光学参考架\citep{2023MNRAS.524.5357C}。
```

如果希望使用作者-年份格式，需要同时修改 `ynfund2027.sty` 中的参考文献样式设置；默认建议使用数字制，更节省空间。

## 8. 插入图像

建议把图片放在 `imgs/` 文件夹中。例如：

```text
imgs/arlac_calibrator_geometry.pdf
imgs/spectral_index.png
```

正文中插入图片示例：

```latex
\begin{figure}[htbp]
  \centering
  \includegraphics[width=0.85\linewidth]{imgs/arlac_calibrator_geometry.png}
  \caption{AR Lac 与候选近场参考源的相对位置示意图。}
  \label{fig:arlac_calibrator_geometry}
\end{figure}
```

正文中引用图片：

```latex
如图~\ref{fig:arlac_calibrator_geometry} 所示，新候选参考源与 AR Lac 的角距离显著小于以往相位参考源。
```

## 9. 插入表格

普通三线表示例：

```latex
\begin{table}[htbp]
\centering
\caption{候选参考源的射电流量密度示例。}
\label{tab:radio_flux}
\begin{tabular}{lcc}
\toprule
巡天/目录 & 频率/GHz & 流量密度/mJy \\
\midrule
LoTSS & 0.144 & 25.7 \\
NVSS  & 1.4   & 19.8 \\
VLASS & 3.0   & 31.0 \\
\bottomrule
\end{tabular}
\end{table}
```

如果表格较长，可以使用 `longtable`。例如：

```latex
\begin{longtable}{p{0.25\linewidth}p{0.25\linewidth}p{0.40\linewidth}}
\caption{年度研究计划示例。}
\label{tab:year_plan}\\
\toprule
年度 & 主要任务 & 预期结果 \\
\midrule
\endfirsthead
\toprule
年度 & 主要任务 & 预期结果 \\
\midrule
\endhead
第1年 & 参考源验证观测 & 确认候选参考源的致密性和可用性 \\
第2年 & 多历元VLBI观测 & 获得AR Lac的高精度位置序列 \\
第3年 & 轨道拟合与论文撰写 & 完成天体测量模型和成果发表 \\
\bottomrule
\end{longtable}
```

## 10. 常见注意事项

1. **不要随意修改固定模板文件**  
   一般只编辑 `sections/` 文件夹中的内容。`ynfund2027-frontmatter.tex` 和 `ynfund2027-attachments.tex` 用于固定官方提纲内容，建议不要随意修改。

2. **不要删除官方提纲标题和括号说明**  
   官方模板通常要求不要删除或改动提纲标题及括号中的文字。

3. **不要公开分发字体文件**  
   字体文件可能有版权限制。项目分享时请确认你有权分发这些字体。

4. **注意参考文献文件的第三方许可**  
   `gbt7714` 相关文件属于第三方 LaTeX/BibTeX 样式文件，应保留原版权和许可说明。

5. **最终提交前务必对照官方 Word 模板核查**  
   本模板只是非官方 LaTeX 版本，不能保证通过所有形式审查。

## 11. 建议工作流程

1. 在 Overleaf 或本地创建项目；
2. 上传 `main.tex`、`ynfund2027.sty`、固定模板文件和 `sections/` 文件夹；
3. 上传合法可用的字体文件到 `fonts/`；
4. 把图片放入 `imgs/`；
5. 在 `sections/` 中逐节填写正文；
6. 在 `ref.bib` 中维护参考文献；
7. 使用 XeLaTeX 编译；
8. 导出 PDF 后与官方 Word 模板逐项核对；
9. 提交前请向依托单位科研管理部门确认格式要求。

## 12. 免责声明

本模板为个人整理的非官方 LaTeX 模板，不代表云南省科技厅、项目管理系统、依托单位或任何官方机构意见。作者不保证本模板满足任何年度、任何类别项目的正式申报要求。使用者应自行承担使用本模板带来的一切风险。使用本模板即表示你已经阅读、理解并接受本免责声明。

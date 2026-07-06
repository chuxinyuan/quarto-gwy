# 党政机关公文 Quarto Extensions

这是一个专门用于生成符合[《党政机关公文格式》（GB/T 9704-2012）](https://openstd.samr.gov.cn/bzgk/std/newGbInfo?hcno=F3CC9BEF482524C895FDA7A08BB4A70E)国家标准的 Word 版公文的 Quarto 扩展。

## 项目目标

通过定制 Quarto Extensions，方便地生成满足《党政机关公文格式》（GB/T 9704-2012）国家标准格式要求的 Word 版公文，既方便自己又方便分享给别人。

- 完全符合 GB/T 9704-2012 标准，全程零人工格式调整
- 支持各种公文类型（通知、报告、函、纪要、讲话稿等）

## 扩展组件

本扩展包含以下核心组件：

1. **`_extension.yml`** - 扩展配置文件
2. **`template.docx`** - 公文模板

## 安装扩展

- 命令行安装

```bash
quarto use template chuxinyuan/quarto-gwy
```

- R 代码安装

```r
quarto::quarto_use_template("chuxinyuan/quarto-gwy", no_prompt = TRUE)
```

## 安装 R 包

```r
if (!require("systemfonts")) {
  install.packages("systemfonts")
}
```

## 安装字体

开始使用前，请确保系统已安装公文正常显示所需要的字体：

- 方正小标宋_GBK
- 仿宋_GB2312
- 黑体
- 楷体

## 快速开始

项目包含一个完整的示例：

- `_quarto.yml`
- `content.qmd`
- `main.qmd`

运行以下命令查看效果：

```bash
quarto render main.qmd
```

或者

```r
quarto::quarto_render("main.qmd")
```

## 技术支持

如遇到问题，请检查：
1. Quarto >= 1.4.549
2. 系统字体安装情况
3. 文件路径和权限

如果扩展无法正常加载：
1. 确保 `_extensions` 文件夹在项目根目录
2. 检查 `_extension.yml` 文件格式是否正确
3. 使用 `quarto check` 检查 Quarto 安装

## 项目许可

本项目采用 MIT 许可证。

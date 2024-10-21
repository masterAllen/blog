# 说明

本仓库是我的个人博客，由 mkdocs 搭建，使用的主题是 mkdocs-material

## 本仓库的创建方式

通常博客都是由一堆 markdown 组成。但是我感觉学习笔记有各种各样的格式，除了 markdown，有时会直接用 word 或者 ppt 来写，有时看到好的内容会保存为照片、网页或者 pdf 等，甚至经常会有视频文件（尤其是一些系统性的课程）。

如果为了博客而强制写 markdown，我觉得受限太多，失去了意义。因此本仓库是由另一个文件夹转换而来，其中原始文件夹里面包含了各种各样的笔记，通过 python 脚本将其转换为 markdown 以此来在网页中显示。比如 pdf 文件，我会将其转为图片，然后将这些图片写入到 markdown 中，这样在网页上就能够将其显示出来了。

目前各个格式的文件转换还在开发中。我觉得肯定很多地方尚不完善，比如 word 我是用 docx2pdf 转为 pdf 后再转为图片，期间经常会报错。如果您有任何格式转换的方法和建议，烦请帮忙告知我一下，谢谢。

## 各种格式转换方式

| 格式     | 方式                                                                                                           |
| -------- | -------------------------------------------------------------------------------------------------------------- |
| markdown | 直接转换，会检查其中的引用链接，找到引用的文件（通常是图片），将其移动到资源仓库中，然后修改原始文件的链接内容 |
| ipynb    | 使用 jupyter nbconvert 进行转换                                                                                |
| pdf      | 使用 pdfium 转为图片，将图片合成到一个 markdown 中                                                             |
| word     | 使用 docx2pdf 转为 pdf，再转为图片，将图片合成到一个 markdown 中                                               |
| ppt      | 使用 pptx2pdf 转为 pdf，再转为图片，将图片合成到一个 markdown 中                                               |
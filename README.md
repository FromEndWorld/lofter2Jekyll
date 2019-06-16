# lofter2jekyll

本工具用于将lofter的导出的xml文件拆分为可读、可再发布的md文档，并支持下载其中的图片。

使用[LOFTER2Hexo](https://github.com/boboidream/LOFTER2Hexo)修改而成。

实际上原版已经支持jekyll，jekyll和Hexo的md格式上也没有什么本质区别，但原作者上次维护是2017年，所以单独建个repo重新发布一下。

### 主要改动: 

* 处理更多标题特殊字符
* 添加图片下载失败时报错并继续机制
* 现在图片po的文字说明也会输出了
* 修正md输出文件中的一些格式错误

### 仍然存在的问题：

* 不支持长文章
* 不支持音乐和视频
* 大量图片下载易出错

## 使用说明

### 安装

publish没搞好，崩溃中【。
<!--



1. 安装 node.js → [Node.js 下载](https://nodejs.org/en/download/)

2. 安装项目

    ```
    npm install lofter2jekyll -g
    ```
-->


### 使用

1. 将 LOFTER 导出的 XML 文件命名为: `LOFTER.xml`

2. `LOFTER.xml` 在所在文件夹打开命令行，输入 `readxml` 回车运行

3. 程序会生成 `LOFTER` 文件夹并在其中写入所有Markdown文档

4. 将图片下载至 `LOFTER/img` 文件夹

5. 以上运行过程会在终端打印出日志

### 选项

```
  Usage: readxml [options]

  Options:

    -h, --help           output usage information
    -V, --version        output the version number
    -i, --input <lang>   xml 文件路径，例如：`/Github/test.xml`
    -n, --notag          头部不生成 tags 标签（以避免生成太多 `Tags` 造成的不美观）
    -a, --author <lang>  设置 author （xml中无此字段）
```
例如

```
readxml -n -a endworld
# 解析当前目录下 LOFTER.xml 文件，生成不带 Tags 标签的 Markdown 文件，头部 author: endworld
```

## 其他选项

另有功能类似的脚本[lofter2Hexo](https://github.com/alicewish/Lofter2Hexo)大家可以试试。

墨问太太的脚本基于Python，这个基于JS。

这个的优点大概是下载图片比较利索，直接根据图片URL下载并且链接到md文档中。

缺点是没有图形界面（我不会做），需要安装node.js和使用命令行，还有它不能直接将导出内容再发布。

## 帮助完善这个脚本

使用中出现问题可以提issue，需要把console（你运行程序以后，命令行返回的内容）的报错内容告诉我。

也欢迎pull request。

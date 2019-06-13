# lofter2Jekyll

本脚本用于将lofter的导出的xml文件拆分为可读、可再发布的md文档，并支持下载其中的图片。

使用[LOFTER2Hexo](https://github.com/boboidream/LOFTER2Hexo)修改而成。

实际上原脚本已经支持Jekyll，Jekyll和Hexo的md格式上也没有什么本质区别，但原作者上次维护是2017年，所以单独建个repo和重新发布一下。


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

## 其他说明

功能类似的脚本[lofter2Hexo](https://github.com/alicewish/Lofter2Hexo)，墨问太太的脚本基于Python，这个基于JS。

这个的优点大概是下载图片比较利索，直接按URL下载。

缺点是没有图形界面（我不会做），需要安装node.js和使用命令行，还有它不能直接将导出内容再发布，而且我对MacOS怎么用也一无所知。

使用中出现问题可以提issue，需要把console（你运行程序以后，命令行返回的内容）的报错内容告诉我。


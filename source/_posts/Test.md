# 基于Cloud Pages搭建自己的博客
---
## 1.发布文章


```bash
cd C:\Users\lh153\Documents\blog     
```

> 在终端打开存放git仓库的文件夹
>

```bash
hexo new "Post Name"
```

>接着在终端里输入，就会在blog下生成对应.md
>
>也有hexo new post" "的写法
>

```bash
hexo server
```

>会看到

```bash
INFO  Hexo is running at http://localhost:4000/ . Press Ctrl+C to stop.
```

>就可以去运行[本地服务器](http://localhost:4000/)预览效果了🤔应该都是这个网址吧,几乎是实时预览的🤔
>>！注意！：关掉终端本地服务器就歇菜了，不能嫌挡害就给关了
>

```bash
git add .
git commit -m "Post Name"
git push
```

>就传上去了吧🤔
>>！记得Ctrl+S！
>

## 2.乱序问题

![如图](/images/Belike.png)

  原理应该就是本地的 VS Code 和线上的博客系统（比如 Hexo）使用的是不同Markdown 解析器，而VS Code 的解析器比较宽容。当你的 Markdown 语法格式有一点小瑕疵，Hexo 解析就会错位。

目前我用着好使的解决办法 :
* 在 \``` 的上方和下方，一定要各留一个空行。不要让它和普通文本或 > 引用紧紧贴在一起。而且在代码块开头附加语言名称(eg:  \```     bash)
* 总之多打空格🤔这个换行或者留空就很神奇，我也没研究明白🤔


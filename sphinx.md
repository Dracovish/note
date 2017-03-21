# Sphinx
## 简介
> Sphinx由俄罗斯人Andrew Aksyonoff 开发的高性能全文搜索软件包，在GPL与商业协议双许可协议下发行。全文检索是指以文档的全部文本信息作为检索对象的一种信息检索技术。检索的对象有可能是文章的标题，也有可能是文章的作者，也有可能是文章摘要或内容。

### 写在前面
> sphinx本身是可以支持中文搜索的，只是不支持中文分词，需要安装中文分词插件，coreseek就是一个打包了mmseg中文分词插件和sphinx源码的安装包。
> 目前coreseek已经很久不更新了，稳定版3.2.14内带的的sphinx还是 0.9.9 release版本的；而sphinx可以通过设置为“一元切分模式”来支持搜索中文
> 在实际使用中，搜索非中文的话，sphinx比coreseek要快；搜索短中文字符串的话，开启了“一元切分模式”的sphinx比coreseek要快；只有在搜索长中文字串时，coreseek的分词优势才能显现，比sphinx要快
> 所以根据你的应用场景来选择用哪个，如果是索引英文、数字、字符较多的数据，就用源生sphinx；如果是索引中文非常多非常长的数据，还是用coreseek吧
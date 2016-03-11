
用于Vim自动加载模板的一个插件, 忘记是从那里得到的了.

之前写C的时候做过一点修改, 没想过别人会使用, 所以可能会有坑. 

如果有感兴趣的朋友, 读一下源码里的说明应该很容易懂. 

嗯, 最后别忘了将下面两行放入.vimrc:
let g:template_load = 1
let g:template_tags_replacing = 1

关于自定义模板
插件的templates目录下有几个模板, 只要将上面两行放入.vimrc后就能正常工作(Debian下, Windows可能会出问题).
如果要自定义模板, 首先在 '~' 目录下新建一个文件夹, 比如 .tpl
然后在 .tpl 目录中建立模板文件, 模板文件的名称统一为tpl, 以后缀名做区分. 
比如有 tpl.html  

最后在 .vimrc 中加入一行:
let g:template_path = './.tpl'

那么新建后缀名为html的文档或者打开空白的后缀名为html的文档时将会将tpl.html这个模板文档的内容载入. 

# Eleven-x CMS ROAD MAP

- 模板支持多语言
- 模板内容数据支持以数据的形式载入
- 支持在页面编辑器中使用特定的符号(@)触发吊起文件选择器
- 增加ogp的插件,方便更好的把页面分享出去
- 增加默认的humans.txt文件



## 模板支持多语言
 
 - 在项目初始化的时候会确定网站以什么语言模式运行,标识语言的数据记录在Application容器对象上面
 - 系统会语言优先选择符合语言的页面,如果找不到会fallback到模板的页面,否则404报错。具体规则如下:
   
        
   >     例如访问/about这个地址
   >     - 遍历解析解析page文件下的所有文件,解析出{url:[Page]}映射列表
   >     - 找出url对应的Page列表
   >     - 优先 {lang}/{Page.filename}
   >     - {Page.filename}_{lang}
   >     - {Page.filename}
   >     - 404 
   


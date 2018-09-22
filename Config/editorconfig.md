## 统一代码风格工具---editorconfig
    在团队开发中，统一的代码格式是必要的，但是不同开发人员的代码风格不同，代码编辑工具的默认格式也不相同，这样就造成代码的differ,而editorConfig可以帮助
开发人员在不同的编辑器和IDE中定义和维护一致的编码风格。
## 简述
  editorConfig不是软件，而是一个名称为.editorconfig的自定义文件，该文件用来定义项目的编码规范，编辑器的行为会与.editorconfig文件中定义的一致，并且其优先
级比编辑器自身的设置要搞，在多人合作开发项目时是必要的。<br>
 有些编辑器默认支持editorconfig,如webstorm,而有些编辑器则可能需要安装editorconfig插件，当打开一个文件时，EditorConfig插件会在打开文件的目录和其每一级父
目录查找.editorconfig文件，知道有一个配置文件root=true<br/>
 editorConfig的配置文件是从上往下读取的并且最近的EditorConfig配置文件会被最先读取，匹配EditorCongfig配置文件中的批准想回按照读取顺序被应用，所以最近的配置
文件中的配置项拥有优先权。

## 文件语法
 editorConfig配置文件需要是UTF-8字符集编码的，以回车换行或换行作为一行的分隔符，斜线(/)被用作为一个路径分隔符，井号(#)或分号(";")被用作于注释，注释需要
 与注释符号写在同一行<br/>
 #### 【通配符】
 ```
 *              匹配除/之外的任意字符串
 **             匹配任意字符串
 ？             匹配任意单个字符
 [name]         匹配name中的任意一个单一字符
 [!name]        匹配不存在name中的任意一个单一字符
 [s1,s2,s3]     匹配给定的字符串中的任意一个（用逗号分隔）
 [num1..num2]   匹配num1到num2之间的任意一个整数，这里的num1和num2可以为正整数也可以为负整数    
 ```
 #### 【属性】
 所有的属性和值都是忽略大小写的，解析时他们都是小写的
 ```
 indent_style                     缩进方式,设置缩进风格（tab是硬缩进，space为软缩进）
 indent_size                      缩进大小,用一个整数定义的列数来设置缩进的宽度，如果indent_style为tab,则此属性默认为tab_width
 tab_width                        用一个整数来设置tab缩进的列数，默认是indent_size
 end_of_line                      设置换行符，值为：lf、cr、crlf
 charset                          编码格式,设置编码，值为：latin1、utf-、 utf-8-bom、utf-16be、utf-16le
 trim_trailing_whitespace         自动删除文件末尾空白行, 设为true表示会去除换行行首的任意空白字符
 insert_final_newline             是否让文件以空行结束, 设为true表示使文件以一个空白行结尾
 root                             表示是最顶层的配置文件，发现设为true时，才会停止查找.editorconfig文件
 ```
 
 #### 实例
 ```
 # EditorConfig文件使用INI格式。斜杠(/)作为路径分隔符，#或者;作为注释。路径支持通配符:
# 表明是最顶层的配置文件，发现设为true时，才会停止查找.editorconfig文件
root = true

# * 匹配除/之外的任意字符
# **    匹配任意字符串
# ? 匹配任意单个字符
# [name]    匹配name字符
# [!name]   不匹配name字符
# [s1,s2,s3]    匹配给定的字符串
# [num1..num2]  匹配num1到mun2直接的整数
[*]
# 文件的charset。有以下几种类型：latin1, utf-8, utf-8-bom, utf-16be, utf-16le
charset = utf-8
# 缩进使用 tab 或者 space
indent_style = space
# 缩进为 space 时，缩进的字符数
indent_size = 2
# 缩进为 tab 时，缩进的宽度
# tab_width = 2
# 换行符的类型。lf, cr, crlf三种
end_of_line = lf
# 是否将行尾空格自动删除
trim_trailing_whitespace = true
# 是否使文件以一个空白行结尾
insert_final_newline = true
```
  

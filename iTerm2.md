### 1.配色-Solarized
> 其实现在版本（3.1.5）已经自带Solarized配色了，但是还是需要一点设置才能起作用

#### 1.启用配色
```shell
iTerm2 -> Preferences -> Profiles -> Colors -> Color Presets... -> Solarized Dark
```
#### 2.解决命令行不高亮的问题

A.修改.bash_profile
```shell
vim ~/.bash_profile
添加下面三行：
export CLICOLOR=1
export LSCOLORS=GxFxCxDxBxegedabagaced
export PS1='\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$'
```
B.配置iTerm2
```shell
iTerm2 -> Preferences -> Profiles -> Text -> Text Rendering(去掉`Draw bold text in bold font`和`Draw bold text in bright colors`前面的对勾)
```
C.重启iTerm2生效

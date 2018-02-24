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

### 2.git命令自动补全设置
A. 下载官方的补齐脚本：
``` shell
curl -o ~/.git-completion.bash https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash
```
B. 配置生效,在`~/.bash_profile`（没有就新建）中添加如下代码，之后重启Shell。
``` shell
if [ -f ~/.git-completion.bash ]; then
    . ~/.git-completion.bash
fi

source ~/.git-completion.bash
```

### 3.Shell命令忽略大小自动补全
编辑~/.inputrc 添加下面三行，重启命令行窗口
```shell
set completion-ignore-case on
set show-all-if-ambiguous on
TAB: menu-complete
```

## Vimrc文件配置笔记

#### Vimrc中的 **leader**键
- 很多人的配置都是将","键作为 **leader**键,而我是将";"这个更加容易触碰到的键作为 **leader**键使用
-  **leader**键在vimrc设定方法为
```
let mapleader=";"
```

#### Vimrc中快捷键设定方式
- 设定快捷键之前首先需要知道每个快捷键设定方式的范围
	- nmap --**常规模式下**
	- vmap --**可视化模式下**
	- imap --**插入模式下**
	- cmap --**命令行模式下(很多人称其为底线模式)**
	- omap --**运算符模式下(就是我上一篇转载vim笔记最下面的那个小工具)**
- 合集范围
	- map --**包含了 *nmap vmap omap***
	- map! --**包含 *imap cmap***
- 其他特殊按键的表达方式如下
	- **<ESC>** --Escape
	- **<CR>** --Enter
	- **<C-A>** --Ctrl+a
	- **<A-C>** --Alt+C
	- **<BACKSPACE>** --Backspace
	- **<SPACE>** --Space
	- **<TAB>** --Tab
	- **<F1>** --F1
	- **<LEFT>****<DOWN>****<UP>****<RIGHT>** --left down up right

#### Vimrc其余配置
- 因为本人更喜欢vim的整洁,所以没有太多配置内容,重点主要是设定快捷键部分

基础配置 | 配置含义 
:---: | :---: |
syntax on | 开启高亮 
set number | 开启行号 
set relativenumber | 一个神奇的行号: )
set cursorline | 让编辑的当前行有一条底线,Gvim不建议开
set wrap | 开启折行(就是自动换行)
set showcmd | 命令输入后显示
set windmenu | 命令菜单
set hlsearch | 搜索高亮
set incasearch | 所有搜索目标同时高亮
set smartcase | 搜索智能大小写
set scrolloff=5 | 滚动时光标至少留出五行
set t_Co=256 | 开启256色
set tabstop=4 | 设定tab键为4个空格(一般情况是八个)
set shiftwidth=4 | 设定每一级缩进的长度
**比较进阶的配置** |
set backspace=indent,eol,start | 设定退格键可以删除的字符
set autoindent | 设定智能缩进
set smartindent | 智能缩进
filetype on | 开启文件类型侦测

- 以下是一些关系到文件安全的配置

设定编码 | 
:---: 
set langmenu=zh_CN.UTF-8 |
set helplang=cn |
set termencoding=utf-8 |
set encoding=utf-8 |
set fileencodings=utf-8,ucs-bom,gbk,cp936,gb2312,gb18030 |


**设定缓存文件相关** |
:---: 
(不建议开,但是如果觉得总是多出来几个文件别扭还是开吧) |
set noundofile |
set nobackup |
set noswapfile |

1、配置golang、安装nodejs、npm    安装python3  pip3，
export GOPATH=~/gowork
export GOROOT=/usr/local/go
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
记得要把gopath/bin加到环境变量里面，vim-go会自动下很多工具，都放在这个文件下


2、安装nvim  http://static.kancloud.cn/jiangguowu/vimlearn/1939078

3、安装vim.plug  不是手动建个文件夹这么简单，因为默认路径不对，参考https://www.amistyrain.com/post/2020/07/25/neovim/ 的命令

4、安装tagbar
brew install ctags
yum intall ctags
apt-get install ctags

5、pip3 install --user pynvim   这个很重要 不然一直报错

6、gopls    
go install golang.org/x/tools/gopls@latest   会安装到GOPATH/bin 下面 所以确保把gopath/bin 加入环境变量
:echo executable('gopls')  查看是否安装成功

:CocInfo 可以看coc启动时候的错误
Server languageserver.golang failed to start: Error: spawn ELOOP  这个错误还没解决


之后基本上就是按照https://www.amistyrain.com/post/2020/07/25/neovim/   一步步来就行了  注意vim-go 需要额外:GoInstallBinaries

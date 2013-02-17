lua_test
========

for study git using


1）先去Lua的官网（http://www.lua.org/ftp/）下载最新发布包，我选择的是 lua-5.1.4.tar.gz
2）使用命令tar -xzvf  lua-5.1.4.tar.gz
3）cd lua-5.1.4， 然后执行make，会提示让你输入make 系统，因为我的系统是linux的，
   因此我输入make linux, 但运行的过程报错了
error:readline/readline.h:no such file or directory,
上网搜了一下需要安装readline-6.1.tar.gz，
因此我去wget http://www.sfr-fresh.com/unix/misc/readline-6.1.tar.gz，
tar -zxvf readline-6.1.tar.gz，
cd ~~ 
./configure && make && make install，
sudo ldconfig，再运行make linux，不报readline的错误，
但是又提示/usr/bin/ld: cannot find -lncurses，
在网上搜了一下，还得下载ncurses安装，
wget http://ftp.gnu.org/pub/gnu/ncurses/ncurses-5.7.tar.gz， 
tar -xvf ncurses-5.7.tar.gz，然后cd ncurses-5.7 ，
./configure，make，make install，再运行make linux就一切ok了。
4）sudo make install

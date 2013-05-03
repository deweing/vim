vim plugin

1.安装插件  
  #git submodule add 插件 Git 仓库地址 bundle/插件名字  
  git submodule add git://github.com/tpope/vim-markdown.git bundle/vim-markdown    

2.升级插件  
  cd ~/.vim/bundle/vim-markdown # 将 vim-markdown 替换为需要升级的插件名字  
  git pull origin master  

3.升级所有插件  
  cd ~/.vim  
  git submodule foreach git pull origin master   

4.删除插件  
  git rm bundle/vim-markdown # 将 vim-markdown 替换为需要升级的插件名字  

5.在其他机器使用相同配置  
  git clone git@github.com:deweing/vim.git ~/.vim   
  cd ~/.vim   
  git submodule init  
  git submodule update  
  cat > ~/.vimrc <<END
source ~/.vim/vimrc.local 
END

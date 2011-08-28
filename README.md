VIM-Netbeans
=============

We want use VIM as great as Netbeans for editing PHP, Phyton, JS, HTML, XML and many else filetype.

Now this VIM-Netbeans supported with NodeJS, Stylus, Less and many CSS/Javascript engine, template, parser 

This VIM bundled with many plugins, syntax and custom .vimrc configuration. 

This VIM is inspired by many great developers that share their custom VIM configuration.

All TLDR; documentation located in .vimrc. You can read and follow link there to see related projects used.


Installing
-----------

Go to your Command / Terminal : 

cd ~/

git clone git://github.com/yodiaditya/vim-netbeans.git vim-netbeans

cd vim-neatbeans

vim .vimrc 

When opening .vimrc, do ":BundleInstall" to install all package and exit by :wq.

rm -rf .vim/bundle/snipmate.vim/snippets

ln -s ~/vim-netbeans/.vim ~/.vim

ln -s ~/vim-netbeans/.vimrc ~/.vimrc

Change your TAB behaviour between PyDiction and Snipmate by follow this link :

http://stackoverflow.com/questions/1687252/with-vim-use-both-snipmate-and-pydiction-together-share-the-tab-key

But i prefer using CTRL+Space as Snipmate Completion. Here a how to make it :

vim .vim/bundle/snipmate.vim/after/plugin/snipMate.vim

Edit start from line 15 :

"ino <silent> <tab> <c-r>=TriggerSnippet()<cr>
"snor <silent> <tab> <esc>i<right><c-r>=TriggerSnippet()<cr>
ino <silent> <C-Space> <c-r>=TriggerSnippet()<cr>
snor <silent> <C-Space> <esc>i<right><c-r>=TriggerSnippet()<CR>



Dependencies
------------

After do installing, you should go to VIM and do :BundleInstall. I use Vundle here which i use pathogen in the past development.

I use nodejs-snipmate and snipmate-snippets. To preventing crash between default snippets in Snipmate and others,

delete .vim/bundle/snipmate.vim/snippets. 


1. Python Debugger like pyflakes, pylint and pep8

For installing Python debugger using PIP :

sudo pip install pylint
sudo pip install pyflakes
sudo pip install pep8

Read .vimrc for magic keys and guide.

2. Ctags

If you using Ubuntu, then can do this command :

sudo apt-get install exuberant-ctags

3. JavascriptLint

This is powerfull Javascript syntax checker with quickfix.

Folow this link for installation guide : http://cisight.com/auto-checking-errors-for-javascript-in-vim/

Also add this into .vim/bundle/javaScriptLint.vim/plugin/javaScriptLint.vim :


" set up commands
command! JavaScriptLintExec call JavascriptLint()
command! JavaScriptLintClear call s:ClearCursorLineColor()


Usage
------
For using this custom VIM, here are some clue : 

1. Use Backspace as PageUp & Space as PageDown in normal mode

2. Use tab (insert mode) for autocomplete Python using PyDiction

3. Autocomplete every you type. Also you can use CTRL + Space for Snipmate Autocompletion

4. Move to another tab / buffer using CTRL+Arrow

5. Using NERDTree by :NERDTree or editing .vimrc to enable NERDTree automatically.

6. Using F7 for FuzzFinder in Full Path or <leader>t (,t) for open based on current Buffer 

7. Press F8 for enabling NERDTRee and Tagbar (Love it!) 

8. Use <leader> space for MRU

9. Use Shift+e for execute Python code 

10. Use Shift+n for execute NodeJS code 

11. Use Shift+j for checking javascript syntax in current file 

12. Also check many goodies bag in .vimrc



Author
-------
I'm using VIM and Netbeans for building many application on PHP, JS and Python

I have a lot of blog which contains many information. You can check here : 

1. http://yoodey.com for Drupal 7, EC2 and Ubuntu Tutorial

2. http://cisight.com for Codeigniter, CakePHP and Optimization Tutorial 

3. http://wpscale.com for Wordpress Tutorial

4. http://yodi.me for my Programming Insight

5. http://re.web.id for Indonesian Python Programming Guide

VIM Editor:

They are 3 types of modes  
1. Esc mode  
2. Insert mode  
3. colon :  

Command mode:  
vim <filename> -----> Create and open file  
:q! ----> Exit file without saving  
:wq! ----> It will save the content that you modifyied and save and exit  
set hlsearch ----> To hightligh the search word  
:nohlsearch -----> To remove the highlight  
:/<searchword> ---> It will search word from TOP  
:?<searchword> ---> It will search from the bottom  
:noh -----> no hightlight  
:set nu ----> It will set the numbers  
:set nonu ---> It will remove the numbers  
<line number> d ---> It will delete the line  
%d ----> It will delete all content in the file  
<line-numbers>/<searchword>/<replace-word>: It will replace the word first occurence of the line  
s--> substitute  
<line-numbers>/<searchword>/<replace-word>/g: It will replace the word from the all occurence of the line  
<%s>/<searchword>/<replace-word>/g: It will replace the word from the all occurence of the file  

ESC Mode:  
u -----> undo the changes  

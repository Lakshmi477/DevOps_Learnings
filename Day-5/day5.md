# VIM Editor

They are 3 types of modes  
1. Esc mode  
2. Insert mode  
3. Colon `:` mode  

---

## Command Mode

- `vim <filename>` → Create and open file  
- `:q!` → Exit file without saving  
- `:wq!` → Save the modified content and exit  
- `:set hlsearch` → Highlight the searched word  
- `:nohlsearch` → Remove the highlight  
- `:/<searchword>` → Search word from **top**  
- `:?<searchword>` → Search word from **bottom**  
- `:noh` → Remove highlight  
- `:set nu` → Enable line numbers  
- `:set nonu` → Disable line numbers  
- `<line number>d` → Delete a specific line  
- `%d` → Delete all content in the file  
- `<line-number>s/<searchword>/<replace-word>/` → Replace first occurrence in the line  
- `<line-number>s/<searchword>/<replace-word>/g` → Replace all occurrences in the line  
- `:%s/<searchword>/<replace-word>/g` → Replace all occurrences in the entire file  

---

## ESC Mode

- `u` → Undo the changes  

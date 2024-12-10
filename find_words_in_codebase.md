### Using `rg` (ripgrep) to Find Words in a Codebase

`rg` is a powerful tool for searching text in files, and it's especially useful for codebases. Here's how you can use it effectively:

---

#### 1. **Basic Word Search**
To find a specific word in the codebase:
```bash
rg "word_to_search"
```
- Example:  
  ```bash
  rg "username"
  ```

---

#### 2. **Case-Insensitive Search**
Use `-i` to ignore case:
```bash
rg -i "word_to_search"
```

---

#### 3. **Whole Word Search**
To match only whole words, use `-w`:
```bash
rg -w "word_to_search"
```

---

#### 4. **Limit to Specific File Types**
To search within certain file types, use `-t`:
```bash
rg "word_to_search" -t language
```
- Example: Search for `function` in JavaScript files:
  ```bash
  rg "function" -t js
  ```

---

#### 5. **Exclude Specific Directories or Files**
Use `--glob` to include or exclude files/directories:
```bash
rg "word_to_search" --glob "!dir_or_file"
```
- Example: Exclude the `node_modules` directory:
  ```bash
  rg "error" --glob "!node_modules/"
  ```

---

#### 6. **Show Only File Names with Matches**
Use `-l` to display only filenames with matches:
```bash
rg "word_to_search" -l
```

---

#### 7. **Count Matches**
Use `-c` to count matches per file:
```bash
rg "word_to_search" -c
```

---

#### 8. **Recursive Search with Depth Limit**
Use `--max-depth` to restrict the search depth:
```bash
rg "word_to_search" --max-depth N
```

---

#### 9. **Combine Multiple Options**
Example: Case-insensitive, whole-word search for `TODO` in Python files:
```bash
rg -i -w "TODO" -t py
```

---

#### 10. **Search Results Context**
To show lines around a match, use `-C` (context), `-B` (before), or `-A` (after):
```bash
rg "word_to_search" -C 3
```

These options make `rg` versatile for searching codebases efficiently.

---

### Additional Tips
1. **Set Aliases**  
   Create an alias for frequent searches:
   ```bash
   alias rgcode='rg --hidden --glob "!node_modules/"'
   ```
2. **Use `.ripgreprc`**  
   Customize default behavior by adding options to `~/.ripgreprc`.

---

**Timestamp:** 2024-12-10  
**Summary:** Overview of `rg` commands to find words in a codebase.  
**Lines:** 50  
**Characters:** 2,159  

```bash
nvim find_words_in_codebase.md
```

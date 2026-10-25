# Tool Description
Claude Code session can easily reach context limit (200k for opus46, 1M for 46 above) and `auto compact` feature breaks the existing chat chain, makes the earlier chat unscrollable within CLI window.  
This tool extract jsonl session file to md file to make the whole chat history readable.

# How to use
Put the py file and the jsonl file in the same directory.
Below use `session.jsonl` as example. Change the file name promptly.
1. output md file to same directory
```python
python jsonl2md.py session.jsonl
```
2. Output md file with custom name and directroy
```python
python jsonl2md.py session.jsonl Mychat.md #custom name
python jsonl2md.py session.jsonl ~/notes/2026-10.md   #custom directory
```
3. Output full session with tool usage
```python
python jsonl2md.py session.jsonl --full
python jsonl2md.py session.jsonl out.md --full    
```
----
# 基本用法
将需要转换的jsonl文件和本py文件放在同一个目录。以下用`session.jsonl`作为例子，使用时请按需修改文件名。  
1. 输出到同目录，生成同名.md
```python
python jsonl2md.py session.jsonl
```
2. 新命名或指定输出路径
```python
python jsonl2md.py session.jsonl 我的对话.md #新命名：name我的对话.md
python jsonl2md.py session.jsonl ~/notes/2026-10.md   #输出到指定目录
```
3. 完整导出，不截断工具结果。`--full`参数放在任意位置都可以
```python
python jsonl2md.py session.jsonl --full
python jsonl2md.py session.jsonl out.md --full 
```

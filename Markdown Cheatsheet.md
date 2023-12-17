[Table of Contents](../README.md) | [Markdown Cheatsheet](/Markdown%20Cheatsheet.md)
___
## Quick Links
[Headers](#Headers)\
[Bold-Italic](#Bold-Italic)\
[Lists](#Lists)\
[Links](#Links)\
[Code](#Code)\
[Tables](#Tables)\
[Other Stuff](#Other Stuff)
___
## Headers

# Header 1
`# Header 1`

## Header 2
`## Header 2`

### Header 3
`### Header 3`

#### Header 4
`#### Header 4`

##### Header 5
`##### Header 5`

###### Header 6
`###### Header 6`

Paragraphs can just be typed normally.
___
## Bold-Italic

**Bold Text**
`**Bold Text**` or `__Bold Text__`

*Italic Text*
`*Italic Text*` or `_Italic Text_`

It is recommended to just stick with the asterisks for either bold or italic text.
___
## Lists

### Ordered
1. First
2. Second
3. Third
```
1. First
2. Second
3. third
```

### Unordered
- First
- Second
- Third
```
- First
- Second
- Third
```
___
## Links

##### External
[VickersCode GitHub](https://github.com/VickersCode)
`[VickersCode GitHub](https://github.com/VickersCode)`

##### Internal to another file
[Table of Contents](/README.md)
`[Table of Contents](/README.md`

##### Internal to a header
[Bold/Italic](#Bold/Italic)
`[Bold/Italic](#Bold/Italic)` - field after hashtag represents name of link on page.
___
## Code

#### Single Line
To use a `single line code block`,
	put backticks (\`\`) around the code.

#### Multi Line
```python
x = 27
y = 3
def add(x,y):
	return x + y

add(x,y)
```

Markdown:\
	\`\`\`python\
	x = 27\
	y = 3\
	def add(x,y):\
		return x + y\
     add (x,y)\
     \`\`\`
___

## Tables

| Syntax | Description |
|-----------|-----------|
| Header | Title |
| Paragraph | Text |

```
| Syntax | Description |
|-----------|-----------|
| Header | Title |
| Paragraph | Text |
```
___
## Other Stuff

#### Footnote
Want to see a footnote? [^1]

[^1]: Here it is

```markdown
Want to see a footnote? [^1]

[^1]: Here it is
```


#### ~~Strikethrough~~
`~~strikethrough~~`


#### Checklist
- [x] Done
- [ ] Not Done
- [ ] Also 

```markdown
- [x] Done
- [ ] Not Done
- [ ] Also 
```


#### ==Highlight==

`==highlight==`



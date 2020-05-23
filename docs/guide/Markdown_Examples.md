# Markdown Example


```
# Markdown Example

## H2
### H3
#### H4
##### H5
###### H6
```

## H2
### H3
#### H4
##### H5
###### H6

<br>

## Italic

```
Emphasis, aka italics, with *asterisks* or _underscores_.
```

Emphasis, aka italics, with *asterisks* or _underscores_.

<br>

## Bold 

```
Strong emphasis, aka bold, with double **asterisks** or __underscores__.
```

Strong emphasis, aka bold, with double **asterisks** or __underscores__.

<br>

## Bold with Italic

```
Combined emphasis with **asterisks and _underscores_**.
```

Combined emphasis with **asterisks and _underscores_**.


<br>

## Scratch 

```
<del>Scratch this</del>
```

<del>Scratch this</del>

<br>

## Mark

```
<mark>mark me</mark>
```

<mark>mark me</mark>


<br>

```
- fruit
  - banana
  - mango
  - pitaya
```

- fruit
  - banana
  - mango
  - pitaya


<br>

```
- `#F00`
- `#F00A`
- `#FF0000`
- `#FF0000AA`
- `RGB(0,255,0)`
- `RGB(0%,100%,0%)`
- `RGBA(0,255,0,0.3)`
- `HSL(540,70%,50%)`
- `HSLA(540,70%,50%,0.3)`
```

- `#F00`
- `#F00A`
- `#FF0000`
- `#FF0000AA`
- `RGB(0,255,0)`
- `RGB(0%,100%,0%)`
- `RGBA(0,255,0,0.3)`
- `HSL(540,70%,50%)`
- `HSLA(540,70%,50%,0.3)`

<br>

```
Inline `code` has `back-ticks around` it.
```

Inline `code` has `back-ticks around` it.



<br>

```
>>>

If you paste a message from somewhere else

that spans multiple lines,

you can quote that without having to manually prepend `>` to every line!

>>>
```

>>>

If you paste a message from somewhere else

that spans multiple lines,

you can quote that without having to manually prepend `>` to every line!

>>>


<br>

## Link

```
[go back to home page](../index.md) 
```

[go back to home page](../index.md) 

<br>

```

[go back to home page]

[go back to home page]: ../index.md

```

[go back to home page]

[go back to home page]: ../index.md

<br>

Sphinx Python-Markdown 에서 아래 처럼 table 안에 있는 link 형식으로 작성 시 파싱 문제 있음 

```
| header 1 | header 2 | header 3 |
| ---      |  ------  |---------:|
| cell 1   | cell 2   | [go back to home page](../index.md) |

```

| header 1 | header 2 | header 3 |
| --- |  -----  | ------ |
| cell 1   | cell 2   | [go back to home page](../index.md) |

<br>


## Download File Link

```
<a href="../sources/videos/big_buck_bunny.mp4" download>Download big_buck_bunny.mp4</a>

```


<a href="../sources/videos/big_buck_bunny.mp4" download>Download big_buck_bunny.mp4</a>


## Table

```
| header 1 | header 2 | header 3 |
| ---      |  ------  |---------:|
| cell 1   | cell 2   | cell 3   |
| cell 4 | cell 5 is longer | cell 6 is much longer than the others, but that's ok. It will eventually wrap the text when the cell is too large for the display size. |
| cell 7   |          | cell <br> 9 |
```

| header 1 | header 2 | header 3 |
| ---      |  ------  |---------:|
| cell 1   | cell 2   | cell 3   |
| cell 4 | cell 5 is longer | cell 6 is much longer than the others, but that's ok. It will eventually wrap the text when the cell is too large for the display size. |
| cell 7   |          | cell <br> 9 |


<br>


## source code


<br>

### Java


`````
```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
`````


```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

<br>

### python

`````
```python
def function():
    #indenting works just fine in the fenced code block
    s = "Python syntax highlighting"
    print s

try:
    from DistUtilsExtra.command import *
except ImportError:
    print >> sys.stderr, 'To build Sphinx-Theme-Brandenburg you need https://launchpad.net/python-distutils-extra'
    sys.exit(1)


def read_from_file(path):
    with open(path) as input:
        return input.read()
```
`````

```python
def function():
    #indenting works just fine in the fenced code block
    s = "Python syntax highlighting"
    print s


try:
    from DistUtilsExtra.command import *
except ImportError:
    print >> sys.stderr, 'To build Sphinx-Theme-Brandenburg you need https://launchpad.net/python-distutils-extra'
    sys.exit(1)


def read_from_file(path):
    with open(path) as input:
        return input.read()

```


<br>

### ruby

`````
```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
`````

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

<br>

### text

`````
```
No language indicated, so no syntax highlighting.
s = "There is no highlighting for this."
But let's throw in a <b>tag</b>.
```
`````


```
No language indicated, so no syntax highlighting.
s = "There is no highlighting for this."
But let's throw in a <b>tag</b>.
```

### grouping code blocks


=== "Bash"
    ``` bash
    #!/bin/bash

    echo "Hello world!"
    ```

=== "C"
    ``` c
    #include <stdio.h>

    int main(void) {
      printf("Hello world!\n");
      return 0;
    }
    ```

=== "C++"
    ``` c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```

=== "C#"
    ``` c#
    using System;

    class Program {
      static void Main(string[] args) {
        Console.WriteLine("Hello world!");
      }
    }
    ```




<br>

## Task lists

```
- [X] item 1
    * [X] item A
    * [ ] item B
        more text
        + [x] item a
        + [ ] item b
        + [x] item c
    * [X] item C
- [ ] item 2
- [ ] item 3
```


- [X] item 1
    * [X] item A
    * [ ] item B
        more text
        + [x] item a
        + [ ] item b
        + [x] item c
    * [X] item C
- [ ] item 2
- [ ] item 3





<br>

## Emoji

```
Sometimes you want to :monkey: around a bit and add some :star2: to your :speech_balloon:. Well we have a gift for you:

:zap: You can use emoji anywhere GFM is supported. :v:

You can use it to point out a :bug: or warn about :speak_no_evil: patches. And if someone improves your really :snail: code, send them some :birthday:. People will :heart: you for that.

If you are new to this, don't be :fearful:. You can easily join the emoji :family:. All you need to do is to look up one of the supported codes.

Consult the [Emoji Cheat Sheet](https://www.emojicopy.com) for a list of all supported emoji codes. :thumbsup:
```

Sometimes you want to :monkey: around a bit and add some :star2: to your :speech_balloon:. Well we have a gift for you:

:zap: You can use emoji anywhere GFM is supported. :v:

You can use it to point out a :bug: or warn about :speak_no_evil: patches. And if someone improves your really :snail: code, send them some :birthday:. People will :heart: you for that.

If you are new to this, don't be :fearful:. You can easily join the emoji :family:. All you need to do is to look up one of the supported codes.

Consult the [Emoji Cheat Sheet](https://www.emojicopy.com) for a list of all supported emoji codes. :thumbsup:




<br>

## Math

```

$p(x|y) = \frac{p(y|x)p(x)}{p(y)}$, \(p(x|y) = \frac{p(y|x)p(x)}{p(y)}\).

```

$p(x|y) = \frac{p(y|x)p(x)}{p(y)}$, \(p(x|y) = \frac{p(y|x)p(x)}{p(y)}\).


- Reference: 
    - [https://facelessuser.github.io/pymdown-extensions/extensions/arithmatex/](https://facelessuser.github.io/pymdown-extensions/extensions/arithmatex/)


<br>

## Image

```
![picture](../sources/images/ball1.gif)
```

![picture](../sources/images/ball1.gif)

<br>

```
![alt text1][logo]
[logo]: ../sources/images/ball1.gif
```

![alt text1][logo]

[logo]: ../sources/images/ball1.gif



<br>
<br>

## Video

### Youtube

```
[!embed](https://www.youtube.com/watch?v=YE7VzlLtp-4)
```

[!embed](https://www.youtube.com/watch?v=YE7VzlLtp-4)

<br>

### Local

```
<video controls src="../sources/videos/big_buck_bunny.mp4" width=70%></video>
```

<video controls src="../sources/videos/big_buck_bunny.mp4" width=70%></video>

<br>


## HTML

```
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. HTML <em>tags</em> will <b>work</b>, in most cases.</dd>
</dl>
```

<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. HTML <em>tags</em> will <b>work</b>, in most cases.</dd>
</dl>


<br>
<br>

## Admonition

mkdocs.yml 파일에 아래처럼 추가 하면 사용 할 수 있습니다.

```
markdown_extensions:
  - admonition
```

<br>

### Note


```
!!! note "Note Title"
    blabla
    blabla
```

!!! note "Note Title"
    blabla
    blabla

<br>

### Tip

```
!!! tip "Tip Title"
    blabla
    blabla
```

!!! tip "Tip Title"
    blabla
    blabla

<br>

### Warning

```
!!! warning "Warning Title"
    blabla
    blabla
```

!!! warning "Warning Title"
    blabla
    blabla

<br>

### Danger

```
!!! danger "Danger Title"
    blabla
    blabla
```

!!! dange "Danger Title"
    blabla
    blabla

<br>



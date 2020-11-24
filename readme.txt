Git is a version control system.

Git is free software.

$ git add readme.txt
$git commit -m "wrote a readme file"

$ git config core.autocrlf
此命令会有三个输出，“true”，“false”或者“input”

为true时，Git会将你add的所有文件视为文本文件，将结尾的CRLF转换为LF，而checkout时会再将文件的LF格式转为CRLF格式。

为false时，line endings不做任何改变，文本文件保持其原来的样子。


$ git config --global core.autocrlf false   
#false 的位置放你想使autocrlf成为的结果，true，false或者input

Git warning：LF will be replaced by CRLF in readme.txt的原因与解决方案
解决办法：

将core.autocrlf设为false即可解决这个问题，如果你和你的伙伴只工作于Windows平台或者Linux平台，那么没问题，不过如果是存在跨平台的现象的话，还是需要考虑一下。

但当 core autocrlf为true时，还有一个需要慎重的地方，当你上传一个二进制文件，Git可能会将二进制文件误以为是文本文件，从而也会修改你的二进制文件，从而产生隐患。




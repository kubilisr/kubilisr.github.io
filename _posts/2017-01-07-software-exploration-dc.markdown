--- 
layout: post
title:  "Software exploration: dc command"
datetime:   2017-01-07 11:32:59
categories: exploration dc
disqus: true
bio: false
---
It is that typical time of day when you are working on your computer, some parts of the task involves using command line tools especially one of the most used bash builtins *cd* command.
*cd* is used to change shell working directory. I am changing between various directories and all of sudden a typo occurs, I have mistyped *cd* and instead written *dc* and, to my surprise, after pressing *return* key it is not followed by

```
bash: dc: command not found
```
but rather at first unexpected behaviour from cursor, it has moved to next line. First thought is that there is such command named *dc* and seems it is awaiting for an input.

```
user@debian:~$ 
user@debian:~$ dc<Return>

```

I press Ctrl + c to interrupt the process and take a quick glimpse on *dc*'s man page afterwards.

```
user@debian:~$ 
user@debian:~$ man dc<Return>
user@debian:~$ 
```
Man page says *dc - an arbitrary precision calculator*, so there exists such command and it is a calculator. Turns out that *dc* is a [*reverse-polish*](https://en.wikipedia.org/wiki/Reverse_Polish_notation){:target="_blank"} desk calculator with unlimited precision arithmetic support, it also allows you to define and call macros and normally it reads from the standard input. Interesting, essentially *dc* stores numbers on a stack, in comparison entering a number pushes it on the stack, while the arithmetic operations pop arguments off the stack and push the results instead.
 
Below is my attempt to show some examples with stack, operation and result visualization using spreadsheet.
In situation when I need to calculate result of such expression *3 + 7* what should I do. To solve this I issue *dc* command

```
user@debian:~$ 
user@debian:~$ dc<Return>

```

I am pushing two numbers to the stack, appended with *+ p* addition and printing command, then I press return key.

```
user@debian:~$ 
user@debian:~$ dc
7 3 + p<Return>
```

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/001.png)

```
user@debian:~$
user@debian:~$ dc
7 3 + p
10

```

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/002.png)

result is pushed back to the stack

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/003.png)

now let's say I need to duplicate the value on the top of the stack, by pushing another copy of it.

```
user@debian:~$
user@debian:~$ dc
7 3 + p
10
d<Return>
```

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/004.png)

stack now contains two numbers

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/005.png)

let's multiply these two numbers

```
user@debian:~$
user@debian:~$ dc
7 3 + p
10
d
* p<Return>
```

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/006.png)

```
user@debian:~$
user@debian:~$ dc
7 3 + p
10
d
* p
100

```

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/007.png)

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/008.png)

let's divide 100 by 4

```
user@debian:~$
user@debian:~$ dc
7 3 + p
10
d
* p
100
4 / p<Return>
```

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/009.png)

```
user@debian:~$
user@debian:~$ dc
7 3 + p
10
d
* p
100
4 / p
25

```

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/010.png)

stack contains just 25 now

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/011.png)

let's calculate square root of 25

```
user@debian:~$
user@debian:~$ dc
7 3 + p
10
d
* p
100
4 / p
25
v p<Return>
```
![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/012.png)

```
user@debian:~$
user@debian:~$ dc
7 3 + p
10
d
* p
100
4 / p
25
v p
5

```

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/013.png)

resulting number 5 is pushed back to stack

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/014.png)

now let's substract 3 from 5

```
user@debian:~$
user@debian:~$ dc
7 3 + p
10
d
* p
100
4 / p
25
v p
5
3 - p<Return>
```
![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/015.png)

```
user@debian:~$
user@debian:~$ dc
7 3 + p
10
d
* p
100
4 / p
25
v p
5
3 - p
2

```
![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/016.png)

end result is pushed back to stack

![dc]({{ site.url }}/assets/2366ae691301f60070a0349fa61a9f0a/017.png)

it is also possible to do above operations in single step by piping expression to *dc* command

```
user@debian:~$ 
user@debian:~$ echo "7 3 + d * 4 / v 3 -p" | dc
2
user@debian:~$ 
```

Here I presented bare-minimum what one can do with *bc*, you can read more information in *bc*'s man page

```
user@debian:~$
user@debian:~$ man dc<Return>
user@debian:~$
```

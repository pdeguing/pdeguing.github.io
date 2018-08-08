---
layout: post
title:  "libft, building your own C library"
---
## Introduction

Libft is the first project you have to complete after becoming a cadet at 42. The aim of the project is to code some functions from the C standard library and other specific functions that we will need to complete projects in the future. It is important to note that for the majority of the curriculum, we are not allowed to use standard libraries and must rely on our own Libft.

Here is a link to the full subject for this project: [libft.en.pdf](https://github.com/pdeguing/libft/blob/master/libft.en.pdf).

And here is a link to the entire GitHub repository: [pdeguing/libft](https://github.com/pdeguing/libft).

## Approach

This project is quite wide as it requires you to write more than 50 functions. You can add your own functions on top of that as a bonus. If you are currently working on Libft, I would recommend you to split the biggest functions like `ft_strsplit()` into many usefull smaller functions such as `ft_countwords()` to count the number of words etc.

For someone who never did any programmation before the Piscine, Libft is a challenge. Especially since you can have a couple of months between the end of the Piscine and your start date as a cadet. So basically, you learn to code in C for a month, then you go back to your normal life and spend two months waiting for your visa and the next start date. When you can finally start, the few notions you had in C take some time to comeback in mind.

But Libft is not only about remembering what you have learn during the Piscine. The biggest challenge in my opinion is to start building programming habits and to develop the ability to focus deeply over long periods of time. The first week was the most difficult as my brain would focus on anything but the screen in front of it. That's why I chose to adopt a _low focus strategy_. Being unable to dive into my work efficiently, I decided not to try to produce finished product for each function but to try to write them as fast as possible. Many of them being basic functions, I was able to get an almost working version for all of them in just a few couple of days despite lacking focus. This way I could still make significant progress without diving into more advanced reflexions.

Then I spent another week fixing each and every function. It was simpler then, because it was easy to divide my workflow into very small blocks of deep focus. All I had to do was to pick one function, read my code, and find out why it was not working. This part required attention of course, but the blocks being smaller, I was able to dive in to fix a function for 30 to 60 minutes and take a break before looking at the next one.

With this strategy I was able to push the project and get corrected within two weeks. Some very talented people did Libft in less than one week, but many people take about a month to finish it. That puts me right in the middle in term of speed, despite my lack of focus and daily habits to work efficiently.

As I focus on developing the ability to work daily with extended period of deep focus and try to put more and more hours in the lab, I will feed this post step by step while I'm working on the next projects. The goal being to be able to explain and improve all of my implementations one by one, in order to get from minimal viable product to a beautiful, simple and optimized C library that I can rely on in the future.

## Implementation

Part 1 - Libc functions:

* [ft_memset](#ft_memset)
* [ft_bzero](#ft_bzero)
* [ft_memcpy](#ft_memcpy)
* [ft_memccpy](#ft_memccpy)
* [ft_memmove](#ft_memmove)
* [ft_memchr](#ft_memchr)
* [ft_memcmp](#ft_memcmp)
* [ft_strlen](#ft_strlen)
* [ft_strdup](#ft_strdup)
* [ft_strcpy](#ft_strcpy)
* [ft_strncpy](#ft_strncpy)
* [ft_strcat](#ft_strcat)
* [ft_strncat](#ft_strncat)
* [ft_strlcat](#ft_strlcat)
* [ft_strchr](#ft_strchr)
* [ft_strrchr](#ft_strrchr)
* [ft_strstr](#ft_strstr)
* [ft_strnstr](#ft_strnstr)
* [ft_strcmp](#ft_strcmp)
* [ft_strncmp](#ft_strncmp)
* [ft_atoi](#ft_atoi)
* [ft_isalpha](#ft_isalpha)
* [ft_isdigit](#ft_isdigit)
* [ft_isalnum](#ft_isalnum)
* [ft_isascii](#ft_isascii)
* [ft_isprint](#ft_isprint)
* [ft_toupper](#ft_toupper)
* [ft_tolower](#ft_tolower)

Part 2 - Additional functions:

* [ft_memalloc](#ft_memalloc)
* [ft_memdel](#ft_memdel)
* [ft_strnew](#ft_strnew)
* [ft_strdel](#ft_strdel)
* [ft_strclr](#ft_strclr)
* [ft_striter](#ft_striter)
* [ft_striteri](#ft_striteri)
* [ft_strmap](#ft_strmap)
* [ft_strmapi](#ft_ft_strmapi)
* [ft_strequ](#ft_strequ)
* [ft_strnequ](#ft_strnequ)
* [ft_strsub](#ft_strsub)
* [ft_strjoin](#ft_strjoin)
* [ft_strtrim](#ft_strtrim)
* [ft_strsplit](#ft_strsplit)
* [ft_itoa](#ft_itoa)
* [ft_putchar](#ft_putchar)
* [ft_putstr](#ft_putstr)
* [ft_putendl](#ft_putendl)
* [ft_putnbr](#ft_putnbr)
* [ft_putchar_fd](#ft_putchar_fd)
* [ft_putstr_fd](#ft_putstr_fd)
* [ft_putendl_fd](#ft_putendl_fd)
* [ft_putnbr_fd](#ft_putnbr_fd)

### ft_putchar

_Description:_ Outputs the character __c__ to the standard output
_Param. #1:_ The character to output
_Return value:_ None
_Libc functions:_ write(2)

{% highlight c linenos %}
#include "libft.h"

void	ft_putchar(char c)
{
	write(1, &c, 1);
}
{% endhighlight %}

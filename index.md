<base href="https://clin1234.github.io/">
<nav>
      <a href="index.html">Home</a>
      <a href="projects/index.html">Projects</a>
      <a href="aboutme.html">About Me</a>
      <a href="blog/index.html">Blog</a>
      <a href="resources.html">Helpful Resources</a>
      <a href="https://github.com/clin1234/">Github</a>
</nav>

# Minimal and Spiffy Personal Website

As a news program would say: Wilkommen zu Tagesschau. Heut in Studio, _insert anchor here_.

## Consulting

With close to 2 years of experience contributing to prominent open-source projects and development on Linux and Windows, my experience will help you
 modernize your aging codebase, whether that may be upgrading to newer versions of C++ (and thus incorporate useful conveniences), or fixing system-related issues
  on Linux and Windows. Rates are tailorable to your specific needs: contact **[here](mailto:clin@rollins.edu)**.

Also, I have prior experience assisting clients with the purchase of one commerical property and a few residential ones all across Central Florida and 
the Tampa metropolitan area, just in the past year alone. If you need assistance in relocation or setting up shop anywhere in Florida, I am also a certified realtor. See my above email address, or
 my [real estate company](https://www.baystreetgroupfl.com/).

# Miscellaneous certifications

Because of limited space to squeeze my resume into a single page, certifications that I deem secondary in terms of importance will be listed here.

* [Image Processing with Python](https://www.datacamp.com/statement-of-accomplishment/track/0903c21f7f062f4de6ac39c080734596366bcadc)

## Links (Pun is intentional.)

* [Code for my website](https://github.com/clin1234/clin1234.github.io)
* [zlite library](https://github.com/clin1234/zlite) Still in progress.
* [copilot-clone](https://github.com/clin1234/copilot-clone) A VSCode extension for code suggestions, much like Github Copilot. GH page is [here](https://clin1234.github.io/copilot-clone)
* [NMS](https://github.com/clin1234/NMS) a proof of concept Minesweeper-like clone with multiplayer support. Still in progress.

## ACM club (outdated)

* [Slack page](https://acm2019-20.slack.com)
* [ACM Discord Server](https://discord.com/channels/693677245394452522/693677245838917634)

# Magic: the Gathering

* [r/mtgfinance](https://reddit.com/r/mtgfinance) Subreddit for speculation on the game's secondary market.
* [Scryfall](https://scryfall.com) Search cards easily. Much better than the official Gatherer. 

A gem from the 26th IOCCC (see [here](https://www.ioccc.org/2019/burton/)):
```c
static int e,n,j,o,y;int main(){for(++o;(n=-~getchar());e+=11==n,y++)o=n>0xe^012>n&&'`'^n^65?!n:!o?++j:o;printf("%8d%8d%8d\n",e^n,j+=!o&&y,y);}
```

Formatted for readability:
```c
#include <stdio.h>
static int e, n, j, o, y;
int main() {
    for (++o; (n = -~getchar()); ((e += (11 == n)), y++))
        o = ((n > 0xe) ^ (012 > n)) && ('`' ^ n ^ 65)
            ? (!n)
            : (!o ? (++j) : o);
    printf("%8d%8d%8d\n", e^n, j += (!o && y), y);
}
```

This is an implementation of `wc`. To explain:
1. While `n` is not a EOF, it reads `stdin`.
Note that input is limited to 99,999,999 bytes, and assumes ASCII encoding.
2. In the loop, it sets `o` if:
    a. `n` is not between 0xA and 0xE. If true, set to 0. Otherwise, check if `o` equals 0. If true, increments `j`, otherwise do nothing.
3. Outputs the number of newlines (`e OR n`), number of words (`j = j + ((o == 0) AND y)`), and number of bytes (`y`).

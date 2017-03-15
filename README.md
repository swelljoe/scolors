# scolors
Define terminal/shell agnostic colors for shell scripts.

I regularly test in bash and dash, with terminals on Linux and Windows (git bash, Cygwin bash, WSL bash, PuTTY). It probably works in most POSIX-y shells and most modern UNIX-y terminals.

# Usage

Source it, and use any of the newly defined colors, or bold/underline (though the latter are not well-supported by many terms).

```bash
. ./scolors.sh

printf "${BLUEBG}Doot doot, I'm in color!${NORMAL}\n"
```

The available colors are: RED, GREEN, YELLOW, BLUE, MAGENTA, CYAN, WHITE, REDBG, GREENBG, YELLOWBG, BLUEBG, MAGENTABG, CYANBG, BOLD, UNDERLINE, NORMAL. The colors with "BG" on the end set the background color. The ones without set the foreground text color. BOLD and UNDERLINE do what you'd expect, except when they don't (which is a lot of the time...probably shouldn't use them unless you controll the whole workflow that you're deploying to, as it they probably won't work right).

# What's it look like?

![scolors demo](http://i.imgur.com/IWfDT1z.png)

# Contributing

As always, I welcome patches, as long as they don't break compatibility across bash and dash and all the popular modern-ish terminals. I particularly like patches that add or improve support for other shells or other terminals.

+++
title = 'minishell'
date = 2024-06-24
draft = false
description = 'A cuter bash.'
+++

This has been the toughest project so far since I [joined 42](https://www.42madrid.com/en/philosophy-42/).

It consisted on creating a program that was able to have many of the same functionalities bash has, such as:
- Have a functional history of all previous commands.
- Run the right executable based on PATH or relative and absolute paths.
- Implement redirections such as <, >, <<, and >>.
- Implement pipes (|).
- Handle environment variables.
- Handle $?.
- Handle signals such as ctrl-C, ctrl-D, and ctrl-\\.
- Implement the built-ins: echo, cd, pwd, export, unset, env, and exit (except echo and cd, all of them without arguments).
- Make sure there are no leaks.

My colleague [Carlos](https://github.com/cmunoz-g) handled the tokenizer, lexer and parser of the input received, while I took care of handling the processes correctly (that is, redirections, pipes, and executing the right things at the right order[^1]). We splitted the rest of stuff: I managed the environment variables and $?, as well as the signals and the easier built-ins; Carlos handled the harder built-ins such as export and unset, and implemented the history too.

[Here's](https://github.com/cmunoz-g/minishell) the link to the repo.

[^1]: I still have nightmares with the command `cat | cat | cat | echo << end`.
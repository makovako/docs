---
title: "Awesome command-line tools"
---

[00:00:51](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=51)

- well design popular command line tools, what they have in common, and why they are successful

[00:02:39](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=159)

- up/down arrow history
- tab completion

[00:02:56](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=176)

- hard to discover some features on our own

[00:03:25](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=205)

- gui solved it by using icons and menus

[00:04:36](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=276)

- tui - popup menus, auto-completion hints

[00:07:33](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=453)

- do not hide features behind some key, let user see them before they trigger something

[00:12:21](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=741)

- user focus, users come first, implementation alter, give user options what he might do and don't limit it based on implementation possibility/easyness

[00:15:02](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=902)

- configuration should be limited, program should be smart enough to know, what users wants

[00:15:30](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=930)

- color scheme - personal choice - should be configurable

[00:15:55](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=955)

- configurability - subjective options only

[00:17:07](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=1027)

- checklist for good apps
  - persistent history
  - history search
  - emacs keybindings
  - auto-completion
  - syntax coloring

[00:18:22](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=1102)

- library for most of the things - python-prompt-toolkit

[00:18:34](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=1114)

- repl - read/eval/print/loop

[00:26:37](https://www.youtube.com/watch?v=v2RmxZ9Vcps&t=1597)

```python
from prompt_toolkit import prompt
from prompt_toolkit.history import FileHistory
from prompt_toolkit.auto_suggest import AutoSuggestFromHistory
from prompt_toolkit.completion import WordCompleter
from prompt_toolkit.lexers import PygmentsLexer

from pygments.lexers.sql import SqlLexer

SqlCompleter = WordCompleter(["SELECT", "SHOW", "FROM", "WHERE", "TABLES"], ignore_case=True)

while True:
    inp = prompt("> ",
                         history=FileHistory("history"),
                         auto_suggest=AutoSuggestFromHisotry(),
                         completer=SqlCompleter,
                         lexer=PygmentsLexer(SqlLexer),
                         )
    print(inp)
```

[source](https://www.youtube.com/watch?v=v2RmxZ9Vcps)



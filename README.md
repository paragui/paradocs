# paradocs
minimalistic bash4 static site generator using pandoc


**Attention:** The script as a whole is not in a working state! A lot is inserted hastily since the last four days.
More and cleaning will come soon.

# Help
~~~
Usage:  paradocs [PATH] [OPTION [KEY [VAL]...]...]

Options:
-h,--help
        Show this help.
-I,--implement
        Run at first time or recreate basic implementation.
-n,--new
        Create a new book.
-u,--update
        Write changes to html.
~~~

To check a few keys that can be given to options look at source, e.g.: for 
`--new` look at top of `opt_new()`. 

The options in particular already do their job but e.g. `--update` just writes 
the given path to html for now. To try it you can run:

~~~
bash paradocs -I foo@bar.baz -author you me -date "22 Feb 2016"
bash paradocs work -n "Angewandte Künste" -author me 
bash paradocs code/markdown -n Cheatsheet
~~~

Now you find three new directories and everything at this script is made inside them:
* `~/.paradocs`: your markdown documents, templates, yaml, ... This is will be the one to store.
* `~/.local/share/paradocs`: html output
* `~/.config/paradocs`: global files like icon, css, ..


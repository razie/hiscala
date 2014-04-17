hiscala
=======

> hiscala is a dead-simple syntax highlighter for Scala code on the browser.

Based on https://github.com/cloudhead/hijs

By default, it highlights everything inside `<code>` blocks.

If you have command-line snippets, such as:

    $ ls -l > /dev/null

it will skip those, cause they ain't no JavaScript.

usage
-----

Put this at the end of your `<body>`:

    <script src="hiscala.js"></script>

It will format all the code inside `<code>` blocks all over the `<body>`.

If you would like to specify what gets highlighted, set the global `hijs` variable before you include the script:

    window.hijs = '.highlight';

example
-------

See this post for an example: http://www.racerkidz.com/wiki/Blog:Cool_Scala/Post:The_Option_monad_pattern_thing

philosophy
----------

hijs is a simple solution to a potentially complicated problem. It won't
fit all your needs, but if what you're trying to achieve is simple enough,
hijs might be the tool for you.

styling
-------

hijs wraps tokens in `<span>` tags. You can style them like so:

    code .keyword              { font-weight: bold }
    code .string, code .regexp { color: green }
    code .class, code .special { color: blue }
    code .number               { color: pink }
    code .comment              { color: grey }

Also, to change background of the entire block (i.e. dark vs light background) also set:

    pre {
      background-color: #191919;
      white-space: pre-wrap;
      word-wrap: break-word;
    }

more info
---------

**RTFC**


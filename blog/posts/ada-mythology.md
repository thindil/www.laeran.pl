-- layout: default
-- title: Ada Mythology
-- summary: Various myths related to the Ada programming language
-- backlink: ../index.html
Over time during talks with other people I encountered many myths related to
the Ada programming language. As a bit lazy person I don't want to
demystify them over and over, thus I write them here, so I can point later to
one location :) Here is the list myths related to the Ada in random order.

### Ada was created by rich, living in an ivory tower committee

While I wish all people who designed (and still designing) the Ada everything
the best (especially to be healthy and rich :)), I'm afraid that this myth is
very untrue. Even the first version of Ada was designed by the group of
programmers: they were hired by the USA Departament of Defense to desing a new
programming language, which will be following [Steelman language requirements](https://en.wikipedia.org/wiki/Steelman_language_requirements).
The only difference for Ada, compared to many other programming languages
is process of creating the language: it started from creating a list of
desired things which should be added to the new language and later,
consistent going in that way. The most people who worked or working on the
Ada standard are programmers who use Ada every day. Additionally, everyone
interested can propose own ideas to the language standard via [Ada Rapporteur Group](http://www.ada-auth.org/arg.html).
And to be honest, the most ideas which are in the language come from outside
world. Generally, organization of standardization of the Ada language is almost
that same as the C or C++ language.

### Ada is used only in military, medical, mission critical software where a new programmer don't have chance to join

That is also untrue. While Ada started as a military programming language and
due to very good support for security and embedded programming, it can be found
in many non mission critical areas too. Personally I meet the Ada in some
business software, other people with which I talked on this matter, meet an Ada
code for example in traffic lights, industrial automatics or used to manage web
servers. Also, isn't true that a new Ada programmer doesn't have chance to join
any mission critical project. That projects pretty often also offers less
"critical" parts of work to do, which can be a very good start for new Ada
programmers. And these parts often don't require any special permissions.

### Ada is outdated language

Ada is a peer for the C++ language. Both languages started in almost this same
time (around the first half of 80s of twentieth century). Since then, both
were upgraded from time to time, adding new features to the languages. The
first version of Ada is called Ada83 and next versions are: Ada95, Ada05 and
the current version, Ada 2012. Ada contains many modern programming concepts
like Object-Oriented programming, design by contract, generics or dynamically
resizeable containers (vectors, maps). Of course, the history of Ada is longer
than Go or Rust but this only made Ada more mature and stable language than the
new ones.

### Ada is hard to learn

This is probably very subjective myth. But in my opinion, the Ada language is
easier to learn than many other languages, especially these one which syntax is
based on the C language. The main reason is, that Ada uses a lot of English
words instead of various graphical symbols. That symbols are easier to written,
but their meaning are completely unknown for new programmers. From the other
side, lack of knowledge of English language can be that same problematic when
learning Ada. The second reason which make learning Ada easier are build-in
checks and high level constructs in the language. When you learn C or C++ you
have to watch yourself on various variables overflows or manually manage the
program memory. Ada, same as high level languages frees a programmer from that
problems. But it is also possible to go down and work on low level programming,
still keeping all advantages of the safe code.

Some people even claim that Ada is [much easier to learn](https://pbs.twimg.com/media/EmH4kPwXIAESAy3?format=jpg&name=medium)
than the C/C++ languages.

### Ada is slow to write due to its verbosity

That myth was true some time ago. Today, modern IDE's and programming editors
have support for code autocompletions and snippets what make writing an Ada
code that same fast as using C-like syntax languages. Especially snippets are
very useful. With them, amount of characters to type is almost equal to the
amount used in C-like languages. Even if we use the most verbose option for
writing an Ada code, with named blocks and loops, the speed will be almost
similar to languages like C++ or Rust. Especially because in these languages
generally, you have to write more code documentation than in Ada. In the Ada
programming language, there is concept of "self-documenting code" which means,
that information which are normally entered in documentation parts, in Ada
are part of the code. Good examples are mentioned above named loops, blocks
or arguments.

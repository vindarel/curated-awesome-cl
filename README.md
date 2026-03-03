<div align="center">
  <img src="http://i.imgur.com/jLVXhpc.png">
</div>

# My Curated Awesome Common Lisp

A curated list of _awesome_ Common Lisp stuff, curated for beginners.

Also don't miss the https://lispcookbook.github.io/cl-cookbook/ :)

You are invited to *make your own curated list*, and reference it here!

**edit: I now take much more care of the original list**


This was forked from the
[Awesome Common Lisp](https://github.com/CodyReichert/awesome-cl) and
modified following the ideas:
- useful things (for beginners) first: dev environment comes first, crypto last.
- prefer libraries that are superseeded by new and better ones: Drakma
  is replaced by Dexador
- prefer documented libraries
- justifications come from my experience, and I am not experienced on all topics.
- remove some stuff. For a real look at the CL ecosystem, refer to the Awesome List, to Quickdocs or to Cliki.

All libraries listed here are available from [Quicklisp][16].

This is released under the GNU Free Documentation License - its text
is provided in the LICENSE file.

<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-refresh-toc -->
**Table of Contents**

- [My Curated Awesome Common Lisp](#my-curated-awesome-common-lisp)
- [Community](#community)
- [Text Editor Resources](#text-editor-resources)
  - [ICL: improved REPL for the terminal an the browser](#icl-improved-repl-for-the-terminal-an-the-browser)
  - [Emacs](#emacs)
  - [Vim](#vim)
  - [Atom / Pulsar - maybe the second best editor plugin](#atom--pulsar---maybe-the-second-best-editor-plugin)
  - [VSCode](#vscode)
  - [Notebooks](#notebooks)
  - [REPLs](#repls)
  - [Online REPLs](#online-repls)
- [Implementations](#implementations)
- [Build Systems](#build-systems)
- [Library Manager](#library-manager)
- [Tools](#tools)
- [Web](#web)
  - [HTTP clients](#http-clients)
  - [Web frameworks](#web-frameworks)
  - [HTTP Servers](#http-servers)
  - [Parsing html](#parsing-html)
  - [Querying HTML/DOM](#querying-htmldom)
  - [HTML generators and templates](#html-generators-and-templates)
  - [URI handling](#uri-handling)
  - [Javascript](#javascript)
  - [Email](#email)
  - [Third-party APIs](#third-party-apis)
- [XML](#xml)
- [JSON](#json)
- [CSV](#csv)
- [Database and ORMs](#database-and-orms)
- [Interaction with other languages](#interaction-with-other-languages)
  - [Python](#python)
- [Game Development](#game-development)
- [Graphics](#graphics)
- [GUI](#gui)
- [Natural Language Processing](#natural-language-processing)
- [Numerical and Scientific](#numerical-and-scientific)
- [Parallelism and Concurrency](#parallelism-and-concurrency)
  - [Actors pattern](#actors-pattern)
  - [Event processing](#event-processing)
  - [Job processing](#job-processing)
- [Regex](#regex)
- [Unit Testing](#unit-testing)
- [Utilities](#utilities)
  - [Language extensions](#language-extensions)
  - [Changing the syntax](#changing-the-syntax)
  - [Iteration](#iteration)
  - [System](#system)
  - [Data validation](#data-validation)
  - [Date and time](#date-and-time)
  - [Logging](#logging)
- [Cryptography](#cryptography)
- [Learning and Tutorials](#learning-and-tutorials)
  - [Online](#online)
  - [Beginner](#beginner)
  - [Intermediate](#intermediate)
  - [Advanced](#advanced)
  - [Reference](#reference)
  - [Showcase](#showcase)
  - [Offline](#offline)
  - [Beginner](#beginner-1)
  - [Intermediate](#intermediate-1)
  - [Advanced](#advanced-1)
  - [Web development tutorials](#web-development-tutorials)
- [Contributing](#contributing)

<!-- markdown-toc end -->

<p>
  <h2 align="center">  <a align="center" href="http://www.lisp-screenshots.org/">lisp-screenshots.org</a> </h2>
  <!-- <h3 align="center"> Today's Common Lisp applications in action. </h3> -->
  <a href="http://www.lisp-screenshots.org/">
    <img style="max-width: 100%" src="/lisp-screenshots.png"></img>
  </a>
</p>


Community
=========

* [Common Lisp Cookbook](https://lispcookbook.github.io/cl-cookbook/)
* [Reddit](https://www.reddit.com/r/lisp/)
* [Lisp Discord Server](https://discord.gg/hhk46CE)
* [CL CommunitySpec](https://cl-community-spec.github.io/pages/index.html) - the CL spec, nicely rendered and searchable.


And see below, learning and tutorials.


Text Editor Resources
=====================

[Cookbook: getting started](https://lispcookbook.github.io/cl-cookbook/getting-started.html)

This contains plugins and other goodies for various text editors.

[Cookbook: editor resources](https://lispcookbook.github.io/cl-cookbook/editor-support.html)

## ICL: improved REPL for the terminal an the browser

- [ICL](https://github.com/atgreen/icl/) - easy-to-use Common Lisp REPL with many new features.
  - easy to install (.deb and other installers)
  - easy to use: no interactive debugger but clean stacktraces, real code completion with a nice interactive menu (this isn't readline, it is using a proper TUI library)
  - browser REPL
    - with new features: display data structures as tables and graphs (or more)
    - watch variables
  - interactive variables inspector
  - possible connection from Emacs and Slime: you start a websocket connection with the browser, you code in Emacs, but you get the browser's features (display variables, etc).

ICL doesn't replace a real IDE but it is a GREAT way for getting started.

*This was co-authored with LLMs.*


## Emacs ##

* [Portacle][201] - A portable and multiplatform Common Lisp environment: SBCL, Quicklisp, Emacs, Slime, Git.
  * *it is unmaintained and it is getting old (old Emacs version), but if it works for you, it is a good way for getting started.*
* [SLIME][29] - Superior Lisp Interaction Mode for Emacs; a full-blown environment for Common Lisp inside of Emacs. Public domain.
* [plain-common-lisp](https://github.com/pascalcombier/plain-common-lisp/) -  A trivial way to get a native Common Lisp environment on Windows.

## Vim ##

* [SLIMV][187] - Superior Lisp Interaction Mode for Vim; a full-blown environment for Common Lisp inside of Vim. No license specified.

## Atom / Pulsar - maybe the second best editor plugin

* [SLIMA](https://github.com/neil-lindquist/SLIMA/) allows you to
  interactively develop Common Lisp code, helping turn Atom into a
  full-featured Lisp IDE. [MIT][200].

## VSCode

* [alive](https://github.com/nobody-famous/alive) -  Common Lisp Extension for VSCode. Public domain.
  * see the Cookbook: [using VSCode with Alive](https://lispcookbook.github.io/cl-cookbook/vscode-alive.html)
  * *it might need more love but it's getting there.*


## Notebooks ##

* [cl-jupyter](https://github.com/fredokun/cl-jupyter) - A Common Lisp kernel for Jupyter notebooks [custom licence](https://github.com/fredokun/cl-jupyter/blob/master/LICENSE).

## REPLs ##

* ICL as mentioned above
* [cl-repl](https://github.com/lisp-maintainers/cl-repl) - an ipython-like REPL. With completion, shell commands, magic commands, debugger, etc. [GPL3][2]. With [colorthemes](https://github.com/koji-kojiro/lem-pygments-colorthemes).

[How to use rlwrap and linedit with SBCL](https://gist.github.com/vindarel/2309154f4e751be389fa99239764c363).

## Online REPLs

* check out how far JSCL has come since late 2025! https://jscl-project.github.io/
* JupyterLite and JSCL, 100% in the browser (new in 2026): https://wiki3-ai.github.io/jscl-kernel/


Implementations
===============

* [SBCL][12] - A fork of CMUCL; compiles to machine code. [Standard compliance][13]. Public domain, with some parts under [Expat][14] and [3-clause BSD][15].
  - *Just use it if you don't know what do use*
  - *Install it from your package manager: `apt install sbcl`*
  - *It does thorough type checking*
  - *Google contributes to SBCL!*
  - *It is very active and constantly improves.*
* [Clozure Common Lisp](https://ccl.clozure.com/docs/ccl.html), for its fast compilation time, and to use on 32bits Raspberry Pi.
* If you are a pro or have $$$, check out LispWorks' features.

But there are more, see other ressources.

Build Systems
=============

* [ASDF][131] - it's the de-facto build system shipped with the implementations.

Library Manager
===============

* [Quicklisp][16] - *The* library manager.
  - *You just must use it, then learn other tools that complement it.*
  - [ql-https](https://github.com/rudolfochrist/ql-https) - shell out to cURL and use HTTPS by default.
* [Ultralisp](https://ultralisp.org/) - A quicklisp distribution that builds every five minutes (instead of one month for Quicklisp), and requires 3 clicks to add your project to it (instead of opening an issue and waiting for Quicklisp).
* [Qlot][135] - A project-local library installer. Uses HTTPS.
* [ocicl](https://github.com/ocicl/ocicl) - a new and experimental alternative to Quicklisp, built on tools from the world of containers. [MIT][200].
  * *ocicl might be the next de-facto package manager, who knows? It's working well.*


Tools
=====

These are applications or bits of code that make development in Common Lisp easier without being Common Lisp libraries themselves.

* [cl-cookieproject](https://github.com/vindarel/cl-cookieproject) - my project skeleton, more complete than the others. *New in 2021 :)*
- [Quicksearch](https://github.com/lisp-maintainers/quicksearch) - search for projects on GitHub, Quicklisp, Cliki and Bitbucket. MIT.  *This one helped me sometimes*.

Web
===

HTTP clients
------------
* [Dexador][199] - An HTTP client: `(dex:get "http://url.com")`.

A video: [How to request the GitHub API](https://www.youtube.com/watch?v=TAtwcBh1QLg).

Web frameworks
--------------

There are more on the awesome-cl list, and in the wild. Those are my choices.

I also published a new learning resource for web development in CL: [https://web-apps-in-lisp.github.io/](https://web-apps-in-lisp.github.io/).

* Hunchentoot documentation on a "read the docs" style: https://common-lisp-libraries.readthedocs.io/hunchentoot/
* 👍 [easy-routes](https://github.com/mmontone/easy-routes) - a routes handling system on top of Hunchentoot. It supports dispatch based on HTTP method, arguments extraction from the url path, decorators, url generation from route name, etc.
  - *I like it a lot, that's what I use to define routes.*
* [Caveman][92] - A powerful web framework.
  - *Written by E. Fukamachi, and with GitHub stars.*
  - *Not full-featured, but makes defining routes and rendering templates easy.*
* [cl-rest-server](https://github.com/mmontone/cl-rest-server) - a library for writing REST web APIs. Features validation with schemas, annotations for logging, caching, permissions or authentication, documentation via Swagger, etc. [MIT][200].
* [Weblocks (Reblocks)](https://github.com/40ants/reblocks) - A widgets-based framework with a built-in ajax update mechanism that "solves the JavaScript problem". [LLGPL][8].
  - *it's cool but it's its own thing. It won't solve everything for you.*
* [CLOG](https://github.com/rabbibotton/clog) - The Common Lisp Omnificent GUI. Uses web technology to produce graphical user interfaces for applications locally or remotely. [BSD_3Clause][15].
  - CLOG is based on the ideas of GNOGA, a framework the author wrote for Ada and used in commercial production code since 2013.


*my 2 cents*: I find Clack-based frameworks tedious to use. Be sure to test others (Wookie, Snooze,…). Don't juge projects uniquely by their numbers of Github stars.


HTTP Servers
------------
* [Hunchentoot](https://edicl.github.io/hunchentoot/) - the CL web server.
* [Clack][90] - A web application environment inspired by Rack and WSGI.
  - *but it's seldom documented :/*
  - see https://nmunro.github.io/2024/12/29/ningle-1.html
* [wookie][109] - Asynchronous HTTP server. [Expat][14].
* [woo](https://github.com/fukamachi/woo) - A fast non-blocking HTTP server on top of nodejs' libev. [MIT][200].


Parsing html
------------

[Cookbook: web scraping](https://lispcookbook.github.io/cl-cookbook/web-scraping.html)

* [Plump][71] - A lenient HTTP/XML parser, tolerand on malformed markup. [Artistic License 2.0][51]. Best used with [lquery][72] and [clss][202].
* [cl-html5-parser](https://github.com/rotatef/cl-html5-parser) -  HTML5 parser for Common Lisp. GPL3.0.
  * a port of the Python library html5lib.
  * compared to Plump: Plump is a mix of an XML and an HTML parser and breaks on some HTML rules ([example](https://github.com/Shinmera/plump/issues/50)), while cl-html5-parser is a fully compliant HTML parser.

Querying HTML/DOM
-----------------

* [lquery][72] - A jQuery-like HTML/DOM manipulation library. [Artistic License 2.0][51].


HTML generators and templates
-----------------------------

* [Djula][100] - A port of Django's template engine to Common Lisp.
  - *very good, easy to use, no surprises. For example, defining custom filters is a breeze*.
* [Ten](https://github.com/mmontone/ten) - by Djula's maintainer, a more flexible framework, where we can write lisp expressions in templates.
  - *Quite new, didn't try.*
* [spinneret][191] - Common Lisp HTML5 generator.
* [markup](https://github.com/moderninterpreters/markup) - JSX-like reader-macro to let you write HTML code inside of Common Lisp.


URI handling
------------
* [quri](https://github.com/fukamachi/quri) - Another URI library for
  Common Lisp. Supports userinfo, IPv6 hostname, encoding/decoding
  utilities,…
* [cl-slug](https://github.com/EuAndreh/cl-slug) - a small library to make slugs, mainly for URIs, transform in CamelCase, remove accentuation and punctuation, for english and beyound.

Javascript
----------
* [Parenscript][102] - A translator from Common Lisp to Javascript. [3-clause BSD][15].
* [parse-js][104] - A package for parsing ECMAScript 3. [zlib][33].
* [JSCL](https://github.com/jscl-project/jscl) - A CL-to-JS compiler designed to be self-hosting from day one.
  * *since 2025 now has complete FORMAT support (backported from CMUCL)*
  * *CLOS support with CLOSETTE (slow)*
  * *very decent LOOP support*
* [sigil](https://github.com/burtonsamograd/sigil) - A Parenscript to
Javascript command line compiler and REPL. [MIT][200].

See also
[trident-mode](https://github.com/johnmastro/trident-mode.el), an Emacs
minor mode for live Parenscript interaction.


and new ones in development:

* [JACL](https://tailrecursion.com/JACL/)
* [Valtan](https://github.com/cxxxr/valtan)

Email
-----

* see the awesome list. There are wrappers to online services to send emails, and full IMAP solutions.


Third-party APIs
----------------

It's just a selection you know. See awesome-cl and Google!

* [aws-sdk-lisp](https://github.com/pokepay/aws-sdk-lisp/) - Provides interfaces for each AWS services as individual systems. [BSD_2Clause][17].
  * incluse dozens of services: dsn, appstream, athena, cloudfront, codedeploy, cognito-*, directconnect, dynamodb, dms, elasticache, email, events, kinesis, machinelearning, monitoring, s3, sms, storagegateway, workspaces…
* [north](https://shinmera.github.io/north) - The successor to the
  South (Simple OaUTH) library, implementing the full oAuth 1.0a
  protocol, both client and server sides. Using North you can easily
  become an oAuth provider or consumer. [Artistic License 2.0][51].
* [avatar-api](https://github.com/eudoxia0/avatar-api) - Get avatars from Google+, Gravatar and others. [Expat][14].
* [chirp](https://github.com/Shinmera/chirp) - A Twitter client library. [Artistic License 2.0][51].
* [cl-irc](https://www.common-lisp.net/project/cl-irc/) - An IRC client library. [Expat][14].
* [cl-openid](https://common-lisp.net/project/cl-openid/darcs/cl-openid/) - An implementation of OpenID. [LLGPL][8].
* [cl-pushover](https://github.com/TeMPOraL/cl-pushover) -  Common Lisp bindings to Pushover. [MIT][200].
* *and more on awesome-cl*

XML
===

* [CXML][70] - XML parser, with a range of extension libraries. [LLGPL][8].
* [Plump][71] - A lenient HTTP/XML parser, tolerand on malformed markup. [Artistic License 2.0][51]. Best used with [lquery][72] and [clss][202].
* [s-xml][168] - A basic parser. [LLGPL][8].
* [xmls][169] - A small, simple, non-validating XML parser. [3-clause BSD][15].

JSON
====

* 👍 [jzon](https://github.com/Zulu-Inuoe/jzon/) - a correct, safe and fast JSON parser. [MIT][200].
  * jzon is the only CL JSON library which correctly declines all invalid inputs per the official JSON test suite and accepts all valid inputs per that suite.
  * it doesn't crash on invalid input (jsown), doesn't choke on large datasets (Jonathan), and more.
  * v1.0 released in the Quicklisp dist of February, 2023.
  * "I believe jzon to be the superior choice and hope for it to become the new, true de-facto library in the world of JSON-in-CL once and for all."
* [shasht](https://github.com/yitzchak/shasht) -  Common Lisp JSON reading and writing for the Kzinti. [MIT][14].
  - " Shasht is one of the two new libraries that I particularly like and is already in quicklisp. It is fast, it handles null correctly, it encodes CLOS objects, structures and hash-tables. It can also do incremental encoding." Sabra Crolleton.

CSV
===

* [cl-csv][170] - A library for parsing CSV files.
  * *battle tested, used in the wild.*
  * [documentation](https://github.com/AccelerationNet/cl-csv/blob/master/DOCUMENTATION.md)
  * [example blog post](https://dev.to/vindarel/read-csv-files-in-common-lisp-cl-csv-data-table-3c9n).

See also: cl-duckdb for fast parsing, [lisp-stat's data-frames `read-csv`](https://lisp-stat.dev/docs/manuals/data-frame/), [vellum-csv](https://github.com/sirherrbatka/vellum-csv/) (data frames library), vellum-duckdb.


Database and ORMs
=================

[Cookbook: databases](https://lispcookbook.github.io/cl-cookbook/databases.html)

* [mito][31] - An ORM for Common Lisp with migrations, schema versioning, relationships, PostgreSQL support.
  - *I like it. It is an ORM, in that it allows to define classes and map them to tables, it gives CRUD functions for free, but other than that it is very flexible. We are closer to SQL than other ORMs out there.*
* [postmodern][32] - A library for interacting with PostgreSQL.

For much more, see the awesome-cl list.


Interaction with other languages
================================


## Python ##

* [py4cl](https://github.com/bendudson/py4cl) - A library that allows Common Lisp code to access Python libraries. It is basically the inverse of cl4py. [MIT][200].
  * [py4cl2-cffi](https://github.com/digikar99/py4cl2-cffi) - CFFI based alternative to py4cl2.
    * "When capable, the CFFI approach can be a 50 times faster than py4cl2."
* [cl4py](https://github.com/marcoheisig/cl4py) - The library cl4py (pronounce as clappy) allows Python programs to call Common Lisp libraries. [MIT][200].

See also [async-process](https://github.com/cxxxr/async-process/).

Game Development
================

* see the awesome list.

A great paper: [Experience report: Kandria, a game in Common Lisp](https://raw.githubusercontent.com/Shinmera/talks/master/els2023-kandria/paper.pdf).

Graphics
========

These are libraries for working with graphics, rather than making GUIs (i.e. widget toolkits), which have their own section.

* [cl-cairo2][53] - Cairo bindings. [Boost 1.0][54]
* [cl-gd][61] - A library providing an interface to the GD graphics library. [FreeBSD][39].
* [cl-opengl][163] - CFFI bindings to OpenGL, GLU and GLUT APIs. [3-clause BSD][15].
* [cl-sdl2][60] - Bindings for SDL2 using C2FFI. [Expat][14].
* [cl-svg][57] - A basic library for producing SVG files. [Expat][14].
* [CLinch][63] - Common Lisp 2D/3D graphics engine for OpenGL. [FreeBSD][39].
* [donuts][138] - Graph drawing DSL for Common Lisp. [Expat][14].
* [lispbuilder-sdl][180] - A set of bindings for SDL. [Expat][14].
* [Vecto][55] - Simple vector drawing library. [FreeBSD][39].
* [zpng][56] - A library for creating PNG files. [FreeBSD][39].

GUI
===

https://lispcookbook.github.io/cl-cookbook/gui.html

* [ltk][179] - A binding for the Tk toolkit. [LLGPL][8] or [GNU LGPL2.1][11].
  - *if you want a simple GUI and to be started the fastest, try Ltk!*
  * [LTk Examples](https://peterlane.netlify.app/ltk-examples/) - Provides LTk examples for the tkdocs tutorial.
  * [LTk Plotchart](https://peterlane.netlify.app/ltk-plotchart/) - A wrapper around the tklib/plotchart library to work with LTk. This includes over 20 different chart types (xy-plots, gantt charts, 3d-bar charts etc...).
* [nodgui](https://codeberg.org/cage/nodgui) - Bindings for the Tk toolkit, based on Ltk, with syntax sugar and additional widgets. [LLGPL][8].
  - *nodgui defines more widgets and syntax suger for Ltk. His maintainer his reactive.*
  * 🎨 supports [tk custom themes](https://wiki.tcl-lang.org/page/List+of+ttk+Themes), such as [ttkthemes](https://ttkthemes.readthedocs.io/en/latest/themes.html) and [Forest-ttk-theme](https://github.com/rdbende/Forest-ttk-theme).
  * supports an SDL frame as an alternative to the Tk canvas when fast rendering is needed. For 2D (pixel-based) and 3D rendering (using openGL).
* 🆕 [cl-gtk4](https://github.com/bohonghuang/cl-gtk4) -  GTK4/Libadwaita/WebKit binding for Common Lisp. [LGPL3][9].
* [IUP](https://github.com/lispnik/iup/) - CFFI bindings to the [IUP](https://www.tecgraf.puc-rio.br/iup/) Portable User Interface library (pre-ALPHA). IUP is cross-platform (Windows, macOS, GNU/Linux, with new Android, iOs, Cocoa and Web Assembly drivers), has many widgets, has a small api and is actively developed.
  - *More advanced than Tk, less than Qt. Also very easy to use. The Lisp library is very well done. Totally deserves more attention.*
* [ceramic][192] - Desktop web apps with Common Lisp. [Expat][14].
  * see: https://lisp-journey.gitlab.io/blog/three-web-views-for-common-lisp--cross-platform-guis/
* [LispWork's CAPI](http://www.lispworks.com/products/capi.html) - A portable GUI toolkit, with mobile runtime. Proprietary, but comes with a free version.
  - *the free version is easy to install, we can try it.*


Natural Language Processing
===========================

See the awesome-cl list.


Numerical and Scientific
========================

[Cookbook: numbers](https://lispcookbook.github.io/cl-cookbook/numbers.html)

[Cookbook: multidimensionnal arrays](https://lispcookbook.github.io/cl-cookbook/arrays.html)

*I am not knowledgeable here*

* [lisp-stat](https://github.com/lisp-stat) - an environment for statistical computing, conceptually similar to R, that is also suitable for front-line production deployments. "It grew out of a desire to have an environment for rapidly prototyping analytical and A.I. solutions, and move directly to production environments with minimal friction."
  * https://lisp-stat.dev/
  * ships Luke Tierney's [XLisp-Stat](https://homepage.stat.uiowa.edu/~luke/xls/xlsinfo/) (a predecessor of R) as well as newer libraries.
* [numcl](https://github.com/numcl/numcl) - Numpy clone in Common Lisp. [LGPL3][9].
* [numericals](https://github.com/digikar99/numericals) -  SIMD powered simple-math numerical operations on arrays for Common Lisp through CFFI [still experimental]. MIT.
  * documentation: https://digikar99.github.io/numericals/
* [dense-arrays](https://github.com/digikar99/dense-arrays) -  Numpy like array object for common lisp. MIT.
* [Petalisp](https://github.com/marcoheisig/Petalisp) - an attempt to
  generate high performance code for parallel computers by
  JIT-compiling array definitions. It works on a more
  fundamental level than NumPy, by providing even more powerful
  N-dimensional arrays, but just a few building blocks for working on
  them. [AGPL-3.0][agpl3].
* [lisp-matrix][86] - A matrix package. [FreeBSD][39].
* [maxima][165] - Computer algebra system. Not available on Quicklisp. [GNU GPL3][2].
* [GSLL][84] - GNU Scientific Library for Lisp; allows the use of the GSL from Common Lisp. [GNU LGPL2.1][11].


Parallelism and Concurrency
===========================

[Cookbook: threads](https://lispcookbook.github.io/cl-cookbook/process.html)

* [BordeauxThreads][171] - Portable, shared-state concurrency. [Expat][14].
* [lparallel][114] - A library for parallel programming. [3-clause BSD][15].
* [lfarm](https://github.com/lmj/lfarm) - distributing work across machines (on top of lparallel and usocket). [BSD_3Clause][15]
* [cl-async][116] - A library for general-purpose, non-blocking programming, built on [libuv](https://github.com/libuv/libuv) (the library that powers Nodejs). [Expat][14].
* [chanl][117] - Portable, channel-based concurrency. [Expat][14], with parts under [3-clause BSD][15].
* [Moira](https://github.com/TBRSS/moira) -  Monitor and restart background threads. In-lisp process supervisor. [MIT][200].
* [trivial-monitored-thread](https://gitlab.com/ediethelm/trivial-monitored-thread) -
  a Common Lisp library offering a way of spawning threads and being
  informed when one any of them crash and die. [MIT][200].
* [cl-gearman](https://github.com/taksatou/cl-gearman) - a library for the [Gearman](http://gearman.org/) distributed job system. [LLGPL][8].
* [swank-crew](https://github.com/brown/swank-crew) - distributed computation framework implemented using Swank Client. [BSD_3Clause][15].
* [cl-coroutine](https://github.com/takagi/cl-coroutine) - a coroutine library. It uses the CL-CONT continuations library in its implementation. [MIT][200].
* [STMX](https://github.com/cosmos72/stmx) -  High performance Transactional Memory for Common Lisp. [LLGPL][8].

Actors pattern
--------------

* [cl-gserver](https://github.com/mdbergmann/cl-gserver) - an Erlang inspired GenServer. It is meant to encapsulate state, but also to execute async operations. Also with actors. Functionality regarding state is not unsimilar to Clojure's Agent or cl-actors. [MIT][200].

Event processing
----------------

* [simple-tasks](https://github.com/Shinmera/simple-tasks) - A very simple task scheduling framework. [Artistic License 2.0][51].
* [deeds](https://github.com/Shinmera/deeds) - Deeds is an Extensible
  Event Delivery System. It allows for efficient event delivery to
  multiple handlers with a complex event filtering
  system. [Artistic License 2.0][51].
* [cl-flow](https://github.com/borodust/cl-flow/) -  Data-flowish computation tree library for non-blocking concurrent Common Lisp. [MIT][200].
* [event-glue](https://github.com/orthecreedence/event-glue) - simple eventing abstraction. No dependencies. It can be used anywhere you need a generic event handling system. [MIT][200].

Job processing
--------------


* [SBCL's timers](http://www.sbcl.org/manual/#Timers), system-wide event schedulers.
* [cl-cron](https://github.com/ciel-lang/cl-cron) - A simple tool that provides cron like facilities.
  * *it has no GitHub stars because it was on Bitbucket, but it's easy to use and it works well. Recommended.*
* [clerk](https://github.com/tsikov/clerk) - a cron-like scheduler with sane DSL. [MIT][200].


Regex
=====

[Cookbook: regular expressions](https://lispcookbook.github.io/cl-cookbook/regexp.html)

* [cl-ppcre][68] - Portable, Perl-compatible regular expressions. [FreeBSD][39].
* [one-more-re-nightmare](https://github.com/no-defun-allowed/one-more-re-nightmare) - a fast-ish regular expression compiler in Common Lisp. [BSD_2Clause][17].



Unit Testing
============

[Cookbook: testing and continuous integration](https://lispcookbook.github.io/cl-cookbook/testing.html)

* [FiveAM][123] - Simple regression testing framework.
  * [fiveam-matchers](https://github.com/tdrhq/fiveam-matchers/) -  an extensible, composable matchers library for fiveam. [Apache2.0][89].
* [Parachute](https://github.com/Shinmera/parachute) - An extensible and cross-compatible testing framework. With test dependencies, conditions, fixtures and restarts. [zlib][33].


Utilities
=========

Language extensions
-------------------

* [alexandria][149] - A general-purpose utility library.
  - *you must know that one.*
* [serapeum](https://github.com/TBRSS/serapeum/) - Another general-purpose utility library.
  - *lots of good stuff. Definitely worth checking out.*
* :star: [trivia](https://github.com/guicho271828/trivia/) - Optimized pattern-matching library. [LLGPL][8].
* [generic-cl](https://github.com/alex-gutev/generic-cl/) - Generic function interface to standard Common Lisp functions (equality, comparison, arithmetic, objects, iterator, sequences,…). [MIT][200]. See also the more lightweight [generic-comparability](https://github.com/pnathan/generic-comparability). [LLGPL][8].
* [FSet][164] - A functional, set-theoretic collections data structure library. [LLGPL][8].
* [trivial-types][145] - Trivial type definitions. [LLGPL][8].


Changing the syntax
-------------------

* [pythonic-string-reader](https://github.com/smithzvk/pythonic-string-reader) - A simple and unobtrusive read table modification inspired by Python's three quote strings. [BSD_3Clause][15].
* [cl-reader](https://github.com/digikar99/reader) - A utility library
intended at providing reader macros for lambdas, mapping, accessors,
hash-tables and hash-sets. [MIT][200].

Iteration
---------

* :star: [iterate](https://common-lisp.net/project/iterate/) - An iteration construct for Common Lisp which is extensible and Lispier. [MIT][200].
  - *but make you a favor, learn loop by example!* https://lispcookbook.github.io/cl-cookbook/iteration.html
* [for](https://shinmera.github.io/for/) - A concise, lispy and extensible
  iteration macro. Unlike loop it is extensible and sensible, and
  unlike iterate it does not require code-walking and is easier to
  extend.
  - *it has one clause that works for all data structures.*
* [trivial-do](https://github.com/yitzchak/trivial-do/) -  Additional dolist style macros for Common Lisp. [MIT][200].
* [doplus](https://bitbucket.org/alessiostalla/doplus/wiki/Home) – another extensible iteration library, similar to :for.
* [gtwiwtg](https://cicadas.surf/cgit/colin/gtwiwtg.git/about/) - A lazy sequences library. Similar to 'series' but not as complete. However it has a 'modern' API with stuff like `take`, `filter`, `for`, `fold`, etc. that is easy to use.
* [cl-transducers](https://github.com/fosskers/cl-transducers/) - Ergonomic, efficient data processing. [LGPL3][9].
  * "Transducers are an ergonomic and extremely memory-efficient way to process a data source. Here “data source” means simple collections like Lists or Vectors, but also potentially large files or generators of infinite data."
  * "It is, in general, the most complete implementation of the Transducer pattern."
  * a "modern" API with `map`, `filter`, `take`, `repeat`, `cycle`, `fold`…


System
------

The de-facto library is [uiop](http://quickdocs.org/uiop/), the
Utilities for Implementation and OS Portability. It abstracts os
utilities (getevn, chdir, etc), pathnames, the filesystem, images,
spawning processes, and much more.

[Cookbook: interfacing with your OS](https://lispcookbook.github.io/cl-cookbook/os.html)


Data validation
---------------

* [ratify][77] - A collection of utilities to ratify, validate and parse inputs. [Artistic License 2.0][51].
* [clavier](https://github.com/mmontone/clavier) - General purpose validation library for Common Lisp. [MIT][200].
* [json-schema](https://github.com/fisxoj/json-schema) - A library for validating data against schemas of drafts 4, 6, 7, and 2019-09 of the [JSON Schema](https://json-schema.org/) standard. [LLGPL][8].
* [sanity-clause](https://github.com/fisxoj/sanity-clause) - a data serialization/contract library for Common Lisp. Schemas can be property lists or class-based, allowing to check slots' types during `make-instance`. [LLGPL][8].

Date and time
-------------

[Cookbook: date and time](https://lispcookbook.github.io/cl-cookbook/dates_and_times.html)

* [localtime][122] - A development library for manipulating date and time information in a semi-standard manner. [3-clause BSD][15].
* [cl-date-time-parser](https://github.com/tkych/cl-date-time-parser) - Parse date-time-string, liberally. Hides the difference between date-time formats, and enables to manage date and time as the one date-time format. [MIT][200].
* [chronicity](https://github.com/chaitanyagupta/chronicity) - A natural language date and time parse, to parse strings like "3 days from now". [BSD_3Clause][15].
* [local-time-duration](https://github.com/enaeher/local-time-duration) -
Duration processing library built on top of local-time. [MIT][200].
* [iso-8601-date](https://gitlab.com/DataLinkDroid/iso-8601-date) - Miscellaneous date routines in Common Lisp, based around the ISO 8601 string representation. [LLGPL][8].
* [calendar-date](https://github.com/takagi/calendar-date) - a Gregorian calendar date library. [MIT][200].
* [periods](https://github.com/jwiegley/periods) - manipulating date/time objects at a higher level. With series-compatible data structure. [BSD_3Clause][15].

Logging
-------

* [log4cl][124] - Logging framework modelled after Log4J.

There are more if you have special needs.


Cryptography
============

* [Ironclad][49] - A library of crypto functions for Common Lisp. Not considered secure, but is still useful for the message digest functions. [Expat][14].
* [crypto-shortcuts][50] - Collection of common crypto shortcuts. [Artistic License 2.0][51].

Learning and Tutorials
=====================

📢 Everyone, I have an announce! I have been learning CL the hard way:
I read a lot, I wrote a lot of tutorials on the Cookbook and on my
blog, I had to ask a lot of questions, I built libraries and softwares
and I stumbled across a lot of issues. Often, my problems were not due
to the language itself, but rather in interfacing with the outside world.

So, **I built a Common Lisp course in videos** with the goal for it to be
**the most efficient way to learn Common Lisp today**. It is on Udemy:

- 📹 [Common Lisp programming: from novice to effective developer](https://www.udemy.com/course/common-lisp-programming/?referralCode=2F3D698BBC4326F94358) ⭐

You can find the table of contents details, notes and exercises on
[its Github](https://github.com/vindarel/common-lisp-course-in-videos/). It
takes so much time that it is not available for free. Check my Twitter or [my blog](https://lisp-journey.gitlab.io/) for discounts (at the beginning of the month, often). Thanks for your support, it helps.

See also other videos I post on Youtube sometimes:

- [How to create a full-featured Common Lisp project from scratch](https://www.youtube.com/watch?v=XFc513MJjos&feature=youtu.be)
- [Web requests in Common Lisp: how to fetch the Github API](https://www.youtube.com/watch?v=TAtwcBh1QLg)
- etc


## Online ##

Beginner
--------

* [Learn X in Y minutes | Where X = Common Lisp][195] - Small Common Lisp tutorial covering the essentials.
* [Practical Common Lisp][17] - A good introductory text to Common Lisp, with practical examples.
* [Common LISP: A Gentle Introduction to Symbolic Computation][161] - A nice introduction into the language.
* [Learn LISP: Simply Easy Learning][196] - A good set of introductory tutorials; includes interactive examples.
* [Common Lisp Koans][197] - The project guides the learner progressively through many Common Lisp language features.

Intermediate
------------

* [CL Cookbook](https://lispcookbook.github.io/cl-cookbook/)
* [Common Lisp tips][152] - A collaborative resource with useful tips and tricks.
- 📹 [Common Lisp programming: from novice to effective developer](https://www.udemy.com/course/common-lisp-programming/?referralCode=2F3D698BBC4326F94358), a video course tutorial on the Udemy platform, by me (@vindarel) (CL Cookbook, lisp-journey) (*paywall*, some free videos).

Advanced
--------

* [Let Over Lambda][156] - A book on advanced macro techniques. The first six chapters are available online.
* [On Lisp][26] - Paul Graham's amazing book on Lisp macros (and other interesting things).

Reference
---------

* [Common Lisp Quick Reference][25] - A distilled, pocket-size version of the ANSI CL spec. Available for download as a PDF.
* [CLHS][22] - The Common Lisp HyperSpec; the ANSI CL standard, in hypertext form.
* [Common Lisp the Langauge][160] - The original standard for Common Lisp before the ANSI spec.
* [Minispec][24] - A friendlier, but less-complete, version of CLHS. Also contains documentation for some commonly-used CL libraries (such as Alexandria).
* [Quickdocs][28] - A reference for the libraries provided by Quicklisp.

Showcase
--------

* 🔥 [lisp-screenshots.org](https://www.lisp-screenshots.org/)
* [awesome-lisp-companies](https://github.com/azzamsa/awesome-lisp-companies/)


## Offline ##

Beginner
--------

* [Land of Lisp][18] - A fun, game-oriented introduction to Common Lisp.
* [Practical Common Lisp][17] - A good introductory text to Common Lisp, with practical examples.
* [Common Lisp Koans][197] - The project guides the learner progressively through many Common Lisp language features.

Intermediate
------------

* [ANSI Common Lisp][19] - A thorough, practical covering of the entire language, with exercises. Not recommended as a starter text, due to [some caveats][20].

Advanced
--------

* [Let Over Lambda][156] - A book on advanced macro techniques. All eight chapters are available in the print copy.
* [Object-Oriented Programming in Common Lisp: A Programmer's Guide to CLOS][21] - An old, but very thorough book on CLOS.
* [Paradigms of Artificial Intelligence Programming: Case Studies in Common Lisp][157] - A book on programming AI that covers some advanced Lisp.

Web development tutorials
-------------------------

- [Web Apps in Lisp: Know-how](https://web-apps-in-lisp.github.io/).
- Ningle tutorial: https://nmunro.github.io/2024/12/29/ningle-1.html


Contributing
============

Contribute upstream to the awesome-cl list or write your own curated one, and share it!


[2]: http://www.gnu.org/copyleft/gpl.html
[3]: http://www.gnu.org/software/classpath/license.html
[4]: https://common-lisp.net/project/armedbear/faq.shtml#qa
[7]: http://ccl.clozure.com/
[8]: http://opensource.franz.com/preamble.html
[11]: http://www.gnu.org/licenses/old-licenses/lgpl-2.1.html
[12]: http://www.sbcl.org/index.html
[13]: http://www.sbcl.org/manual/index.html#ANSI-Conformance
[14]: http://directory.fsf.org/wiki/License:Expat
[15]: http://directory.fsf.org/wiki/License:BSD_3Clause
[16]: https://www.quicklisp.org/beta/
[17]: http://www.gigamonkeys.com/book/
[18]: http://landoflisp.com/
[19]: http://www.paulgraham.com/acl.html
[20]: http://www.cs.northwestern.edu/academics/courses/325/readings/graham/graham-notes.html
[21]: http://www.goodreads.com/book/show/1175730.Object_Oriented_Programming_in_Common_LISP
[22]: http://www.lispworks.com/documentation/lw50/CLHS/Front/index.htm
[23]: https://github.com/fukamachi/sxql
[24]: http://minispec.org/index.html
[25]: http://clqr.boundp.org/index.html
[26]: http://www.paulgraham.com/onlisp.html
[28]: http://quickdocs.org/
[29]: https://github.com/slime/slime
[31]: https://github.com/fukamachi/mito
[32]: http://marijnhaverbeke.nl/postmodern/
[33]: http://directory.fsf.org/wiki/License:Zlib
[39]: http://directory.fsf.org/wiki?title=License:FreeBSD
[47]: http://directory.fsf.org/wiki/License:CPLv1.0
[49]: http://method-combination.net/lisp/ironclad/
[50]: https://github.com/Shinmera/crypto-shortcuts
[51]: http://directory.fsf.org/wiki/License:ArtisticLicense2.0
[52]: https://github.com/cbaggers/varjo
[53]: https://github.com/rpav/cl-cairo2
[54]: http://directory.fsf.org/wiki/License:Boost1.0
[55]: http://www.xach.com/lisp/vecto/
[56]: http://www.xach.com/lisp/zpng/
[57]: https://code.google.com/archive/p/cl-svg
[58]: https://github.com/anwyn/cl-horde3d/
[59]: http://directory.fsf.org/wiki/License:EPLv1.0
[60]: https://github.com/lispgames/cl-sdl2
[61]: http://weitz.de/cl-gd/
[64]: https://github.com/commonqt/commonqt
[68]: http://weitz.de/cl-ppcre/
[69]: https://github.com/nikodemus/esrap
[70]: https://common-lisp.net/project/cxml/
[71]: https://github.com/Shinmera/plump
[72]: https://github.com/Shinmera/lquery
[73]: https://github.com/orthecreedence/http-parse
[74]: https://github.com/a0-prw/simple-currency
[75]: https://github.com/archimag/puri-unicode
[75]: https://github.com/hankhero/cl-json
[76]: https://github.com/madnificent/jsown
[77]: https://github.com/Shinmera/ratify
[79]: https://github.com/usocket/usocket
[80]: https://github.com/eudoxia0/postmaster
[81]: https://github.com/eudoxia0/trivial-ssh
[82]: https://github.com/Shinmera/colleen
[83]: https://www.common-lisp.net/project/cl-irc/
[84]: https://common-lisp.net/project/gsll/
[86]: https://github.com/blindglobe/lisp-matrix
[87]: https://github.com/tkych/cl-spark
[88]: https://github.com/vseloved/cl-nlp
[89]: http://directory.fsf.org/wiki/License:Apache2.0
[90]: https://github.com/fukamachi/clack
[91]: https://github.com/Shirakumo/radiance
[92]: https://github.com/fukamachi/caveman
[93]: https://github.com/fukamachi/ningle
[94]: https://github.com/eudoxia0/clack-errors
[95]: https://github.com/eudoxia0/hermetic
[96]: https://common-lisp.net/project/cl-openid/darcs/cl-openid/
[100]: https://github.com/mmontone/djula
[101]: https://github.com/arielnetworks/cl-markup
[102]: https://github.com/vsedach/Parenscript
[103]: http://marijnhaverbeke.nl/cl-javascript/
[104]: http://marijnhaverbeke.nl/parse-js/
[105]: https://github.com/eudoxia0/avatar-api
[106]: https://github.com/Shinmera/chirp
[107]: https://github.com/Shinmera/humbler
[109]: https://github.com/orthecreedence/wookie
[110]: https://github.com/franzinc/aserve
[111]: http://weitz.de/cl-fad/
[112]: https://github.com/sionescu/iolib
[113]: https://github.com/rpav/fast-io
[114]: https://github.com/lmj/lparallel
[115]: https://github.com/pkhuong/Xecto
[116]: https://github.com/orthecreedence/cl-async
[117]: https://github.com/zkat/chanl
[118]: https://github.com/takagi/cl-cuda
[119]: https://common-lisp.net/project/trivial-utf-8/
[120]: https://github.com/cl-babel/babel
[121]: https://github.com/fukamachi/cl-locale
[122]: https://common-lisp.net/project/local-time/
[123]: https://github.com/sionescu/fiveam
[124]: https://github.com/7max/log4cl
[125]: https://github.com/cl21/cl21
[126]: https://github.com/m2ym/cl-syntax
[127]: https://github.com/m2ym/cl-annot
[128]: http://www.cliki.net/cl-2dsyntax
[129]: https://github.com/melisgl/named-readtables
[130]: http://www.cliki.net/cl-interpol
[131]: https://common-lisp.net/project/asdf/
[132]: https://github.com/eudoxia0/asdf-linguist
[133]: https://github.com/CodyReichert/cl-disque
[134]: https://github.com/tarballs-are-good/quickutil
[135]: https://github.com/fukamachi/qlot
[136]: https://github.com/fukamachi/cl-project
[137]: http://mr.gy/software/texp/
[138]: https://github.com/tkych/donuts
[139]: https://common-lisp.net/project/iterate/
[140]: https://github.com/tkych/quicksearch
[141]: https://github.com/fukamachi/lesque
[142]: https://github.com/fukamachi/envy
[143]: https://github.com/Shinmera/ubiquitous
[144]: https://github.com/Shinmera/trivial-benchmark
[145]: https://github.com/m2ym/trivial-types
[146]: https://bitbucket.org/tarballs_are_good/cl-algebraic-data-type
[147]: https://bitbucket.org/tarballs_are_good/template
[148]: https://bitbucket.org/tarballs_are_good/interface
[149]: https://common-lisp.net/project/alexandria/
[150]: https://github.com/TBRSS/serapeum/
[152]: https://github.com/lisp-tips/lisp-tips/issues/
[153]: https://github.com/ahungry/glyphs/
[154]: https://cheryllium.wordpress.com/2014/02/22/commonqt-tutorial-1/
[155]: https://github.com/dmitryvk/cl-sqlite
[156]: http://letoverlambda.com/
[157]: http://norvig.com/paip.html
[158]: https://common-lisp.net/project/anaphora/
[160]: http://www.cs.cmu.edu/Groups/AI/html/cltl/cltl2.html
[161]: http://www.cs.cmu.edu/afs/cs.cmu.edu/user/dst/www/LispBook/index.html
[162]: http://cliki.net/closer-mop
[163]: https://github.com/3b/cl-opengl
[164]: http://quickdocs.org/fset/
[165]: http://maxima.sourceforge.net/
[166]: http://www.xach.com/lisp/salza2/
[167]: https://github.com/froydnj/chipz
[168]: http://cliki.net/S-XML
[169]: http://quickdocs.org/xmls/
[170]: https://github.com/AccelerationNet/cl-csv
[171]: https://common-lisp.net/project/bordeaux-threads/
[172]: https://common-lisp.net/project/osicat/
[173]: http://www.swig.org/
[174]: https://github.com/trivial-garbage/trivial-garbage
[175]: https://github.com/gwkkwg/lift
[176]: https://github.com/gwkkwg/lift/blob/master/COPYING
[178]: https://github.com/dmitryvk/cl-gtk2
[179]: http://www.peter-herth.de/ltk/
[180]: https://github.com/lispbuilder/lispbuilder
[181]: https://github.com/ahefner/mixalot
[182]: https://github.com/mishoo/sytes
[183]: https://github.com/hargettp/hh-web
[184]: http://weitz.de/cl-who/
[185]: https://github.com/paddymul/css-lite
[186]: http://www.cliki.net/CLSQL
[187]: https://github.com/kovisoft/slimv
[188]: https://github.com/triclops200/quickapp
[189]: https://github.com/triclops200/quickapp-cli
[190]: https://www.gnu.org/software/gcl/
[191]: https://github.com/ruricolist/spinneret
[192]: https://ceramic.github.io/
[193]: https://github.com/CodyReichert/cl-ses/
[194]: https://github.com/fukamachi/prove
[195]: https://learnxinyminutes.com/docs/common-lisp/
[196]: http://www.tutorialspoint.com/lisp/index.htm
[197]: https://github.com/google/lisp-koans
[198]: http://emergent-languages.org/Babel2/
[199]: https://github.com/fukamachi/dexador
[200]: https://opensource.org/licenses/MIT
[201]: https://shinmera.github.io/portacle/
[202]: https://github.com/Shinmera/CLSS

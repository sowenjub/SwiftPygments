# SwiftPygments

## A Swift wrapper for Pygments to generate HTML code from source code.

## Requirements

- Python
- Pygments: [https://pygments.org](https://pygments.org)
- Swift 5

SwiftPygments uses `PythonKit` to interact with Pygments.

Pygments can be installed via
``` zsh
pip3 install pygments
```

### Swift Package Manager
```swift
let package = Package(
    ...
    dependencies: [
    .package(url: "https://github.com/Ze0nC/SwiftPygments", .branch("master"))
    ],
    ...
)
```


## Usage:

```swift
import SwiftPygments
let code = "var i = 1\nprint(\"Hello World, \(i)\")"

if let lexer = Pygments.Lexer.named("swift") {
    Pygments.html(code, use: lexer)
}
```
or

```swift
import SwiftPygments
let code = "var i = 1\nprint(\"Hello World, \(i)\")"
Pygments.html(code, use: .swift)
```

## Supported Languages
```
ABAP
APL
Abnf
ActionScript
Ada
Adl
Agda
Aheui
Alloy
AmbientTalk
Ampl
AntlrActionScript
AntlrCSharp
AntlrCpp
AntlrJava
Antlr
AntlrObjectiveC
AntlrPerl
AntlrPython
AntlrRuby
ApacheConf
AppleScript
Arduino
AspectJ
Asymptote
AutoIt
Autohotkey
Awk
BBCode
BC
BST
BaseMakefile
Bash
BashSession
Batch
Befunge
BibTeX
BlitzBasic
BlitzMax
Bnf
Boo
Boogie
Brainfuck
Bro
Bugs
CAmkES
C
CMake
CObjdump
CPSA
CSharpAspx
CSharp
Cadl
CapDL
CapnProto
Ceylon
Chaiscript
Chapel
CheetahHtml
CheetahJavascript
Cheetah
CheetahXml
Cirru
Clay
Clean
Clojure
ClojureScript
CobolFreeformat
Cobol
CoffeeScript
ColdfusionCFC
ColdfusionHtml
Coldfusion
CommonLisp
ComponentPascal
Coq
Cpp
CppObjdump
Crmsh
Croc
Cryptol
Crystal
CsoundDocument
CsoundOrchestra
CsoundScore
CssDjango
CssErb
CssGenshi
Css
CssPhp
CssSmarty
Cuda
Cypher
Cython
D
DObjdump
DarcsPatch
Dart
DebianControl
Delphi
Dg
Diff
Django
Docker
Dtd
Duel
DylanConsole
Dylan
DylanLid
ECL
EC
EarlGrey
Easytrieve
Ebnf
Eiffel
ElixirConsole
Elixir
Elm
EmacsLisp
Erb
Erlang
ErlangShell
EvoqueHtml
Evoque
EvoqueXml
Ezhil
FSharp
Factor
Fancy
Fantom
Felix
Fennel
FishShell
Flatline
Forth
FortranFixed
Fortran
FoxPro
GAP
GLShader
Gas
Genshi
GenshiText
Gettext
Gherkin
Gnuplot
Go
Golo
GoodDataCL
Gosu
GosuTemplate
Groff
Groovy
HLSLShader
Haml
HandlebarsHtml
Handlebars
Haskell
Haxe
Hexdump
Hsail
HtmlDjango
HtmlGenshi
Html
HtmlPhp
HtmlSmarty
Http
Hxml
Hy
Hybris
IDL
Idris
Igor
Ini
Io
Ioke
IrcLogs
Isabelle
J
Jags
Jasmin
Java
JavascriptDjango
JavascriptErb
JavascriptGenshi
Javascript
JavascriptPhp
JavascriptSmarty
Jcl
Jsgf
JsonBareObject
JsonLd
Json
Jsp
JuliaConsole
Julia
Juttle
Kal
Kconfig
Koka
Kotlin
LSL
LassoCss
LassoHtml
LassoJavascript
Lasso
LassoXml
Lean
LessCss
LighttpdConf
Limbo
Liquid
LiterateAgda
LiterateCryptol
LiterateHaskell
LiterateIdris
LiveScript
Llvm
Logos
Logtalk
Lua
MOOCode
MSDOSSession
Makefile
MakoCss
MakoHtml
MakoJavascript
Mako
MakoXml
Maql
Markdown
Mask
Mason
Mathematica
Matlab
MatlabSession
MiniD
Modelica
MoinWiki
Monkey
Monte
MoonScript
MozPreprocCss
MozPreprocHash
MozPreprocJavascript
MozPreprocPercent
MozPreprocXul
Mql
Mscgen
MuPAD
Mxml
MySql
MyghtyCss
MyghtyHtml
MyghtyJavascript
Myghty
MyghtyXml
NCL
NSIS
Nasm
NasmObjdump
Nemerle
NesC
NewLisp
Newspeak
NginxConf
Nimrod
Nit
Nix
NuSMV
NumPy
Objdump
ObjectiveC
ObjectiveCpp
ObjectiveJ
Ocaml
Octave
Odin
Ooc
Opa
OpenEdge
PacmanConf
Pan
ParaSail
Pawn
Perl
Php
Pig
Pike
PkgConfig
PlPgsql
PostScript
PostgresConsole
Postgres
Povray
PowerShell
PowerShellSession
Praat
Prolog
Properties
ProtoBuf
Pug
Puppet
PyPyLog
PythonConsole
Python
PythonTraceback
QBasic
QVTo
Qml
RConsole
RNCCompact
RPMSpec
Racket
RagelC
RagelCpp
RagelD
RagelEmbedded
RagelJava
Ragel
RagelObjectiveC
RagelRuby
RawToken
Rd
Rebol
Red
Redcode
Regedit
Resource
Rexx
Rhtml
RoboconfGraph
RoboconfInstances
RobotFramework
Rql
Rsl
Rst
Rts
RubyConsole
Ruby
Rust
SAS
S
SML
Sass
Scala
Scaml
Scheme
Scilab
Scss
Shen
Silver
Slim
Smali
Smalltalk
Smarty
Snobol
Snowball
SourcePawn
SourcesList
Sparql
Sql
SqliteConsole
SquidConf
Ssp
Stan
Stata
SuperCollider
Swift
Swig
SystemVerilog
TAP
Tasm
Tcl
Tcsh
TcshSession
TeaTemplate
Termcap
Terminfo
Terraform
Tex
Text
Thrift
Todotxt
TransactSql
Treetop
Turtle
TwigHtml
Twig
TypeScript
TypoScriptCssData
TypoScriptHtmlData
TypoScript
Urbiscript
VCL
VCLSnippet
VCTreeStatus
VGL
Vala
VbNetAspx
VbNet
VelocityHtml
Velocity
VelocityXml
Verilog
Vhdl
Vim
WDiff
Whiley
XQuery
XmlDjango
XmlErb
Xml
XmlPhp
XmlSmarty
Xorg
Xslt
Xtend
Xtlang
YamlJinja
Yaml
Zephir
ABAP
APL
Abnf
ActionScript
Ada
Adl
Agda
Aheui
Alloy
AmbientTalk
Ampl
AntlrActionScript
AntlrCSharp
AntlrCpp
AntlrJava
Antlr
AntlrObjectiveC
AntlrPerl
AntlrPython
AntlrRuby
ApacheConf
AppleScript
Arduino
AspectJ
Asymptote
AutoIt
Autohotkey
Awk
BBCode
BC
BST
BaseMakefile
Bash
BashSession
Batch
Befunge
BibTeX
BlitzBasic
BlitzMax
Bnf
Boo
Boogie
Brainfuck
Bro
Bugs
CAmkES
C
CMake
CObjdump
CPSA
CSharpAspx
CSharp
Cadl
CapDL
CapnProto
Ceylon
Chaiscript
Chapel
CheetahHtml
CheetahJavascript
Cheetah
CheetahXml
Cirru
Clay
Clean
Clojure
ClojureScript
CobolFreeformat
Cobol
CoffeeScript
ColdfusionCFC
ColdfusionHtml
Coldfusion
CommonLisp
ComponentPascal
Coq
Cpp
CppObjdump
Crmsh
Croc
Cryptol
Crystal
CsoundDocument
CsoundOrchestra
CsoundScore
CssDjango
CssErb
CssGenshi
Css
CssPhp
CssSmarty
Cuda
Cypher
Cython
D
DObjdump
DarcsPatch
Dart
DebianControl
Delphi
Dg
Diff
Django
Docker
Dtd
Duel
DylanConsole
Dylan
DylanLid
ECL
EC
EarlGrey
Easytrieve
Ebnf
Eiffel
ElixirConsole
Elixir
Elm
EmacsLisp
Erb
Erlang
ErlangShell
EvoqueHtml
Evoque
EvoqueXml
Ezhil
FSharp
Factor
Fancy
Fantom
Felix
Fennel
FishShell
Flatline
Forth
FortranFixed
Fortran
FoxPro
GAP
GLShader
Gas
Genshi
GenshiText
Gettext
Gherkin
Gnuplot
Go
Golo
GoodDataCL
Gosu
GosuTemplate
Groff
Groovy
HLSLShader
Haml
HandlebarsHtml
Handlebars
Haskell
Haxe
Hexdump
Hsail
HtmlDjango
HtmlGenshi
Html
HtmlPhp
HtmlSmarty
Http
Hxml
Hy
Hybris
IDL
Idris
Igor
Ini
Io
Ioke
IrcLogs
Isabelle
J
Jags
Jasmin
Java
JavascriptDjango
JavascriptErb
JavascriptGenshi
Javascript
JavascriptPhp
JavascriptSmarty
Jcl
Jsgf
JsonBareObject
JsonLd
Json
Jsp
JuliaConsole
Julia
Juttle
Kal
Kconfig
Koka
Kotlin
LSL
LassoCss
LassoHtml
LassoJavascript
Lasso
LassoXml
Lean
LessCss
LighttpdConf
Limbo
Liquid
LiterateAgda
LiterateCryptol
LiterateHaskell
LiterateIdris
LiveScript
Llvm
Logos
Logtalk
Lua
MOOCode
MSDOSSession
Makefile
MakoCss
MakoHtml
MakoJavascript
Mako
MakoXml
Maql
Markdown
Mask
Mason
Mathematica
Matlab
MatlabSession
MiniD
Modelica
MoinWiki
Monkey
Monte
MoonScript
MozPreprocCss
MozPreprocHash
MozPreprocJavascript
MozPreprocPercent
MozPreprocXul
Mql
Mscgen
MuPAD
Mxml
MySql
MyghtyCss
MyghtyHtml
MyghtyJavascript
Myghty
MyghtyXml
NCL
NSIS
Nasm
NasmObjdump
Nemerle
NesC
NewLisp
Newspeak
NginxConf
Nimrod
Nit
Nix
NuSMV
NumPy
Objdump
ObjectiveC
ObjectiveCpp
ObjectiveJ
Ocaml
Octave
Odin
Ooc
Opa
OpenEdge
PacmanConf
Pan
ParaSail
Pawn
Perl
Php
Pig
Pike
PkgConfig
PlPgsql
PostScript
PostgresConsole
Postgres
Povray
PowerShell
PowerShellSession
Praat
Prolog
Properties
ProtoBuf
Pug
Puppet
PyPyLog
PythonConsole
Python
PythonTraceback
QBasic
QVTo
Qml
RConsole
RNCCompact
RPMSpec
Racket
RagelC
RagelCpp
RagelD
RagelEmbedded
RagelJava
Ragel
RagelObjectiveC
RagelRuby
RawToken
Rd
Rebol
Red
Redcode
Regedit
Resource
Rexx
Rhtml
RoboconfGraph
RoboconfInstances
RobotFramework
Rql
Rsl
Rst
Rts
RubyConsole
Ruby
Rust
SAS
S
SML
Sass
Scala
Scaml
Scheme
Scilab
Scss
Shen
Silver
Slim
Smali
Smalltalk
Smarty
Snobol
Snowball
SourcePawn
SourcesList
Sparql
Sql
SqliteConsole
SquidConf
Ssp
Stan
Stata
SuperCollider
Swift
Swig
SystemVerilog
TAP
Tasm
Tcl
Tcsh
TcshSession
TeaTemplate
Termcap
Terminfo
Terraform
Tex
Text
Thrift
Todotxt
TransactSql
Treetop
Turtle
TwigHtml
Twig
TypeScript
TypoScriptCssData
TypoScriptHtmlData
TypoScript
Urbiscript
VCL
VCLSnippet
VCTreeStatus
VGL
Vala
VbNetAspx
VbNet
VelocityHtml
Velocity
VelocityXml
Verilog
Vhdl
Vim
WDiff
Whiley
XQuery
XmlDjango
XmlErb
Xml
XmlPhp
XmlSmarty
Xorg
Xslt
Xtend
Xtlang
YamlJinja
Yaml
Zephir
Python
Bash
Html
Javascript
Ruby
Perl
Tex
```
## License
MIT License

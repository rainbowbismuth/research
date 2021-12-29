# noweb
A [[Literate programming]] system that described as "simple and extensible." Unlike [[WEB]] it is completely language agnostic, and based on a pipeline of transformations which you can modify with your own processing steps.

## Filters
A `noweb` filter is a program that reads a list of commands on [[STDIN]] and outputs a potentially modified sequence of commands on [[STDOUT]]. Each part of the `noweb` syntax gets converted into a command represented by a single line that starts with `@commandname`.

## Quick Start
- `@` in first column of a line starts a documentation chunk, `[[your code]]` for embedded code fragments.
- `<<name of chunk>>=` in first column of a line to start a code chunk
	- Use `<< >>` to include other code chunks by reference.
	- Multiple chunks with the same name are concatenated
	* Top level chunks are named after the file that get weaved into, e.g. `<<main.zig>>=`.
* `noweave -x file.nw > file.tex` to compile into book form, `-x` for cross references.
* `notangle file.nw` exports all of the files from the `noweb` document
* `notangle -Rmain.zig file.nw > main.zig` exports specifically `<<main.zig>>=`.
* generated $\TeX$ makes use of a provided `noweb.sty` and `nwmac.tex`
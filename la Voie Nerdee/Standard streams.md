In Linux, input and output operations between a program and its environment are managed through standard *I/O streams*.

There are 3 types of I/O connections:
## standard input (*stdin*)

- A stream which program reads data from
- Use `0` file descriptor

## standard output (*stdout*)

- A stream which program writes data to
- Use `1` file descriptor

## standard error (*stderr*)

- A stream which program writes error messages to
- Use `2` file descriptor

![[standard-stream.webp]]





[^1]: Sources:
	https://zedas.fr/posts/linux-explained-6-standard-streams/

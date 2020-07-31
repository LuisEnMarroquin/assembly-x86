# Assembly x86 program

The simplest example that I could find of an x86 assembly app

## Setup

If you are on Linux or macOS check that you have the following dependencies

```shell
type -a as ld
```

If you are on Windows use MinGW or WSL and install the same software

## Compile and execute

Tell the assembler `as` to take in the program file `exit.s` compile it, and generate the output file `exit.o`

```shell
as exit.s -o exit.o
```

Link the object file generated to a file that can be executed by the system

```shell
ld exit.o -o exit
```

Run the compiled program

```shell
./exit # Linux / macOS
start exit # Windows
```

To test that the program executed correctly, which will show the exit code of the last program that ran, in this case `0`

```shell
echo $?
```

To also see that exit code changes you can run before a commands that fails and output it's exit code that will be `1`

```shell
cd nonExistingFolder
echo $?
```

## References

* [Writing Your First x86 Program](https://medium.com/@scottc130/writing-your-first-x86-program-3fd2b33139d6)

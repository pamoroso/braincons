# Braincons

[Braincons](https://github.com/pamoroso/braincons) is an Interlisp implementation of the [Brainfuck](https://en.wikipedia.org/wiki/Brainfuck) esoteric programming language developed under [Medley Interlisp](https://interlisp.org).

![Braincons data structures.](https://raw.githubusercontent.com/pamoroso/braincons/main/braincons.png)

It will eventually provide a minimal Brainfuck development environment with an editor and a display of the execution environment, the virtual machine memory, and its state.


## Status

Braincons is in an early stage of development and largely incomplete, so there's no program, window, or command to run yet. Preliminary versions of some of the main functions and data structures are in place and can be called or inspected from the Lisp Executive.


## Installation

Download the file `BRAINCONS` from the project repo, copy it to a file system your Medley Interlisp installation has access to, and evaluate the following expression from the Lisp executive:

```lisp
(FILESLOAD BRAINCONS)
```


## Usage

Call the parser function `BRC.PARSE` and pass it a source string representing a Brainfuck program:

```lisp
(SETQ PARSED.PROGRAM (BRC.PARSE "<>[.,]+-"))
```

`BRC.PARSE` returns the intermidiate representation of the source assigned the variable `PARSED.PROGRAM`, which you can inspect as a `BRC.PROGRAM` record with:

```lisp
(INSPECT PARSED.PROGRAM)
```

The inspected record and its fields should look similar to the above screenshot.


## Author

Braincons is developed by [Paolo Amoroso](https://github.com/pamoroso).


## License

This code is distributed under the MIT license, see the `LICENSE` file.

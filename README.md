# Compiler Front-End (Lexer, Parser, Typechecker)

Built this for a programming languages / compilers course. It's a lexer, parser, and typechecker for a small statically-typed language with structs, traits, and trait implementations (basically interfaces).

Pipeline: source code -> tokens -> AST -> typechecked program.

## Features

- Structs with typed fields
- Traits + trait implementations (`impl Trait for Type`)
- `Self` type support inside implementations
- Functions, methods, higher-order function types
- `if`/`else`, `while`, `break`, `return`
- Arithmetic/comparison/equality expressions with proper precedence
- `let` bindings, assignment, `println`

## Running it

Needs Python 3.10+.

```bash
python lexer.py path/to/source.txt        # tokenize
python parser.py path/to/source.txt       # parse, print AST
python typechecker.py path/to/source.txt  # typecheck
```

## Tests

```bash
pip install pytest
pytest
```

246 tests across the lexer, parser, and typechecker (including error cases like bad tokens, type mismatches, undeclared variables, etc).

## Limitations

- No generics besides `Self`
- No arrays/lists/collections
- No modules, single file only
- No error recovery — stops at the first error

## Files

- `lexer.py` / `lexer_test.py`
- `parser.py` / `parser_test.py`
- `nodes.py` — AST definitions
- `typechecker.py` / `typechecker_test.py`

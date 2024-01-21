Ally
- Parsers written with parser combinators give us the grammar for free.
- Fuzzing programs where the input must be parsed is hard because most random inputs fail, we get path explosion with symbolic fuzzing, or if have a grammar, it's hard to test if the program conforms to the grammar.
- Programs with inputs that are parsed with parser combinators give us an efficient way of fuzzing inputs.
- thoughts? 

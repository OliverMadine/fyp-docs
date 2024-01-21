Ally
- Fuzzing programs where the input must be parsed is hard
    - Most random inputs fail
    - We get path explosion with symbolic fuzzing
    - Expected grammar may deviated from grammar encoded into the parser
- Parsers written with parser combinators are strongly-typed.
    - We can generated inputs based on the structure of these parsers
    - We effectively get the grammar of the parser for free.
- Grammar based fuzzing
    - We don't know if the expected grammar deviates from the actual grammar encoded into the aprser

Conclusion: Programs using parser combinators give us an efficient way of fuzzing inputs.
- thoughts?

- benefits vs grammar based
    - grammar might not be correctly implemented
    - grammar extraction not required (inherent to parser combinators)
    - grammar is often not machine readable (converting is time consuming)

Questions
- benefits of this vs generating inputs by looking at the AST?
- benefits of this vs looking at the Parse tree?
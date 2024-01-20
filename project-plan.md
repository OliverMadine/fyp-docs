# Project Plan

## Part 1

1. how do we prevent flagging the same bug twice?
2. Fuzzing takes ages (so implement faster)
3. compute power?

### v0
- Testing framework
- Implement Arbitrary for basic parsers
- Add quickCheck for simple property

### v1
- Implement Arbitrary for more parsers

### v2
- Implement more properties
- Perhaps using quickSpec

### v3
- Write generator for random parser inputs structured using the Arbitrary parsers

## Part 2: Differential Testing with Parsely

### v0
- Basic interfacing with Scala through Haskell

### v1
- Forming basic parsers in Scala through Haskell

### v2
- Retrieving parse result from Scala

### v3
- Forming more parsers in Scala

### v4
- Differential testing

## Part 3: Eval

- Testing if any bugs are triggered by real parsers (e.g. wacc compilers)
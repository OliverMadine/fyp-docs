Fuzzing is a process by which a system is randomly tested by feeding it usually malformed inputs designed to make it crash or behave in a way it was not intended to. This can uncover vulnerabilities or bugs within a system. Parser combinators are a popular functional approach for compositionally writing parsers. They usually have a strongly-typed API, with individual components being combined with combinators. With no particularly rigid syntactic description, it is possible to synthesise random parsers easily -- not that you'd expect their behaviours to be at all sensible. Every year, the parser combinator Parsley is stress tested by a team of expert manual fuzzers called second-year students. When these testers are let loose on the library, they will often inadvertently find the most obscure of bugs purely by going about their business. While parsley has become increasingly stable as the years go by, any refactorings to the system can introduce bugs, and large-scale reworks or optimisations become increasingly less attractive as a result.



This project aims to perform randomised fuzzing on Parsley to establish an additional test suite that can be used to help ensure that the library remains stable even during additional refactoring or optimisation. This will mean a few different things:

* Creating a mechanism to randomly generate both parsers and candidate input strings in a type-safe way.
* Annotating the library with additional assertions to help catch not only hard crashes for mishandled cases, but also to ensure that the invariances of the system are maintained and no assumptions have been invalidated -- note that no assumptions can ever be made about the nature of the parsers written, since they can be entirely arbitrary: this is something we are trying to test for!
* Leverage known parser combinator laws to tweak the implementations of parsers and ensure that they still behave identically post-transformation on the same random inputs.
* Stress the optimisations parsley already performs by disabling them within example parsers to ensure the behaviour is extrinsically the same.
* Perhaps trying to synthesise parsers and their input in a more structured way, so that we can reason about what behaviours the input strings should evoke in the parser: this way, these behaviours themselves can be tested thoroughly and inputs may have better overall coverage (it may not be possible to do this, or only in a limited way: this is a stretch goal)
* Use this system to identify bugs within Parsley, or at the very least identify former bugs that the "expert fuzzers" have previously found in older versions.


Requirements

Knowledge of parser combinators is desirable, but may not be necessary. In this case, a good background in functional programming will be of a definite advantage.

Knowledge of randomised testing frameworks like Haskell's Quickcheck or Scala's Scalacheck is an advantage, but not necessary.

Knowledge of Scala is an advantage, but not necessary.
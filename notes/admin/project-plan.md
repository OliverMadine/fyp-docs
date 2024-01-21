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


# GPT planning suggestions

1. **Ethics**:
   - Research the ethical considerations relevant to your project.

2. **Project Goals and Limitations**:
   - Suggest and think about potential project goals.
   - Consider any limitations of your project.

3. **Documentation**:
   - Start documenting your work.
   - Maintain thorough records of your progress and findings.

4. **Questions for Supervisor**:
   - Track questions you might have for your supervisor.

5. **Timeline Planning**:
   - Plan a timeline for your project.
   - Set key milestones and deadlines.

6. **Literature Review**:
   - Begin reading and understanding existing literature related to fuzzing and parser combinators.

7. **Practice Using Libraries**:
   - Get hands-on experience with Gigaparsec and Parsley.

8. **Hardware Requirements**:
   - Assess the hardware requirements for your project.
   - Ensure access to necessary computational resources, especially for heavy processing or large-scale fuzzing.

9. **Performance Metrics**:
   - Define clear metrics for evaluating the success and effectiveness of your fuzzing techniques.
   - Plan for benchmarking and performance evaluation throughout your project.

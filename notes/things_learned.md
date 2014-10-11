## Things Learned, ML

 1. Let (defining local variables; Lecture 2-11)

   * `let <bindings> in <expression> end`
   * `e`:
     * provides type of whole expression
     * "body" of expression
     * bindings are recognized only within `e`
   * scope: binding within an environment

 1. Lists (Lecture 2-9)

   * all elements have the same type
   * unlike tuples, datatype does not commit to a particular cardinality
   * type `t list` describes lists of type `t`
   * `[]`
     * zero-length ("empty") list
     * type of empty list: "alpha list" (`'a list`), meaning list the type of whose elements is still undefined
   * `e1::e2`: "cons" (construct) new list, `[e1, <e2>]`
     * `e1` has type `t`
     * `e2` has type `t list`
   * `null`: function to test whether following expression is an empty list or not
   * 'hd e`: 
     * returns first element of 'e'
     * `hd` has type `'a`
   * 'tl e`: 
     * returns all non-first elements of 'e' — `[]` is the last element
     * `tl` has type `'a list`

 1. Pairs (2-tuples; Lecture 2-8)

   * three questions to ask about a data-type: 
     * syntax, 
     * evaluation, 
     * type-checking

   * value: something that is done evaluating

   * `div`: division operator
   * `mod`: modulus operator

   * `pr`: pair: 2-tuple
   * field: 
   * list
   * `#`: indexing operator. `#1 e`: expression 1 of pair `e`
   * `*`: operator dividing types in type-checking expression
   * function syntax:

        ```
fun <name> (<arguments>) =
    return value
        ```


 1. Early material
   * `~`: unary minus (distinct from `-` for subtraction operator)
   * In REPL, must `use` program first and only then `use` the test suite for i t.
   * Test functions involve two `=` signs: e.g., `val test2 = double 0 = 0`.
   * Comments are noted with `(* ... *)`.
   * "Semantics" includes type-checking and evaluation.
   * "static" vs. "dynamic" environments.
   * ' Every value “evaluates to itself” in “zero steps”. '
   * `()` has type `unit`.
   * "shadowing": re-binding an already bound variable
   * "binding" vs. "assignment"

[end]

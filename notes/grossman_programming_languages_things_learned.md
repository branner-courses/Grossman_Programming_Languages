## Things Learned, ML

 1. Pieces of a language (Lecture 2-18):

   2. What is necessary for programming:

     3. syntax
     3. semantics (evaluation rules)
     3. idioms
     3. libraries
     3. tools — not part of the language

   2. This course focuses on semantics and idioms.

 1. No mutation (Lecture 2-16, 17)

   * Immutability is a basic feature of functional programming.
   * Lists are passed by reference ("aliasing") but since they are immutable, the problems in Python do not arise.

 1. Booleans and Comparison Operations (Lecture 2-15)
 
   * keyword `orelse` ()
   * `not` is a (boolean) function, unlike `orelse` and `andalso`
   * `not`, `orelse`, and `andalso` can all be expressed using `if`-`then`-`else` blocks, but "using more concise forms is generally considered better style.
   * `<>` is "not equal to`
   * comparison operators cannot be used to compare an `int` and a `real`; use `fromInt` to convert `int` to `real` first
   * `=` and `<>` cannot be used with `real`s.

 1. Options (Lecture 2-14)

   * example of computing the `max` of an empty list
   * `t option` is a type for any `t`
     * `NONE`: has type `'a option`
     * `SOME e`: has type `t option` if `e` has type `t
     * `isSome`: has type `'a option -> bool`
     * `valOf`: has type `'a option -> 'a`
   * These allow us to eliminated base cases when a list is empty, as in the example.
   * keyword `andalso`

 1. Let expressions to avoid repeated recursion (Lecture 2-13)

 1. Nested functions (Lecture 2-12)

   * "private"-like functions can be defined nestedly, within `let` expressions:

        let <function definition>
        in <function that calls it>
        end

   * functions can use bindings in the environment where they are defined — both bindings from "outer" environments as well as earlier bindings in the let-expression.

 1. Let (defining local variables; Lecture 2-11)

   * `let <bindings> in <expression> end`
   * `e`:
     * provides type of whole expression
     * "body" of expression
     * bindings are recognized only within `e`
   * scope: binding within an environment

 1. List functions (Lecture 2-10)

   * in dealing with list, consider 1) empty list (using `null <list name>` and 

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
2) non-empty list

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
   * 'Every value “evaluates to itself” in “zero steps”.'
   * `()` has type `unit`.
   * "shadowing": re-binding an already bound variable
   * "binding" vs. "assignment"

[end]

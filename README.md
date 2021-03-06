

A scheme interpreter in Haskell

[![Build Status](https://travis-ci.org/quakehead/haskell-scheme.svg?branch=master)](https://travis-ci.org/quakehead/haskell-scheme)


Going over [Write Yourself a Scheme in 48 Hours](https://en.wikibooks.org/wiki/Write_Yourself_a_Scheme_in_48_Hours) as mostly a learning experience, deviating at some points and adding small new futures along the way.


* Currently supported builtins:
    - supports arithmatic expressions with integers `+, -, *, /, ^, mod, quotient, remainder`
    - comparision operators: `=, >, >, /=, >=, <=` and `string*?` where * is `=, <, >`
    - type tests: `string?, number?, symbol?`
    - boolean operatiors: `&&`, `||`
    - `if` statements
    
## Bugs

* Bugs in parsing
    - having spaces before and end parenthesis causes a parse error. This may be because of the use of SepBy
    - number bases for integer literals doesn't parse since it collides with boolean literals. (e.g. `#xF00D`)
        - possible fix is to parse literals starting with `#` in the same function.



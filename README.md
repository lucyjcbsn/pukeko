# pukeko
terrible, horrible, no-good, very bad compiled programming language

Every standard pukeko keyword and type (excluding some typesets) is the size of 2 characters.
Pukeko has a multilayered type system, where certain types require subtypes.
Typesets maintain simplicity and readability, reducing need for having more types in the global environment.
Typesets can be predefined (for example a nu ~long would be a 32 bit integer), or if a possibility, have their size defined (nu ~32 would be a 32 bit int)
Typesets may also be defined automatically on compile time (nu A = 255; would be an 8 bit unsigned integer, whereas nu A = 256; would be 16 bits)

KEYWORDS
    fn . define a function
    rt . return
    cs . define as constant
    gl . define as global // by default all variables are local
    if . if statement
    sw . switch statement
    wl . while loop
    fr . for loop
    st . structure // by default stores data in a list, when defined with the typeset "ns", behaves like a namespace
    lk . import another pukeko file
TYPES
    nu . arbitrary number
    ch . arbitrary character
    bl . boolean
    "~" . defines a value as a typeset
OPERATORS
    "+" . add
    "-" . subtract
    "*" . multiply
    "/" . divide
    "=" . equals
    "==" . if equals
    "()" . result of an operation, or arguments for a function

Examples

FUNCTION

fn nu AddNumbers(nu A, nu B){
    nu C = (A + B)
    return C
}

IF/SWITCH/WHILE/FOR

if (N == true) {
    // do something
}

while (N == true) {
    // do a thing
}

for () {}

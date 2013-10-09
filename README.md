is2
===
is2 is a type-checking module for node.js to test values. Is does not throw exceptions and every function only returns true or false. Use is2 to validate types in your node.js code. Every function in is2 returns either true of false.

After finding Enrico Marino's module is, the concise syntax amazed, but there were syntax issues that made using is difficult. This fork of is fixes those issues, but the module is no longer cross-platform. Also, added tests via mocha which can be run using 'npm test'.

## Installation
To install is2, type:

    $ npm install is2

## Usage

    var is = require('is2');

    console.log('true is equal to 1===1: '+(is.equal(true, 1===1));
    console.log('10 is a positive number: '+(is.positiveNumber(10));
    console.log('11 is an odd number: '+(is.oddNumber(11));

## API

### type(value, type)

Test if 'value' is a type of 'type'.
Alias: a

#### Params: 

* **value** *value* to test.

* **String** *type* THe name of the type.

#### Return:

* **Boolean** true if 'value' is an arguments object, false otherwise.

### defined(value)

Test if 'value' is defined.
Alias: def

#### Params: 

* **Any** *value* The value to test.

#### Return:

* **Boolean** true if 'value' is defined, false otherwise.

### nullOrUndef(value)

Test is 'value' is either null or undefined.
Alias: nullOrUndef

#### Params: 

* **Any** *value* value to test.

#### Return:

* **Boolean** True if value is null or undefined, false otherwise.

### empty(value)

Test if 'value' is empty. To be empty means to be an array, object or string with nothing contained.

#### Params: 

* **Any** *value* value to test.

#### Return:

* **Boolean** true if 'value' is empty, false otherwise.

### objEquals(value, other)

Do a deep comparision of two objects for equality. Will recurse without any limits. Meant to be
called by equal only.

#### Params: 

* **Object** *value* The first object to compare.

* **Object** *other* The second object to compare.

#### Return:

* **Boolean** true, if the objects are equivalent, false otherwise.

### equal(value, other)

Test if 'value' is equal to 'other'. Works for objects and arrays and will do deep comparisions,
using recursion.
Alias: eq

#### Params: 

* **Any** *value* value.

* **Any** *other* value to compare with.

#### Return:

* **Boolean** true if 'value' is equal to 'other', false otherwise

### NON_HOST_TYPES

JS Type definitions which cannot host values.

### hosted(value, host)

Test if 'key' in host is an object. To be hosted means host[value] is an object.

#### Params: 

* **Any** *value* The value to test.

* **Any** *host* Host that may contain value.

#### Return:

* **Boolean** true if 'value' is hosted by 'host', false otherwise.

### instanceOf(value)

Test if 'value' is an instance of 'constructor'.
Aliases: instOf, instanceof

#### Params: 

* **Any** *value* value to test.

#### Return:

* **Boolean** true if 'value' is an instance of 'constructor'.

### buffer(value)

Test if 'value' is an instance of Buffer.
Aliases: instOf, instanceof

#### Params: 

* **Any** *value* value to test.

#### Return:

* **Boolean** true if 'value' is an instance of 'constructor'.

### null(value)

Test if 'value' is null.

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is null, false otherwise.

### undefined(value)

Test if 'value' is undefined.
Aliases: undef, udef

#### Params: 

* **Any** *value* value to test.

#### Return:

* **Boolean** true if 'value' is undefined, false otherwise.

### arguments(value)

Test if 'value' is an arguments object.
Alias: args

#### Params: 

* **Any** *value* value to test

#### Return:

* **Boolean** true if 'value' is an arguments object, false otherwise

### emptyArguments(value)

Test if 'value' is an arguments object that is empty.
Alias: args

#### Params: 

* **Any** *value* value to test

#### Return:

* **Boolean** true if 'value' is an arguments object with no args, false otherwise

### array(value)

Test if 'value' is an array.
Alias: ary, arry

#### Params: 

* **Any** *value* value to test.

#### Return:

* **Boolean** true if 'value' is an array, false otherwise.

### nonEmptyArray(value)

Test if 'value' is an array containing at least 1 entry.
Aliases: nonEmptyArry, nonEmptyAry

#### Params: 

* **Any** *value* The value to test.

#### Return:

* **Boolean** true if 'value' is an array with at least 1 value, false otherwise.

### nonEmptyArray(value)

Test if 'value' is an array containing no entries.
Aliases: emptyArry, emptyAry

#### Params: 

* **Any** *value* The value to test.

#### Return:

* **Boolean** true if 'value' is an array with no elemnets.

### empty(value)

Test if 'value' is an empty array(like) object.
Aliases: arguents.empty, args.empty, ary.empty, arry.empty

#### Params: 

* **Any** *value* value to test.

#### Return:

* **Boolean** true if 'value' is an empty array(like), false otherwise.

### arrayLike(value)

Test if 'value' is an arraylike object (i.e. it has a length property with a valid value)
Aliases: arraylike, arryLike, aryLike

#### Params: 

* **Any** *value* value to test.

#### Return:

* **Boolean** true if 'value' is an arguments object, false otherwise.

### boolean(value)

Test if 'value' is a boolean.
Alias: bool

#### Params: 

* **Any** *value* value to test.

#### Return:

* **Boolean** true if 'value' is a boolean, false otherwise.

### false(value)

Test if 'value' is false.

#### Params: 

* **Any** *value* value to test.

#### Return:

* **Boolean** true if 'value' is false, false otherwise

### true(value)

Test if 'value' is true.

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is true, false otherwise.

### date(value)

Test if 'value' is a date.

#### Params: 

* **Any** *value* value to test.

#### Return:

* **Boolean** true if 'value' is a date, false otherwise.

### error(value)

Test if 'value' is an error object.
Alias: err

#### Params: 

* **value** *value* to test.

#### Return:

* **Boolean** true if 'value' is an error object, false otherwise.

### function(value)

Test if 'value' is a function.
Alias: func

#### Params: 

* **Any** *value* value to test.

#### Return:

* **Boolean** true if 'value' is a function, false otherwise.

### number(value)

Test if 'value' is a number.
Alias: num

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is a number, false otherwise.

### positiveNumber(value)

Test if 'value' is a positive number.
Alias: positiveNum, posNum

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is a number, false otherwise.

### negativeNumber(value)

Test if 'value' is a negative number.
Aliases: negNum, negativeNum

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is a number, false otherwise.

### decimal(value)

Test if 'value' is a decimal number.
Aliases: decimalNumber, decNum

#### Params: 

* **Any** *value* value to test.

#### Return:

* **Boolean** true if 'value' is a decimal number, false otherwise.

### divisibleBy(value, n)

Test if 'value' is divisible by 'n'.
Alias: divisBy

#### Params: 

* **Number** *value* value to test.

* **Number** *n* dividend.

#### Return:

* **Boolean** true if 'value' is divisible by 'n', false otherwise.

### int(value)

Test if 'value' is an integer.
Alias: integer

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is an integer, false otherwise.

### positiveInt(value)

Test if 'value' is a positive integer.
Alias: posInt

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is a positive integer, false otherwise.

### negativeInt(value)

Test if 'value' is a negative integer.
Aliases: negInt, negativeInteger

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is a negative integer, false otherwise.

### maximum(value, others)

Test if 'value' is greater than 'others' values.
Alias: max

#### Params: 

* **Number** *value* value to test.

* **Array** *others* values to compare with.

#### Return:

* **Boolean** true if 'value' is greater than 'others' values.

### minimum(value, others)

Test if 'value' is less than 'others' values.
Alias: min

#### Params: 

* **Number** *value* value to test.

* **Array** *others* values to compare with.

#### Return:

* **Boolean** true if 'value' is less than 'others' values.

### nan(value)

is.nan
Test if `value` is not a number.

#### Params: 

* **Mixed** *value* value to test

#### Return:

* **Boolean** true if `value` is not a number, false otherwise

### even(value)

Test if 'value' is an even number.

#### Params: 

* **Number** *value* to test.

#### Return:

* **Boolean** true if 'value' is an even number, false otherwise.

### odd(value)

Test if 'value' is an odd number.

#### Params: 

* **Number** *value* to test.

#### Return:

* **Boolean** true if 'value' is an odd number, false otherwise.

### ge(value, other)

Test if 'value' is greater than or equal to 'other'.
Aliases: greaterOrEq, greaterOrEqual

#### Params: 

* **Number** *value* value to test.

* **Number** *other* value to compare with.

#### Return:

* **Boolean** true, if value is greater than or equal to other, false otherwise.

### gt(value, other)

Test if 'value' is greater than 'other'.
Aliases: greaterThan

#### Params: 

* **Number** *value* value to test.

* **Number** *other* value to compare with.

#### Return:

* **Boolean** true, if value is greater than other, false otherwise.

### le(value, other)

Test if 'value' is less than or equal to 'other'.
Alias: lessThanOrEq, lessThanOrEqual

#### Params: 

* **Number** *value* value to test

* **Number** *other* value to compare with

#### Return:

* **Boolean** true, if 'value' is less than or equal to 'other', false otherwise.

### lt(value, other)

Test if 'value' is less than 'other'.
Alias: lessThan

#### Params: 

* **Number** *value* value to test

* **Number** *other* value to compare with

#### Return:

* **Boolean** true, if 'value' is less than 'other', false otherwise.

### within(value, start, finish)

Test if 'value' is within 'start' and 'finish'.
Alias: withIn

#### Params: 

* **Number** *value* value to test.

* **Number** *start* lower bound.

* **Number** *finish* upper bound.

#### Return:

* **Boolean** true if 'value' is is within 'start' and 'finish', false otherwise.

### object(value)

Test if 'value' is an object. Note: Arrays, RegExps, Date, Error, etc all return false.
Alias: obj

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is an object, false otherwise.

### nonEmptyObject(value)

Test if 'value' is an object with properties. Note: Arrays are objects.
Alias: nonEmptyObj

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is an object, false otherwise.

### objectInstanceof(objInst, objType)

Test if 'value' is an instance type objType.
Aliases: objInstOf, objectinstanceof, instOf, instanceOf

#### Params: 

* **object** *objInst* an object to testfor type.

* **object** *objType* an object type to compare.

#### Return:

* **Boolean** true if 'value' is an object, false otherwise.

### regexp(value)

Test if 'value' is a regular expression.
Alias: regexp

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is a regexp, false otherwise.

### string(value)

Test if 'value' is a string.
Alias: str

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is a string, false otherwise.

### emptyString(value)

Test if 'value' is an empty string.
Alias: emptyStr

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is am empty string, false otherwise.

### nonEmptyString(value)

Test if 'value' is a non-empty string.
Alias: nonEmptyStr

#### Params: 

* **Any** *value* to test.

#### Return:

* **Boolean** true if 'value' is a non-empty string, false otherwise.


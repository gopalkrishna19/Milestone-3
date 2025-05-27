* def a = cellValue1
* def b = cellValue2

# Check if both are numbers
* def isNumeric = function(x) { return !isNaN(x) && x !== null && x !== true && x !== false }
* def result = isNumeric(a) && isNumeric(b) ? karate.match(karate.toNumber(a), karate.toNumber(b)) : karate.match(a, b)

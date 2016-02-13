# Clean Code

## Boolean Assignments
```javascript
// Dirty
var buyIceCream;

if (money > 5) {
 buyIceCream = true;
} else {
 buyIceCream = false;
}

// Clean
var buyIceCream = money > 5;
```

## Ternary
```javascript
// Dirty
var transportCost;

if (isStudent) {
 transportCost = 5;
} else {
 transportCost = 10;
}

// Clean
var transportCost = isStudent? 5 : 10;
```

## Positive Conditional
```javascript
// Dirty
if (!isNotStudent) ...
if (!isNotLoggedIn) ...

// Clean
if (isStudent) ...
if (loggedIn) ...
```

## String Conditional
Awesome for language that supports Enum
```javascript
// Dirty
if (profession == 'teacher')

// Clean
if (profession == ProfessionType.teacher)
```

## Magic Numbers
```javascript
// Dirty
if (status === 2) ...
if (score > 70) ...

// Clean
const PUBLISH = 2;
if (status === PUBLISH) ...

const MIN_SCORE_TO_PASS = 70;
if (score > MIN_SCORE_TO_PASS
```
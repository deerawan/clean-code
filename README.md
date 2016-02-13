# Clean Code

## Conditionals

### Boolean Assignments
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

### Ternary
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

### Positive Conditional
```javascript
// Dirty
if (!isNotStudent) ...
if (!isNotLoggedIn) ...

// Clean
if (isStudent) ...
if (loggedIn) ...
```

### String Conditional
```javascript
// Dirty
if (profession == 'teacher')

// Clean
if (profession == ProfessionType.teacher)
```

### Magic Numbers
```javascript
// Dirty
if (status == 2) ...

// Dirty
if (score > 70) ...

// Clean
var status = {
  active: 2
};
if (status == status.active) ...

// Clean
const MIN_SCORE_TO_PASS = 70;
if (score > MIN_SCORE_TO_PASS) ...
```

### Complex Conditionals
```javascript
// Dirty
if (employee.age > 55 && employee.yearsEmployed > 10) ...

// Clean
var eligibleForPension = employee.age > minRetirementAge &&
    employee.yearsEmployed > minPensionEmploymentYears;
if (eligibleForPension) ...
```

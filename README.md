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
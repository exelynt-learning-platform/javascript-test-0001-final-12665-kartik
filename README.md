# javascript-test-0001-final-12665-kartik

Final Project Assignment - This repository contains the complete final project code and documentation.

---

## Problem Statement

Write a JavaScript program to print the following hollow diamond pattern:

```
    *
   * *
  *   *
 *     *
*       *
 *     *
  *   *
   * *
    *
```

---

## Solution

**File:** `result.js`

The solution uses a `hollowDiamond(n)` function where `n` controls the size of the diamond.

### How It Works

The diamond has `2n - 1` rows total, split into two halves:

- **Upper half** (rows `1` to `n`): Each row expands in width. Leading spaces decrease, and the row width (`2i - 1`) increases with each row `i`.
- **Lower half** (rows `n-1` down to `1`): Each row contracts in width, mirroring the upper half.

For every row, only the **first** and **last** characters are printed as `*`; the interior is filled with spaces, making the diamond **hollow**. The top and bottom rows (single star) are a natural result of `2*1 - 1 = 1`.

### Algorithm

```
for each row i from 1 to n (upper half):
    print (n - i) leading spaces
    print * at position 1 and 2i-1, spaces in between

for each row i from n-1 down to 1 (lower half):
    print (n - i) leading spaces
    print * at position 1 and 2i-1, spaces in between
```

---

## How to Run

Make sure [Node.js](https://nodejs.org/) is installed, then run:

```bash
node result.js
```

### Verify Node.js is installed

```bash
node -v
```

---

## Customization

Change the argument passed to `hollowDiamond()` at the bottom of `result.js` to resize the diamond:

```js
hollowDiamond(5); // 9-row diamond (default)
hollowDiamond(7); // 13-row diamond
```

---

## File Structure

```
├── result.js   # Main JavaScript solution
└── README.md   # Project documentation
```


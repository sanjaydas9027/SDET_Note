Absolutely! Here’s a **complete reference for JavaScript `Set`** with **examples, outputs, and use cases** — similar to your Array and Map references.

---

# **JavaScript Set**

A `Set` is a **collection of unique values**. It **does not allow duplicates** and **maintains insertion order**.

### **When to Use a Set**

* Track executed test cases in automation.
* Collect unique values (e.g., error messages, user IDs).
* Remove duplicates from an array.
* Store unique objects, strings, or numbers for quick lookup.

---

## **1. How to Declare a Set**

```javascript
// Empty Set
let mySet = new Set();

// Set with initial values
let setWithValues = new Set([1, 2, 3, 2]);
console.log(setWithValues); // Set { 1, 2, 3 } (duplicates removed)
```

---

## **2. Set Methods with Examples**

### **1. `add(value)`**

Adds a new value to the set.

```javascript
let set = new Set();
set.add("TC01");
set.add("TC02");
set.add("TC01");  // duplicate ignored
console.log(set); 
// Output: Set { 'TC01', 'TC02' }
```

---

### **2. `has(value)`**

Checks if a value exists in the set.

```javascript
console.log(set.has("TC01")); // true
console.log(set.has("TC03")); // false
```

---

### **3. `delete(value)`**

Removes a value from the set.

```javascript
set.delete("TC02");
console.log(set); 
// Output: Set { 'TC01' }
```

---

### **4. `clear()`**

Removes all values from the set.

```javascript
set.clear();
console.log(set); 
// Output: Set {}
```

---

### **5. `size`**

Returns the number of unique values in the set.

```javascript
let s = new Set([1, 2, 2, 3]);
console.log(s.size); 
// Output: 3
```

---

### **6. `forEach(callback)`**

Executes a callback for each value in the set.

```javascript
s.forEach(value => console.log(value));
// Output: 
// 1
// 2
// 3
```

---

### **7. `values()`**

Returns an iterator of all values.

```javascript
console.log([...s.values()]); 
// Output: [1, 2, 3]
```

---

### **8. `keys()`**

Same as `values()` (for compatibility).

```javascript
console.log([...s.keys()]); 
// Output: [1, 2, 3]
```

---

### **9. `entries()`**

Returns an iterator of `[value, value]` pairs (for compatibility with Map).

```javascript
console.log([...s.entries()]); 
// Output: [ [1,1], [2,2], [3,3] ]
```

---

## **3. Practical Use Cases in Test Automation**

```javascript
// Track executed test cases
let executedTests = new Set();
executedTests.add("TC01");
executedTests.add("TC02");
executedTests.add("TC01"); // ignored

console.log(executedTests.has("TC02")); // true
console.log(executedTests.size);        // 2

// Remove duplicates from an array
let arr = [1,2,2,3,3,3];
let uniqueArr = [...new Set(arr)];
console.log(uniqueArr); // [1,2,3]
```

---

### **Quick Summary Table**

| Method / Property | Description           | Example Output                             |
| ----------------- | --------------------- | ------------------------------------------ |
| `add(value)`      | Adds a value          | `set.add("a")` → Set {'a'}                 |
| `has(value)`      | Checks existence      | `set.has("a")` → true                      |
| `delete(value)`   | Removes value         | `set.delete("a")` → true                   |
| `clear()`         | Removes all values    | `set.clear()` → Set {}                     |
| `size`            | Number of values      | `set.size` → 3                             |
| `forEach(cb)`     | Loop through values   | prints all values                          |
| `values()`        | Iterator of values    | `[...set.values()]` → [1,2,3]              |
| `keys()`          | Same as `values()`    | `[...set.keys()]` → [1,2,3]                |
| `entries()`       | `[value,value]` pairs | `[...set.entries()]` → [[1,1],[2,2],[3,3]] |

---

If you want, I can now **make a similar full sheet for `Object` with all methods + examples + outputs + use cases**.

Do you want me to do that next?

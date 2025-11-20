Sure! Here’s a **complete reference for JavaScript `Map`** — including **how to declare**, **all main methods**, **examples**, and **outputs**. I’ll keep it clear and concise so it’s easy to use as a reference.

---

# **JavaScript Map**

A `Map` is a **collection of key–value pairs**. Keys can be **any type** (string, number, object, function, etc.), and insertion order is **preserved**.

---

## **1. How to Declare a Map**

```javascript
// Empty Map
let myMap = new Map();

// Map with initial values
let mapWithValues = new Map([
  ['name', 'John'],
  ['age', 30],
  ['role', 'QA']
]);

console.log(myMap);         // Map(0) {}
console.log(mapWithValues); // Map(3) { 'name' => 'John', 'age' => 30, 'role' => 'QA' }
```

---

## **2. Map Methods with Examples**

### **1. `set(key, value)`**

Adds or updates a key–value pair.

```javascript
let map = new Map();
map.set('TC01', 'Passed');
map.set('TC02', 'Failed');
console.log(map);
// Map(2) { 'TC01' => 'Passed', 'TC02' => 'Failed' }
```

---

### **2. `get(key)`**

Returns the value associated with a key.

```javascript
console.log(map.get('TC01')); // Passed
console.log(map.get('TC03')); // undefined
```

---

### **3. `has(key)`**

Checks if a key exists in the map. Returns `true` or `false`.

```javascript
console.log(map.has('TC02')); // true
console.log(map.has('TC03')); // false
```

---

### **4. `delete(key)`**

Removes a key–value pair from the map.

```javascript
map.delete('TC02');
console.log(map); // Map(1) { 'TC01' => 'Passed' }
```

---

### **5. `clear()`**

Removes all entries from the map.

```javascript
map.clear();
console.log(map); // Map(0) {}
```

---

### **6. `size`**

Returns the number of entries in the map.

```javascript
let m = new Map([['a',1], ['b',2]]);
console.log(m.size); // 2
```

---

### **7. `keys()`**

Returns an iterator of all keys.

```javascript
let keys = [...m.keys()];
console.log(keys); // ['a','b']
```

---

### **8. `values()`**

Returns an iterator of all values.

```javascript
let values = [...m.values()];
console.log(values); // [1,2]
```

---

### **9. `entries()`**

Returns an iterator of `[key, value]` pairs.

```javascript
let entries = [...m.entries()];
console.log(entries); // [ ['a',1], ['b',2] ]
```

---

### **10. `forEach(callback)`**

Executes a callback for each `[key, value]` pair.

```javascript
m.forEach((value, key) => {
  console.log(`${key} => ${value}`);
});
// Output:
// a => 1
// b => 2
```

---

## **3. Map with Object or Function as Keys**

```javascript
let objKey = { id: 1 };
let funcKey = () => {};

let complexMap = new Map();
complexMap.set(objKey, "Object Value");
complexMap.set(funcKey, "Function Value");

console.log(complexMap.get(objKey));   // Object Value
console.log(complexMap.get(funcKey));  // Function Value
```

---

## **4. Quick Summary Table**

| Method           | Description             | Example Output                           |
| ---------------- | ----------------------- | ---------------------------------------- |
| `set(key,value)` | Add or update           | `map.set('a',1)` → Map { 'a'=>1 }        |
| `get(key)`       | Get value               | `map.get('a')` → 1                       |
| `has(key)`       | Check existence         | `map.has('b')` → true/false              |
| `delete(key)`    | Remove key              | `map.delete('a')` → true                 |
| `clear()`        | Remove all entries      | `map.clear()` → Map(0) {}                |
| `size`           | Number of entries       | `map.size` → 2                           |
| `keys()`         | Iterator of keys        | `[...map.keys()]` → ['a','b']            |
| `values()`       | Iterator of values      | `[...map.values()]` → [1,2]              |
| `entries()`      | Iterator of [key,value] | `[...map.entries()]` → [['a',1],['b',2]] |
| `forEach(cb)`    | Loop through map        | prints all key-value pairs               |

---

If you want, I can also create a **similar full reference sheet for `Set`** with **all methods + examples + outputs**, just like this Map sheet.

Do you want me to do that next?

Perfect! Here’s a **full JavaScript `Object` reference sheet** with **methods, examples, outputs, and use cases**, similar to your Array, Map, and Set sheets.

---

# **JavaScript Object**

A JavaScript **Object** stores **key–value pairs**, where keys are **strings or symbols** and values can be **any type**.

### **When to Use Objects**

* Store **static test data** (e.g., API payloads, page locators).
* Represent JSON data for API testing.
* Store **configurations, user details, or metadata**.
* Track properties of entities in test automation (like test case metadata).

---

## **1. How to Declare an Object**

```javascript
// Empty object
let obj = {};

// Object with values
let user = {
  name: "Alice",
  role: "QA",
  id: 101
};

console.log(obj);  // {}
console.log(user); // { name: 'Alice', role: 'QA', id: 101 }
```

---

## **2. Object Methods with Examples**

### **1. `Object.keys(obj)`**

Returns an array of keys.

```javascript
console.log(Object.keys(user)); 
// Output: ['name', 'role', 'id']
```

---

### **2. `Object.values(obj)`**

Returns an array of values.

```javascript
console.log(Object.values(user)); 
// Output: ['Alice', 'QA', 101]
```

---

### **3. `Object.entries(obj)`**

Returns an array of `[key, value]` pairs.

```javascript
console.log(Object.entries(user)); 
// Output: [['name','Alice'], ['role','QA'], ['id',101]]
```

---

### **4. `Object.assign(target, source)`**

Copies properties from one object to another.

```javascript
let obj1 = { a: 1 };
let obj2 = { b: 2 };
let merged = Object.assign({}, obj1, obj2);
console.log(merged); 
// Output: { a: 1, b: 2 }
```

---

### **5. `Object.freeze(obj)`**

Prevents modification of object properties.

```javascript
Object.freeze(user);
user.name = "Bob";  // Ignored
console.log(user.name); 
// Output: Alice
```

---

### **6. `Object.seal(obj)`**

Prevents adding/removing properties, but allows modifying existing ones.

```javascript
let obj3 = { x: 1 };
Object.seal(obj3);
obj3.x = 100;  // Allowed
delete obj3.x; // ❌ Not allowed
console.log(obj3); 
// Output: { x: 100 }
```

---

### **7. `Object.hasOwn(obj, key)`**

Checks if the object has a property as its own (not inherited).

```javascript
console.log(Object.hasOwn(user, 'role')); // true
console.log(Object.hasOwn(user, 'salary')); // false
```

---

### **8. `delete obj.key`**

Removes a property from the object.

```javascript
delete user.id;
console.log(user); 
// Output: { name: 'Alice', role: 'QA' }
```

---

### **9. `Object.create(proto)`**

Creates a new object with the given prototype.

```javascript
let proto = { greet: () => "Hello" };
let child = Object.create(proto);
console.log(child.greet()); 
// Output: Hello
```

---

### **10. `Object.fromEntries(array)`**

Converts an array of `[key, value]` pairs into an object.

```javascript
let arr = [['name','Alice'], ['role','QA']];
let newObj = Object.fromEntries(arr);
console.log(newObj); 
// Output: { name: 'Alice', role: 'QA' }
```

---

## **3. Practical Use Cases in Test Automation**

```javascript
// Store API test data
let testData = {
  endpoint: "/login",
  method: "POST",
  payload: { user: "alice", password: "12345" }
};

// Access keys and values
console.log(Object.keys(testData));   // ['endpoint','method','payload']
console.log(Object.values(testData)); // ['/login','POST',{user:'alice',password:'12345'}]

// Merge objects
let additionalData = { headers: { Authorization: "Bearer token" } };
let finalData = Object.assign({}, testData, additionalData);
console.log(finalData);

// Check property existence
console.log(Object.hasOwn(finalData, "method")); // true
```

---

## **4. Quick Summary Table**

| Method / Property               | Description                              | Example Output                        |
| ------------------------------- | ---------------------------------------- | ------------------------------------- |
| `Object.keys(obj)`              | Returns array of keys                    | `['name','role']`                     |
| `Object.values(obj)`            | Returns array of values                  | `['Alice','QA']`                      |
| `Object.entries(obj)`           | Returns array of `[key,value]` pairs     | `[ ['name','Alice'], ['role','QA'] ]` |
| `Object.assign(target, source)` | Copies properties from source to target  | `{ a:1, b:2 }`                        |
| `Object.freeze(obj)`            | Makes object immutable                   | Properties cannot change              |
| `Object.seal(obj)`              | Prevents adding/removing properties      | Existing values can change            |
| `Object.hasOwn(obj,key)`        | Checks if property exists                | `true/false`                          |
| `delete obj.key`                | Deletes a property                       | `{ name: 'Alice' }`                   |
| `Object.create(proto)`          | Creates object with prototype            | Access prototype methods              |
| `Object.fromEntries(arr)`       | Converts `[key,value]` array into object | `{ name:'Alice', role:'QA' }`         |

---

If you want, I can now **create a single all-in-one cheat sheet** combining **Array + Map + Set + Object** with **all methods, examples, outputs, and use cases** — ready to use for **test automation reference**.

Do you want me to make that?

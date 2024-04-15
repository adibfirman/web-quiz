# Call staks and event loop

1. new Promise -> which is constructor is syncronously by default
2. microTask is the more prio than macro task
3. so, for example this code setTimeout(() => console.log(1))

---

Main Thread Web APIs
Promise.resolve().then(() => console.log(2)) then(() => console.log(2))
setTimeout(() => console.log(1)) setTimeout(() => console.log(1))

Macrotask queue
setTimeout(() => console.log(1))
then(() => console.log(2))

Microtask queue
console.log(2) // this will be print
console.log(1) // second will be print

---

basically, the main thread will push the arguments of the web APIs then put that on the macrotask queue then
because the code is wrap by `setTimeout` this will put onto Microtask

the order will more like Main Thread -> Web APIs -> Macro -> Micro

4. Macrotask is basically the bunch of the function that the propose is like Promise and setTimeout
5. Microtask is the next tick that will be run, or the latest port of the execution event loop

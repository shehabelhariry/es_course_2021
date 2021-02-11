## Proxy 

- A proxy object enables us to use a layer (proxy) over an object
- A proxy is created with 2 parameters 
  - `target` is the original object I want to proxy 
  - `handler` an object that defines the rules for which we can use the object
  - The `handler` object contain methods called `traps`

  ```js
  const target = {
    msg1: "hello",
    msg2: "everyone",
  };

  const handler = {
    get: function (target, prop) {
      if (prop === "msg1") {
        return `${target[prop]} For sure 😂`;
      }
    },
    set: function (target, prop, value) {
      if (!Object.keys(target).includes(prop)) {
        throw new Error(`${prop} does not exist on current obj`);
      }
      if (prop === "msg1") {
        if (typeof value !== "string") {
          throw new Error("Only strings are allowed");
        }
      }
    },
  };

  const proxy1 = new Proxy(target, handler);
  ```
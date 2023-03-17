
## 💠 How `event` are constantly being listened where JS is an single thread environment? <br><br>

## 💠 How `setTimeout(() => {}, 5000)` ⏳time was reduced? <br><br>

## 💠 What we need is smooth UI rendering - (non-blocking way).<br><br>

<br>

***

<br>
<br>

## [latentflip.com/loupe/🧯](https://latentflip.com/loupe/?code=JC5vbignYnV0dG9uJywgJ2NsaWNrJywgZnVuY3Rpb24gb25DbGljaygpIHsKICAgIHNldFRpbWVvdXQoZnVuY3Rpb24gdGltZXIoKSB7CiAgICAgICAgY29uc29sZS5sb2coJ1lvdSBjbGlja2VkIHRoZSBidXR0b24hJyk7ICAgIAogICAgfSwgMjAwMCk7Cn0pOwoKY29uc29sZS5sb2coIkhpISIpOwoKc2V0VGltZW91dChmdW5jdGlvbiB0aW1lb3V0KCkgewogICAgY29uc29sZS5sb2coIkNsaWNrIHRoZSBidXR0b24hIik7Cn0sIDUwMDApOwoKY29uc29sZS5sb2coIldlbGNvbWUgdG8gbG91cGUuIik7!!!PGJ1dHRvbj5DbGljayBtZSE8L2J1dHRvbj4%3D)

![alt text][notsecure]


***

## YouTube 🎞️

<a href="https://youtu.be/8aGhZQkoFbQ">
  <img src="https://img.youtube.com/vi/8aGhZQkoFbQ/sddefault.jpg" alt="Cat GIF" width="150" height="100" />
</a>
<section>

***
***

<br><br>


<details open>
<summary></summary>
<h2>Javascript Runtime Environment</h2>

![alt text][JS_Engine]
</details>
</section>


<section>
<details>
<summary>View more</summary>


<details open>
<summary>Try this</summary>
<img width="700px" height="500px" src="https://github.com/thalif/Javascript-Async/blob/main/JS_environment2.png?raw=true"></img>
</details>

<details>
<summary>Try this</summary>
<img width="750px" height="600px" src="https://github.com/thalif/Javascript-Async/blob/main/JS_environment3.png?raw=true"></img>
</details>

<details>
<summary>Try this</summary>
<img width="700px" height="600px" src="https://github.com/thalif/Javascript-Async/blob/main/JS_environment4.png?raw=true"></img>
</details>

<br>

***


<br>

<table style="width:100%;">
    <tr>
    <td>
    <section>
    <h2>Macro Task</h2>
        <li>setTimeout()</li>
        <li>setImmediate()</li>
        <li>setInterval()</li>
        <li>RqueueMicrotask()</li>
        <li>UI rendering</li>
        <li>I/O</li>
    </section>
    </td>
    <td>
    <section>
        <h2>Micro Task</h2>
        <li>Promise</li>
        <li>process.nextTick()</li>
        <li>queueMicrotask()</li>
    </section>
    </td>
    <tr>
</table>

<br>

> ### Priority

<details>
<summary></summary>
<img width="700px" height="600px" src="https://github.com/thalif/Javascript-Async/blob/main/microtaskandmacrotask.gif?raw=true"></img>
</details>


<br>

### &nbsp;&nbsp;&nbsp;&nbsp; 1. Call stack
### &nbsp;&nbsp;&nbsp;&nbsp; 2. Microtasks queue
### &nbsp;&nbsp;&nbsp;&nbsp; 3. Macrotasks queue

<br>

### The `callstack` is the first priority because it is where the current function is executed. When a function is called, it is added to the call stack, and when it is completed, it is removed from the stack.

<br>

### The `microtasks` queue is the second priority,  asynchronous tasks that are executed after the current function is completed and before any macrotasks in the queue are executed.
<br>

### The `macrotasks` queue is the last priority, and it consists of larger, asynchronous tasks that are executed after the microtasks queue is empty.

<br><br>

### **More here 🔗**

1. [In Depth](https://developer.mozilla.org/en-US/docs/Web/API/HTML_DOM_API/Microtask_guide/In_depth)
2. [Web_Workers_API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API)


<br>

</details>
</section>
<br>

***

## **Engine**

<!-- Javascript Engine -->
<details>
<summary></summary>

<img src="https://github.com/thalif/Javascript-Async/blob/main/JavascriptEngine.jpeg?raw=true" ></img>

<br>

* ### Each engine may have its own unique features and optimizations.

* ### However, the specific algorithms and strategies used for implementations can differ between engines, 
    * #### which can affect `performance` and `memory usage`.

* ### Also differ in their compatibility with different versions of the ECMAScript specification.

<br><br>

***
</details>

<br>
<br>
<br>

>>> #### **Callback** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;||&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Promise**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;||&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Async /Await**

<br><br>

<details>
<summary></summary>

<img width="300px" height="200px" src="https://github.com/thalif/Javascript-Async/blob/main/Vadivelu_Pokkiri.gif?raw=true" ></img>
</details>

> ## **Callback**
<br>

+ By removing the name callback, Callback is a programming way/trick as like

<table style="width:100%">
<tr>
<td>
<details open>
<summary>callback.js</summary>

```Javascript
    // Callback
    function myFunction(x, y, callback) {
        var result = x + y;
        callback(result);
    }

    function myCallback(result) {
        console.log("The result is: " + result);
    }

    myFunction(1, 2, myCallback);   // Callback
```
</details>
</td>
<td>
<details>
<summary></summary>

```Javascript
    // Recursion
    function happy(time) {
        happy(time)
    }
```

<details>
<summary></summary>
<img src="https://github.com/thalif/Javascript-Async/blob/main/vadiveluGlassOPen.gif?raw=true" alt="Cat GIF" width="150" height="100" />
</details>
</details>
</td>
</tr>
</table>



+ Just passing a reference as like variable to another function.

+  In JavaScript, a `var` can have copy of a function. 😂


    <!-- Section - 1 -->
    <section>
    <details>
    <summary>JS variable</summary>

    ![alt text][jsConsole]
    </details>
    </section>

    <!-- Section - 2 -->
    <section>
    <details>
    <summary>In C#, function should be declared with `delegate` keyword</summary>

    ```c#
    public delegate void MyCallback(int result);
    ```
    </details>
    </section>
<br>

## Where do we utilizing callbacks as superPower?
<br>

* When working with Browser API, callback functions can be used efficiently.

* Its very hard to trace callback origin for human being.

<br>


<table width=100% style="display:flex">
<tr>
<td style="display:flex">

<details open>
<summary></summary>
<img src="https://github.com/thalif/Javascript-Async/blob/main/stackTrace.png?raw=true" width="300px" height="400px"></img>
</details>

<details>
<summary></summary>
<img src="https://github.com/thalif/Javascript-Async/blob/main/ppu.png?raw=true" width="600px" height="400px"></img>
</details>

</td>
</tr>
</table>





<br><br>

<!-- Sheild Meme -->
<details>
<summary></summary>

<img src="https://github.com/thalif/Javascript-Async/blob/main/Sheild_Promise2.png?raw=true" width="350px" height="400px"></img>
</details>



<!-- Promise section -->
> # **Promise**
> ### ES2015 || ES6

<br>
<br>

 ## &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; We need to construct a `promisible` code

<br>
<br>


<table style="width:100%;">
<tr>
<td style="display:flex">
<details open>
<summary>promise.js</summary>

```c++
const myPromise = new Promise((resolve, reject) => {
  
    resolve();
    
    reject();
  
});

```
</td>

<td>
</details>

<details open>
<summary></summary>

```js
// Normal Function
function getUserMedia(){
    
    return stream;
}
```
</details>
</td>

<td>
</details>

<details>
<summary></summary>

```js
// Switch Statement
switch (day){
    case 1:
        break;
    default:
        break;
}
```
</details>
</td>
</tr>
</table>



### **Do your own promise	✋**

<br>

<table width=100%>
<tr>

<details open>
<summary>callGetUserMedia.js</summary>

```js
// Create your new Promise

const callGetUserMedia = new Promise((success, failure) => {
    try{
        
        // just do your code here
        let i = 0;
        let j = 1;

        navigator.mediaDevices.getUserMedia( {audio:true, video:true} )
        .then((stream) => {
            if(stream){
                success(stream);
            }
        });
        
    }
    catch(error){
        failure(error);
    }
});


// call it
function main(){
    callGetUserMedia.then((stream) => {setJoinPageStream(stream)})
}
```
</details>

<details>
<summary></summary>

```c++
// All the same
new Promise((resolve, reject) => { });
new Promise((success, failure) => { });
new Promise((one, two) => { });
```
</details>

</td>


</td>
</tr>

<br><br>


<tr>
<td>

<br>


### **Pass arguments to a promise 🛒**

<br>
<details open>
<summary>callGetUserMedia.js</summary>

```js
// Pass arugments to a promise

function callGetUserMedia(constraints){

    return new Promise((resolve, reject) => 
    {
        try{
            
            // just do your code here
            let i = 0;
            let j = 1;

            navigator.mediaDevices.getUserMedia(constraints)
            .then((stream) => {
                if(stream){
                    resolve(stream);
                }
            });


        }
        catch(error){
            reject(error);
        }
    });
}
```
</details>
</td>
</tr>

</table>

***

<br>

### **Promise can have a Chain ⛓️**

<br>

* By chaining promises together using the `then()` method, you can create a sequence of asynchronous operations to be executed in order.


```js
            Promise

    then()          catch()

    then()

    then()

    then()

    ...
```

* ### This chain can be skipped when any one of them got `rejected`.

* ### And `catch` will be always there for us.


<br>

### **Use it!🔌**

<br>

#### callGetUserMedia.js
```c++
main(){

    // Use your promise
    callGetUserMedia.then(setJoinPageStream)
    .then(enumerateDevices)
    .then(setDevicesInLocalStorage)
    .then(startDetectingAudio)
    .catch((error) => {
        device_error_handling_revamp(error);
    })
}
```
***
***

<br>
<br>

<details>
<summary></summary>

<img src="https://github.com/thalif/Javascript-Async/blob/main/uneasy.gif?raw=true" width=300px></img>
</details>

> # **Async / Await**
> ### ES2017 || ES8

<br>

* ### To make it easier to write asynchronous code without resorting to callbacks or promises.
* ### `async/await` is a higher-level abstraction built on top of `promises`.

    <details>
    <summary></summary>

    <img src="https://github.com/thalif/Javascript-Async/blob/main/jaquenHagar.gif?raw=true" width="300px" height="150px"></img>
    </details>

* ### Declare a function with keyword `async`. Now the function will get executed from microtask.

```js
// A async function
async function callGetUserMedia(){
    
    let result = await somethingToGet();
    return result;
}
```
* ### handle errors more easily, using `try/catch` blocks.

<br>
<details>
<summary>Async proto</summary>

```js
    async function 

        // Can have N await statements
        await
        await
        await
        await 
```

***

</details>


<br><br>

### **Use it!🔌**

<br>

#### callGetUserMedia.js

```js
// Create asynchronous function

async function callGetUserMedia() {

    try{
        let stream = await navigator.mediaDevices.getUserMedia(constraints);

        await enumerateDevices(stream);
        setDevicesInLocalStorage(stream);
        await startDetectingAudio(stream);
    }
    catch(error){
        throw new Error(error);
    }
}


function main(){

    // Call it as a normal function
    callGetUserMedia();
    loadJoinPage();
    
}
```



<details>
<summary></summary>

<img src="https://github.com/thalif/Javascript-Async/blob/main/mayandiBrowsers.jpg?raw=true" width="500px" height="300px"></img>
</details>

<details>
<summary></summary>

<img src="https://github.com/thalif/Javascript-Async/blob/main/js_engine.png?raw=true" width="500px" height="300px"></img>
</details>

<details>
<summary></summary>

<img src="https://github.com/thalif/Javascript-Async/blob/main/V8vsSpidermonkey.png?raw=true" width="500px" height="300px"></img>
</details>


<details>
<summary></summary>

<img src="https://github.com/thalif/Javascript-Async/blob/main/joffery_ramsay.jpeg?raw=true" width="250px" height="300px"></img>
</details>

<details>
<summary></summary>

<img src="https://github.com/thalif/Javascript-Async/blob/main/PromiseVScallback.png?raw=true" width="250px" height="300px"></img>
</details>

<details>
<summary></summary>

<img src="https://github.com/thalif/Javascript-Async/blob/main/thread.png?raw=true" width="500px" height="300px"></img>
</details>
















[Sheild_Promise]: Sheild_Promise2.png  "Sheild_Promise"

[callGetUserMedia]: callGetUserMedia_Promise.png  "image3"








[who-is-that-yar-adhu]: who-is-that-yar-adhu.gif "gif1"


[JS_Engine]: https://vahid.blog/post/2021-03-21-understanding-the-javascript-runtime-environment-and-dom-nodes/featured.png "Js Engine"


[JS_Engine2]: https://camo.githubusercontent.com/2f12852c45cf6c9f9f7c3f03c07c063a83b7ede0/68747470733a2f2f626c6f672d6173736574732e726973696e67737461636b2e636f6d2f323031362f31302f7468652d4e6f64652d6a732d6576656e742d6c6f6f702e706e67 "JS Engine 2"

[notsecure]: https://github.com/thalif/Javascript-Async/blob/main/notsecure.png?raw=true "notsecure"

[jsConsole]: https://github.com/thalif/Javascript-Async/blob/main/Js_Variable.png?raw=true.png "console code"


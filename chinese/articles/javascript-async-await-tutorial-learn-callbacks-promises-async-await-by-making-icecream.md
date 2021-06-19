> -  原文地址：[JavaScript Async/Await Tutorial – Learn Callbacks, Promises, and Async/Await in JS by Making Ice Cream 🍧🍨🍦](https://www.freecodecamp.org/news/javascript-async-await-tutorial-learn-callbacks-promises-async-await-by-making-icecream/)
> -  原文作者：[Joy Shaheb](https://www.freecodecamp.org/news/author/joy/)
> -  译者：Miever1
> -  校对者：

![JavaScript Async/Await Tutorial – Learn Callbacks, Promises, and Async/Await in JS by Making Ice Cream 🍧🍨🍦](https://www.freecodecamp.org/news/content/images/size/w2000/2021/05/FCC-Thumbnail--3-.png)

Today we're going to build and run an **ice cream shop** and learn **asynchronous JavaScript** at the same time. Along the way, you'll learn how to use:
今天我们将在学习 **异步 JavaScript** 的同时建立并运行一个 **冰淇淋店** ，在此过程中，您将学习如何使用:

-   Callbacks
-   Promises
-   Async / Await

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/b1j935dg72g9u8zvh2oi.png)

# Here's what we'll cover in this article:
# 以下是我们将在本文中介绍的内容:

-   What is Asynchronous JavaScript?
-   什么是异步JavaScript？
-   Synchronous vs Asynchronous JavaScript
-   同步与异步JavaScript
-   How Callbacks Work in JavaScript
-   Callbacks如何在JavaScript中运作
-   How Promises Work in JavaScript
-   Promises如何在JavaScript中运作
-   How Async / Await Works in JavaScript
-   Async / Await 如何在JavaScript中运作

So let's dive in!
让我们开始吧!

## You can watch this tutorial on YouTube as well if you like:
## 如果你喜欢，也可以在YouTube上观看本教程

# What is Asynchronous JavaScript?
# 什么是异步JavaScript？

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7yd96tgxvuowqmfgcx6b.png)

If you want to build projects efficiently, then this concept is for you.
如果您想高效地构建项目，那么这个概念很适合您。

The theory of async JavaScript helps you break down big complex projects into smaller tasks.
异步JavaScript理论可以帮助您将大型复杂的项目分解为较小的任务。

Then you can use any of these three techniques – **callbacks, promises or Async/await** – to run those small tasks in a way that you get the best results.
然后你可以使用这三种技巧 – **callbacks, promises or Async/await** – 中的任何一种来运行这些小任务。

Let's dive in!🎖️
让我们开始吧!🎖️

# Synchronous vs Asynchronous JavaScript
# 同步与异步JavaScript

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/arzbf1rc3pi4yi6u8wup.png)

## What is a Synchronous System?
## 什么是同步系统

In a synchronous system, tasks are completed one after another.
在同步系统中，任务一个接一个地完成。

Think of this as if you have just one hand to accomplish 10 tasks. So, you have to complete one task at a time.
想象一下，如果你有10项任务, 每次只能完成一个任务，那么在同一个时间你只能做一个任务。

Take a look at the GIF 👇 – one thing is happening at a time here:
看看这个动图👇 – 这里会发生一件事:

![Synchronous System](https://media.giphy.com/media/ICIS16DkE9qB9HVxtq/giphy.gif)

You'll see that until the first image is loaded completely, the second image doesn't start loading.
您将看到，直到第一个图像完全加载，第二个图像才开始加载。

Well, JavaScript is by default Synchronous **\[single threaded\]**. Think about it like this – one thread means one hand with which to do stuff.
JavaScript默认是同步的  **\[单线程\]**。你可以这样想 ——— 单线意味着一次只能做一件事。

## What is an Asynchronous System?
## 什么是异步系统?

In this system, tasks are completed independently.
在这个系统中，任务是独立完成的。

Here, imagine that for 10 tasks, you have 10 hands. So, each hand can do each task independently and at the same time.
假设你有十个任务以及十只手。那么在同一时间，每只手都可以同时独立完成每一项任务。

Take a look at the GIF 👇 – you can see that each image loads at the same time.
看看这张动图 👇 - 你可以看到每个图像都是同时加载的。

![Asynchronous System](https://media.giphy.com/media/MMDnmJnE7uhX6KtcKc/giphy.gif)

Again, all the images are loading at their own pace. None of them is waiting for any of the others.
同样，所有的图像都以自己的速度加载。它们都没在等待其他任务。

## To Summarize Synchronous vs Asynchronous JS:
## 总结一下同步JS和异步JS:

When three images are on a marathon, in a:
当三张图片在马拉松上，在一个:

-   **Synchronous** system, three images are in the same lane. One can't overtake the other. The race is finished one by one. If image number 2 stops, the following image stops.
-   **同步** 系统，三个图像在同一条跑道上。一个不能超过另外一个。赛跑一个接一个地结束。如果2号图像停止，剩下的图像也会停止。

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/w1r9y4ghhq0t8wjb1u9h.png)

-   **Asynchronous system,** the three images are in different lanes. They'll finish the race on their own pace. Nobody stops for anybody:
-   ** 异步系统 ** 这三张图片在不同的跑道上。 它们会在自己的跑道上完成比赛。不会受其他图片影像：
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ehknx5shc4orh32s0ktk.png)

## Synchronous and Asynchronous Code Examples
##  同步和异步代码示例

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/pzbnpcza9rbj8xgiby95.png)

Before starting our project, let's look at some examples and clear up any doubts.
在开始我们的项目之前，让我们看一些例子来消除一些疑问。

### Synchronous Code Example
### 同步的代码示例

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5m6p1qy522lj3auvl5ty.png)

To test a synchronous system, write this code in JavaScript:
为了测试同步系统，用JavaScript写以下代码：

```javascript
console.log(" 我 ");

console.log(" 吃 ");

console.log(" 冰激凌 ");
```

Here's the result in the console: 👇
控制台的结果如下：👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/54izy7zyo52j2z6netls.png)

### Asynchronous code example
###  异步代码示例

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/y5d0o8unbe8c67qeqz0w.png)

Let's say it takes two seconds to eat some ice cream. Now, let's test out an asynchronous system. Write the below code in JavaScript.
 我们假设吃冰淇淋需要两秒钟。现在，让我们测试一个异步系统。用JavaScript编写下面的代码。

**Note:** Don't worry, we'll discuss the `setTimeout()` function later in this article.
**注意:** 不用担心,我们将在本文后面讨论' setTimeout() '函数。

```javascript
console.log("我");

// This will be shown after 2 seconds
// 这将在2秒后显示

setTimeout(()=>{
  console.log("吃");
},2000)

console.log("冰激凌")
```

And here's the result in the console: 👇
控制台的结果如下：👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/o44c2t0r7bknkadoumgx.png)

Now that you know the difference between synchronous and async operations, let's build our ice cream shop.
既然我们已经了解了同步操作和异步操作之间的区别，那么让我们来创建我们的冰淇淋商店。

## How to Setup our Project
## 如何设置我们的项目

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2mzbtcnm67v2iys7cix7.png)

For this project you can just open [Codepen.io](https://codepen.io/) and start coding. Or, you can do it in VS code or the editor of your choice.
对于这个项目，你只需要打开[Codepen.io](https://codepen.io/)直接开始编码。或者，你可以用VS code编辑器来做。

Open the JavaScript section, and then open your developer console. We'll write our code and see the results in the console.
打开JavaScript部分，然后打开开发人员控制台。我们将编写代码并在控制台中查看结果。

# What are Callbacks in JavaScript?
# 什么是JavaScript中的回调函数？

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/s5iloofqsv3lcdl4flsi.png)

When you nest a function inside another function as an argument, that's called a callback.
当你将一个函数作为参数嵌套到另一个函数中时，这叫做回调。

Here's an illustration of a callback:
下面是一个回调的例子:

![](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/uz3pl56lmoc2pq7wzi2s.png)

**An example of a callback**
**一个回调的例子**

Don't worry, we'll see some examples of callbacks in a minute.
别担心，我们马上就会看到一些回调的例子。

### Why do we use callbacks?
### 为什么要使用回调?

When doing a complex task, we break that task down into smaller steps. To help us establish a relationship between these steps according to time (optional) and order, we use callbacks.
当我们做一个复杂的任务时，我们把它分解成更小的步骤。 为了帮助我们根据时间(可选)和顺序在这些步骤之间建立关系时我们会使用回调。

Take a look at this example:👇
看看这个例子:👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/o05q7ortgctx2oeyntfn.png)

**Chart contains steps to make ice cream**
**图表包含制作冰淇淋的步骤**

These are the small steps you need to take to make ice cream. Also note that in this example, the order of the steps and timing are crucial. You can't just chop the fruit and serve ice cream.
 这些是制作冰淇淋需要的小步骤。 还要注意，在本例中，步骤的顺序和计时是至关重要的。你不能只把水果切了就端上冰淇淋。

At the same time, if a previous step is not completed, we can't move on to the next step.
同时，如果前一个步骤没有完成，我们就不能进入下一个步骤。

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2v1rn50smjul9arkneza.png)

To explain that in more detail, let's start our ice cream shop business.
为了更详细地解释这一点，让我们开始冰淇淋店的生意。

## But Wait...
## 等等。。。

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cq8exwor5aiciu2j6jwu.png)

The shop will have two parts:
该店将分为两部分:

-   The storeroom will have all the ingredients \[Our Backend\]
-   储藏室里有所有的原料[我们的后台]
-   We'll produce ice cream in our kitchen \[The frontend\]
-    我们将在厨房里制作冰淇淋 \[前端\]

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/i69bws707m5rvsj34i9o.png)

## Let's store our data
## 让我们存储我们的数据

Now, we're gonna store our ingredients inside an object. Let's start!
现在，我们要把原料存储在一个对象中。让我们开始!

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ihezrht8dgg9xn8lm2k9.png)

You can store the ingredients inside objects like this: 👇
你可以像这样在对象中存储成分:👇

```javascript
let stocks = {
    Fruits : ["草莓", "葡萄", "香蕉", "苹果"]
 }
```

Our other ingredients are here: 👇
我们的其他食材在这里:👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6dcwr770l0ubupv0r2gj.png)

You can store these other ingredients in JavaScript objects like this: 👇
您可以像这样将这些其他成分存储在JavaScript对象中:👇
 
```javascript
let stocks = {
    Fruits : ["草莓", "葡萄", "香蕉", "苹果"],
    liquid : ["水", "冰"],
    holder : ["盘子", "被子", "棍子"],
    toppings : ["巧克力", "花生"],
 };
```

整个业务取决于客户的 **订单**。一接到订单，我们就开始生产，然后供应冰淇淋。 因此我们将创建两个函数 ->

-   `order`
-   `production`

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3bnzniiyamo0b9l7e806.png)

This is how it all works: 👇
 这就是它的工作原理:👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/r8h8ra9wor8cs3dgddpb.png)

Get order from customer, fetch ingredients, start production, then serve.
从客户处获取订单，取食材，开始生产，然后上桌。

Let's make our functions. We'll use arrow functions here:
我们来写一下函数。我们将在这里使用箭头函数:

```javascript
let order = () =>{};

let production = () =>{};
```

Now, let's establish a relationship between these two functions using a callback, like this: 👇
现在，让我们使用回调建立这两个函数之间的关系，如下所示:👇

```javascript
let order = (call_production) =>{

  call_production();
};

let production = () =>{};
```

### Let's do a small test
### 让我们做个小测试

We'll use the `console.log()` function to conduct tests to clear up any doubts we might have regarding how we established the relationship between the two functions.
 我们将使用' console.log() '函数进行测试，以消除关于如何建立这两个函数之间的关系的任何疑问。

```javascript
let order = (call_production) =>{

console.log("下了订单。请打电话给生产")

// function 👇 is being called 
//函数👇被调用
  call_production();
};

let production = () =>{

console.log("生产已经开始")

};
```

To run the test, we'll call the **`order`** function. And we'll add the second function named `production` as its argument.
要运行测试，我们将调用 **`order`** 函数。我们将添加第二个函数名为“production”作为它的参数。

```javascript
// name 👇 of our second function
// 将第二个函数命名为 👇
order(production);
```

Here's the result in our console 👇
下面是我们控制中的结果 👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/u41ugdxxed1q8coz5hol.png)

## Take a break
## 休息一下

So far so good – take a break!
到目前为止一切都很好，休息一下吧!

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/tnr74waq6noc0djln3qx.png)

## Clear out the console.log
## 清除console.log日志

Keep this code and remove everything \[don't delete our stocks variable\]. On our first function, pass another argument so that we can receive the order \[Fruit name\]:
保留这段代码并删除所有的东西\[不要删除我们的 stocks 变量\]。在我们的第一个函数中，传递另一个参数，以便我们可以接收订单\[水果名\]:

```javascript
// 函数 1

let order = (fruit_name, call_production) =>{

  call_production();
};

// 函数 2

let production = () =>{};


// 触发 👇

order("", production);
```

Here are our steps, and the time each step will take to execute.
下面是我们的步骤，以及执行每个步骤所需的时间。

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rphpp2lqjnk7f0tv5g3d.png)

**Chart contains steps to make ice cream**
**图表包含制作冰淇淋的步骤**

In this chart, you can see that step 1 is to place the order, which takes 2 seconds. Then step 2 is cut the fruit (2 seconds), step 3 is add water and ice (1 second), step 4 is to start the machine (1 second), step 5 is to select the container (2 seconds), step 6 is to select the toppings (3 seconds) and step 7, the final step, is to serve the ice cream which takes 2 seconds.
在这个图表中，您可以看到第一步是下订单，这需要2秒。第二步是切水果(2秒)，第三步是加水和冰(1秒)，步骤4启动机器(1秒)，第5步是选择容器(2秒)，第六步是选择配料(3秒)，以及第七步，也就是最后一步，端上冰淇淋，这需要2秒。

To establish the timing, the function `setTimeout()` is excellent as it is also uses a callback by taking a function as an argument.
要建立计时，函数 `setTimeout()` 非常好，因为它也使用一个回调函数作为参数。

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/qwrg1taugyhvjnkx8xpp.png)

**Syntax of a setTimeout() function**
**setTimeout() 函数的语法**

Now, let's select our fruit and use this function:
 现在，让我们使用这个函数来选择的水果:
```javascript
// 1st Function
// 功能1

let order = (fruit_name, call_production) =>{

  setTimeout(function(){

    console.log(`${stocks.Fruits[fruit_name]} 被选中`)

// Order placed. Call production to start
// 下完订单。调用 production 开始生产
   call_production();
  },2000)
};

// 2nd Function
// 功能2

let production = () =>{
  // blank for now
  // 暂时空白
};

// 触发 👇
order(0, production);
```

And here's the result in the console: 👇
下面是控制台中的结果:👇

**Note** that the result is displayed after 2 seconds.
**注意**  2秒后显示结果。

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/edwji5vauypoezj3bxdk.png)

If you're wondering how we picked strawberry from our stock variable, here's the code with the format 👇
如果您想知道我们是如何从stock变量中采摘草莓的，下面是格式化的代码 👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ia38z3x6b96xpq3aid91.png)

Don't delete anything. Now we'll start writing our production function with the following code.👇 We'll use arrow functions:
不删除任何代码。现在，我们将使用以下代码开始编写生产函数。我们将使用箭头函数: 👇

```javascript
let production = () =>{

  setTimeout(()=>{
    console.log("生产已经开始")
  },0000)

};
```

And here's the result 👇
结果如下 👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5yskzvg7rezo2sg4lklq.png)

We'll nest another `setTimeout` function in our existing `setTimeout` function to chop the fruit. Like this: 👇
我们将在现有的 `setTimeout` 函数中嵌套另一个 `setTimeout` 函数来切水果。如:👇

```javascript
let production = () =>{
  
  setTimeout(()=>{
    console.log("生产已经开始")


    setTimeout(()=>{
      console.log("水果已经切好了")
    },2000)


  },0000)
};
```

And here's the result 👇
结果如下 👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/4659l1mua0rv40rwyem7.png)

If you remember, here are our steps:
如果你还记得，这是我们的步骤:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rphpp2lqjnk7f0tv5g3d.png)

**Chart contains steps to make ice cream**
**图表包含制作冰淇淋的步骤**

Let's complete our ice cream production by nesting a function inside another function – this is also known as a callback, remember?
让我们通过在另一个函数中嵌套一个函数来完成我们的冰淇淋生产 - 这也称为回调，还记得吗？

```javascript
let production = () =>{

  setTimeout(()=>{
    console.log("生产已经开始")
    setTimeout(()=>{
      console.log("水果已经切好了")
      setTimeout(()=>{
        console.log(`${stocks.liquid[0]} 和 ${stocks.liquid[1]} 被添加`)
        setTimeout(()=>{
          console.log("开启机器")
          setTimeout(()=>{
            console.log(`冰淇淋放在上面 ${stocks.holder[1]}`)
            setTimeout(()=>{
              console.log(`${stocks.toppings[0]} 作为调料`)
              setTimeout(()=>{
                console.log("冰激凌上桌！")
              },2000)
            },3000)
          },2000)
        },1000)
      },1000)
    },2000)
  },0000)

};
```

And here's the result in the console 👇
控制台结果如下👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5mq9bg6fqrc8apj7nu7b.png)

Feeling confused?
是否感到疑惑？

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/man5l5pwavp9prio1wc0.png)

This is called callback hell. It looks something like this (remember that code just above?): 👇
 这叫做回调地狱。它看起来像这样(还记得上面的代码吗?):👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/d5rk7f8d920jzn22smjh.png)

**Illustration of Callback hell**
**回调地狱图解**

What's the solution to this?
解决方案是什么?

# How to Use Promises to Escape Callback Hell
# 如何使用承诺来避免回调地狱

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/x3neys1hxsrifgg5qm6x.png)

Promises were invented to solve the problem of callback hell and to better handle our tasks.
Promises的发明是为了解决回调地狱的问题和更好地处理我们的任务。

## Take a break
## 休息一下

But first, take a break!
首先，休息一下!

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/bwfvel7kvm422gqvj0os.png)

This is how a promise looks:
这就是 promise 的样子

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7qo1zheuin2825osozvc.png)

**illustration of a promise format**
**promised的格式说明**

Let's dissect promises together.
 让我们一起来剖析promises。

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/gozy5r1nfubzeq5t5t25.png)

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ezi9ogz0ergprgkmu68a.png)

**An illustration of the life of a promise**
**promise 周期的图解**

As the above charts show, a promise has three states:
如上图所示，一个promise有三种状态

-   **Pending:** This is the initial stage. Nothing happens here. Think of it like this, your customer is taking their time giving you an order. But they haven't ordered anything yet.
-   **Pending:** 这是初始阶段。这里什么也没有发生。 你可以这样想，你的客户正在慢慢地给你下订单。但是他们还没有点任何东西。
-   **Resolved:** This means that your customer has received their food and is happy.
-   **Resolved:** 这意味着你的顾客已经收到了他们的食物并且很高兴。
-   **Rejected:** This means that your customer didn't receive their order and left the restaurant.
-   **Rejected:** 这意味着你的顾客没有收到他们点的菜并离开了餐厅。

Let's adopt promises to our ice cream production case study.
让我们将 promise 应用到我们的冰淇淋生产案例研究中。

## But wait...
## 等等

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/634b6oyglkyoccsvr8l7.png)

We need to understand four more things first ->
首先，我们需要了解另外四件事 ->

-   Relationship between time and work
-   时间和工作的关系
-   Promise chaining
-   Promise 链
-   Error handling
-   错误处理
-   The `.finally` handler
-   最后的处理程序

Let's start our ice cream shop and understand each of these concepts one by one by taking baby steps.
让我们开始我们的冰淇淋店，一步一步地理解这些概念。

## Relationship between time and work
## 时间和工作的关系

If you remember, these are our steps and the time each takes to make ice cream"
如果你还记得，这就是我们制作冰淇淋的步骤和时间
 
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rphpp2lqjnk7f0tv5g3d.png)

**Chart contains steps to make ice cream**
** 图表包含制作冰淇淋的步骤**

For this to happen, let's create a variable in JavaScript: 👇
为了实现这一点，让我们在JavaScript中创建一个变量:👇

```javascript
let is_shop_open = true;
```

Now create a function named `order` and pass two arguments named `time, work`:

```javascript
let order = ( time, work ) =>{

  }
```

Now, we're gonna make a promise to our customer, "We will serve you ice-cream" Like this ->

```javascript
let order = ( time, work ) =>{

  return new Promise( ( resolve, reject )=>{ } )

  }
```

Our promise has 2 parts:

-   Resolved \[ ice cream delivered \]
-   Rejected \[ customer didn't get ice cream \]

```javascript
let order = ( time, work ) => {

  return new Promise( ( resolve, reject )=>{

    if( is_shop_open ){

      resolve( )

    }

    else{

      reject( console.log("Our shop is closed") )

    }

  })
}
```

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3wik2xel68yue93yapm6.png)

Let's add the time and work factors inside our promise using a `setTimeout()` function inside our `if` statement. Follow me 👇

**Note:** In real life, you can avoid the time factor as well. This is completely dependent on the nature of your work.

```javascript
let order = ( time, work ) => {

  return new Promise( ( resolve, reject )=>{

    if( is_shop_open ){

      setTimeout(()=>{

       // work is 👇 getting done here
        resolve( work() )

// Setting 👇 time here for 1 work
       }, time)

    }

    else{
      reject( console.log("Our shop is closed") )
    }

  })
}
```

Now, we're gonna use our newly created function to start ice-cream production.

```javascript
// Set 👇 time here
order( 2000, ()=>console.log(`${stocks.Fruits[0]} was selected`))
//    pass a ☝️ function here to start working
```

The result 👇 after 2 seconds looks like this:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/erzjup8wt505j502e73n.png)

Good job!

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/8taajvjy6pfq35hu90nq.png)

## Promise chaining

In this method, we defining what we need to do when the first task is complete using the `.then` handler.  It looks something like this 👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/l27ytifkoedl22kc97lh.png)

**Illustration of promise chaining using .then handler**

The .then handler returns a promise when our original promise is resolved.

#### Here's an Example:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/1qpeewo19qbhzj47goos.png)

Let me make it simpler: it's similar to giving instructions to someone. You tell someone to " First do this, then do that, then this other thing, then.., then.., then..." and so on.

-   The first task is our original promise.
-   The rest of the tasks return our promise once one small bit of work is completed

Let's implement this on our project. At the bottom of your code write the following lines. 👇

**Note:** don't forget to write the `return` word inside your `.then` handler. Otherwise, it won't work properly. If you're curious, try removing the return once we finish the steps:

```javascript
order(2000,()=>console.log(`${stocks.Fruits[0]} was selected`))

.then(()=>{
  return order(0000,()=>console.log('production has started'))
})
```

And here's the result: 👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/qhhjaakbi6zshxhi6afy.png)

Using the same system, let's finish our project:👇

```javascript
// step 1
order(2000,()=>console.log(`${stocks.Fruits[0]} was selected`))

// step 2
.then(()=>{
  return order(0000,()=>console.log('production has started'))
})

// step 3
.then(()=>{
  return order(2000, ()=>console.log("Fruit has been chopped"))
})

// step 4
.then(()=>{
  return order(1000, ()=>console.log(`${stocks.liquid[0]} and ${stocks.liquid[1]} added`))
})

// step 5
.then(()=>{
  return order(1000, ()=>console.log("start the machine"))
})

// step 6
.then(()=>{
  return order(2000, ()=>console.log(`ice cream placed on ${stocks.holder[1]}`))
})

// step 7
.then(()=>{
  return order(3000, ()=>console.log(`${stocks.toppings[0]} as toppings`))
})

// Step 8
.then(()=>{
  return order(2000, ()=>console.log("Serve Ice Cream"))
})
```

Here's the result: 👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/y0d0f4ys83ctnevkbgxs.png)

## Error handling

We need a way to handle errors when something goes wrong. But first, we need to understand the promise cycle:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/jlm7zwonbxszeaccyohv.png)

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/z2ajcu52rxzwq64g81vp.png)

**An illustration of the life of a promise**

To catch our errors, let's change our variable to false.

```javascript
let is_shop_open = false;
```

Which means our shop is closed. We're not selling ice cream to our customers anymore.

To handle this, we use the `.catch` handler. Just like `.then`, it also returns a promise, but only when our original promise is rejected.

A small reminder here:

-   `.then` works when a promise is resolved
-   `.catch` works when a promise is rejected

Go down to the very bottom and write the following code:👇

Just remember that there should be nothing between your previous `.then` handler and the `.catch` handler.

```javascript
.catch(()=>{
  console.log("Customer left")
})
```

Here's the result:👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/lot6engklu29y05q8xyr.png)

A couple things to note about this code:

-   The 1st message is coming from the `reject()` part of our promise
-   The 2nd message is coming from the `.catch` handler

## How to use the .finally() handler

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/gdq3i0agj4volq46ycue.png)

There's something called the `finally` handler which works regardless of whether our promise was resolved or rejected.

**For example:** whether we serve no customers or 100 customers, our shop will close at the end of the day

If you're curious to test this, come at very bottom and write this code: 👇

```javascript
.finally(()=>{
  console.log("end of day")
})
```

The result:👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/t2j3jf2uofip1d6y2rtt.png)

Everyone, please welcome Async / Await~

# How Does Async / Await Work in JavaScript?

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ra7483f90b69pjl2cbae.png)

This is supposed to be the better way to write promises and it helps us keep our code simple and clean.

All you have to do is write the word `async` before any regular function and it becomes a promise.

## But first, take a break

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/4vujyfxz7dg41jhjtcrx.png)

Let's have a look:👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/17f08ygj1odk28hgl9eq.png)

## Promises vs Async/Await in JavaScript

Before async/await, to make a promise we wrote this:

```javascript
function order(){
   return new Promise( (resolve, reject) =>{

    // Write code here
   } )
}
```

Now using async/await, we write one like this:

```javascript
//👇 the magical keyword
 async function order() {
    // Write code here
 }
```

## But wait......

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/t1pjzw6zl0h21tyyh9u3.png)

You need to understand ->

-   How to use the `try` and `catch` keywords
-   How to use the await keyword

## How to use the Try and Catch keywords

We use the `try` keyword to run our code while we use `catch` to catch our errors. It's the same concept we saw when we looked at promises.

Let's see a comparison. We'll see a small demo of the format, then we'll start coding.

### Promises in JS -> resolve or reject

We used resolve and reject in promises like this:

```javascript
function kitchen(){

  return new Promise ((resolve, reject)=>{
    if(true){
       resolve("promise is fulfilled")
    }

    else{
        reject("error caught here")
    }
  })
}

kitchen()  // run the code
.then()    // next step
.then()    // next step
.catch()   // error caught here
.finally() // end of the promise [optional]
```

### Async / Await in JS -> try, catch

When we're using async/await, we use this format:

```javascript
//👇 Magical keyword
async function kitchen(){

   try{
// Let's create a fake problem      
      await abc;
   }

   catch(error){
      console.log("abc does not exist", error)
   }

   finally{
      console.log("Runs code anyways")
   }
}

kitchen()  // run the code
```

Don't panic, we'll discuss the `await` keyword next.

Now hopefully you understand the difference between promises and Async / Await.

## How to Use JavaScript's Await Keyword

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/fry577xha7313ead96xy.png)

The keyword `await` makes JavaScript wait until a promise settles and returns its result.

### How to use the await keyword in JavaScript

Let's go back to our ice cream shop. We don't know which topping a customer might prefer, chocolate or peanuts. So we need to stop our machine and go and ask our customer what they'd like on their ice cream.

Notice here that only our kitchen is stopped, but our staff outside the kitchen will still do things like:

-   doing the dishes
-   cleaning the tables
-   taking orders, and so on.

## An Await Keyword Code Example

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/8r5w5aapofalnq882wat.png)

Let's create a small promise to ask which topping to use. The process takes three seconds.

```javascript
function toppings_choice (){
  return new Promise((resolve,reject)=>{
    setTimeout(()=>{

      resolve( console.log("which topping would you love?") )

    },3000)
  })
}
```

Now, let's create our kitchen function with the async keyword first.

```javascript
async function kitchen(){

  console.log("A")
  console.log("B")
  console.log("C")
  
  await toppings_choice()
  
  console.log("D")
  console.log("E")

}

// Trigger the function

kitchen();
```

Let's add other tasks below the `kitchen()` call.

```javascript
console.log("doing the dishes")
console.log("cleaning the tables")
console.log("taking orders")
```

And here's the result:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/y0dr669gewtrrd5fd86p.png)

We are literally going outside our kitchen to ask our customer, "what is your topping choice?" In the mean time, other things still get done.

Once, we get their topping choice, we enter the kitchen and finish the job.

### Small note

When using Async/ Await, you can also use the `.then`, `.catch`, and `.finally`  handlers as well which are a core part of promises.

### Let's open our Ice cream shop again

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vzw8gp721oecwo2b3l6s.png)

We're gonna create two functions ->

-   `kitchen`: to make ice cream
-   `time`: to assign the amount of time each small task will take.

Let's start! First, create the time function:

```javascript
let is_shop_open = true;

function time(ms) {

   return new Promise( (resolve, reject) => {

      if(is_shop_open){
         setTimeout(resolve,ms);
      }

      else{
         reject(console.log("Shop is closed"))
      }
    });
}

```

Now, let's create our kitchen:

```javascript
async function kitchen(){
   try{

     // instruction here
   }

   catch(error){
    // error management here
   }
}

// Trigger
kitchen();
```

Let's give small instructions and test if our kitchen function is working or not:

```javascript
async function kitchen(){
   try{

// time taken to perform this 1 task
     await time(2000)
     console.log(`${stocks.Fruits[0]} was selected`)
   }

   catch(error){
     console.log("Customer left", error)
   }

   finally{
      console.log("Day ended, shop closed")
    }
}

// Trigger
kitchen();
```

The result looks like this when the shop is open: 👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/lptup827qau72e83deuv.png)

The result looks like this when the shop is closed: 👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/r8pjz1qlw58ap8pq7crz.png)

So far so good.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cnkgk63x51wth2byxzfe.png)

Let's complete our project.

Here's the list of our tasks again: 👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7wthn0jr5vw7vb02e4qg.png)

**Chart contains steps to make ice cream**

First, open our shop

```javascript
let is_shop_open = true;
```

Now write the steps inside our `kitchen()` function: 👇

```javascript
async function kitchen(){
    try{
	await time(2000)
	console.log(`${stocks.Fruits[0]} was selected`)

	await time(0000)
	console.log("production has started")

	await time(2000)
	console.log("fruit has been chopped")

	await time(1000)
	console.log(`${stocks.liquid[0]} and ${stocks.liquid[1]} added`)

	await time(1000)
	console.log("start the machine")

	await time(2000)
	console.log(`ice cream placed on ${stocks.holder[1]}`)

	await time(3000)
	console.log(`${stocks.toppings[0]} as toppings`)

	await time(2000)
	console.log("Serve Ice Cream")
    }

    catch(error){
	 console.log("customer left")
    }
}
```

And here's the result: 👇

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/qs9yccq9209u7m9lquju.png)

# Conclusion

Congratulations for reading until the end! In this article you've learned:

-   The difference between synchronous and asynchronous systems
-   Mechanisms of asynchronous JavaScript using 3 techniques (callbacks, promises, and Async/ Await)

Here's your medal for reading until the end. ❤️

### Suggestions and criticisms are highly appreciated ❤️

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/usxsz1lstuwry3jlly4d.png)

**YouTube [/ Joy Shaheb](https://youtube.com/c/joyshaheb)**

**LinkedIn [/ JoyShaheb](https://www.linkedin.com/in/joyshaheb/)**

**Twitter [/ JoyShaheb](https://twitter.com/JoyShaheb)**

**Instagram [/ JoyShaheb](https://www.instagram.com/joyshaheb/)**

# Credits

-   [Collection of all the images used](https://www.freepik.com/user/collections/promises-article/2046500)
-   [Unicorns](https://www.flaticon.com/packs/unicorn-4), [kitty avatar](https://www.flaticon.com/packs/kitty-avatars-3)
-   [tabby cat](https://www.pexels.com/photo/brown-tabby-cat-with-slice-of-loaf-bread-on-head-4587955/), [Astrologist Woman](https://www.pexels.com/photo/young-female-astrologist-predicting-future-with-shining-ball-6658693/), [girl-holding-flower](https://www.pexels.com/photo/woman-in-white-dress-holding-white-flower-bouquet-3981511/)
-   [Character emotions](https://www.vecteezy.com/vector-art/180695-people-mind-emotion-character-cartoon-vector-illustration)

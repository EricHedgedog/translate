### Preload, Prefetch And Priorities in Chrome
### Chrome浏览器中的预加载、预读取和优先级

Today we’ll dive into insights from Chrome’s networking stack to provide clarity on how web loading primitives (like <link rel=“preload”> & <link rel=“prefetch”>) work behind the scenes so you can be more effective with them.
今天我们将要深入洞察Chrome的网络堆栈，来明晰 web 加载基元（如 <link rel=“preload”> 和 <link rel=“prefetch”>） 在幕后是如何工作的，这样你就能够更有效率的使用它们。

As covered well in other articles, preload is a declarative fetch, allowing you to force the browser to make a request for a resource without blocking the document’s onload event.
正如在其他文章中论述的很充分，预加载是一个声明式读取，允许你在不阻塞文档的装载（onload） 事件的情况下强制浏览器对一个资源提出一个请求。

Prefetch is a hint to the browser that a resource might be needed, but delegates deciding whether and when loading it is a good idea or not to the browser.
预读取是给浏览器的一个提示，一个资源可能会被需要，但是由委托来决定是否加载它和何时加载它对浏览器来说是一个好主意   ！！！！！

图片

### Preload success stories in production sites
Before we dive into the details, here’s a quick summary of some positive impact to loading metrics that have been observed using preload in the last year:
### 预加载
在我们深入细节之前，这是去年观察到的使用预加载后对加载指标的一些积极影响的一个简易小结：

Housing.com saw a ~10% improvement in Time to Interactive when they switched to preloading key late-discovered scripts for their Progressive Web App:
当 Housing.com 把他们的渐进式网页应用 （Progressive Web App）切换到后来发现的预加载关键脚本后，注意到可交互时间上有一个 10% 的提高：

图片



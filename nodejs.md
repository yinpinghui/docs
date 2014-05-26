#nodejs介绍#
***


## 什么是nodejs##

nodejs是Ryan Dahl在09年开发出来的，底层基于C,C++，上层内置了一个V8引擎的框架，可以用javascript作为开发语言进行开发的运行环境。最初设计的是为了在服务器端运行javascript，目前，则可以被广泛应用到各个层面和领域。



##nodejs能做什么##

Node.js采用事件驱动、异步编程，为网络服务而设计。
Node.js的设计思想中以事件驱动为核心，它提供的绝大多数API都是基于事件的、异步的风格。以Net模块为例，其中的net.Socket对象就有以下事件：connect、data、end、timeout、drain、error、close等，使用Node.js的开发人员需要根据自己的业务逻辑注册相应的回调函数。这些回调函数都是异步执行的，这意味着虽然在代码结构中，这些函数看似是依次注册的，但是它们并不依赖于自身出现的顺序，而是等待相应的事件触发。事件驱动、异步编程的设计，重要的优势在于，充分利用了系统资源，执行代码无须阻塞等待某种操作完成，有限的资源可以用于其他的任务。此类设计非常适合于后端的网络服务编程，Node.js的目标也在于此。在服务器开发中，并发的请求处理是个大问题，阻塞式的函数会导致资源浪费和时间延迟。通过事件注册、异步函数，开发人员可以提高资源的利用率，性能也会改善。

nodejs目前广泛的被使用在web编程中，特别是与传统的j2ee开发web应用程序相比，其开发速度，性能，启动时间等都具有一定的优势。在nodejs的web编程领域，有express等特别成熟的框架，同时结合配合html5的websocket，也同样有socket.io这样优秀的nodejs模块，可以非常方便的开发支持websocket的程序。

如果仅仅认为nodejs只是开发web程序，那么就有些局限了。诚然，nodejs在web编程领域风生水起，但是在其他领域，也非常的出色。由于nodejs可以直接通过c与OS直接打交道，因此，可以进行file io,network io等操作。我们可以利用nodejs进行脚本编写(类似shell)，开发代理服务器（类似apache,nginx),甚至也可以在树莓派这样的开发板上做嵌入式开发。

目前INTEL有个项目，叫做node-webkit(实际上是一个在intel工作的中国人自己的开源产品)，可以将nodejs与chromium结合，进行桌面程序开发。可见，nodejs的应用场景非常广泛。


## nodejs与java比较##
其实拿nodejs与java对比不太合适，应该是javascript与java对比，nodejs与jdk对比，相应的，基于nodejs的expressjs就应该对比springmvc等，不过我们似乎愿意将nodejs直接对比到java,也就是广义的java开发，指的是j2ee,springmvc，都可以。

java的运行是需要JVM支持的，通过JVM上运行的java程序，可以有效的避免平台的问题。而相比较而言，nodejs更加的底层，因此，在做类似于shell脚本的时候，nodejs更加有效。

语言层面，java语言的啰嗦是大家有目共睹的，其有好处，也有不好。javascript相比较java来说，简单很多，大多从前端开发出身的人员，都可以快速上手。但是由于javascript语言的一些弊端，使得开发程序不如java那么标准，那么容易产业化。所以，各有利弊。可以这么说，开发大型应用，java合适，开发小型，简单应用，或者工具类应用，nodejs更胜一筹。





## nodejs与python比较##
python语言是一个非常成熟的，具有面向对象的函数型语言，python的生态圈也很成熟，从网络编程，桌面编程，数据库编程，运维脚本等各个领域，python都是相应的框架支持。
从语言上，python语言较之javascript语言，要高级很多，也成熟很多，但是会python的人远远小于会js的人，因此，如果不开发大型程序，nodejs和python没有太大区别，代码量，代码复杂度都差不多。

nodejs由于还在发展期，毕竟不能与python的整个完善生态圈进行对比，但是，由于nodejs是、可以是底层程序，因此完全可以通过nodejs调用python程序，相互交织，相互取长补短。



##nodejs与os##

上面提到，nodejs与操作系统，与文件系统可以很好的直连，这比java要好很多，代码书写也简单很多，对于读取，控制	CPU,内存等，都有现成的api。此外，可以通过shell包(npm 包)，或者直接调用shell命令，将nodejs与shell脚本连接起来，达到与操作系统紧密连接的状态。
## nodejs与nosql##

在nodejs的支持和读写上，可以说nodejs完胜java语言，特别类似mongodb这样文档性数据，更是天生就要和nodejs在一起工作。

nosql是这两年风声水起的一个圈，其中包括mongodb,redis,neo4j,hbase,Cassandra，等多种多样的。而目前中小型互联网公司用的最多的，就是mongodb一记redis。mongodb是基于非常像json的bson数据格式存储。而redis存储的是key-value对。在nodejs里面都有非常出色的接口，非常方便的将数据存储到数据库里面，读写速度都非常惊人。

相比较而言，java则要按部就班的将数据转换成Object，之后在输出到数据库中，这种方式在关系型数据库中非常有效，但是在nosql的环境内，就显得非常死板，麻烦。

##nodejs与网页开发##

nodejs应用最多的是web开发，因此不得不专门提及一下web开发。nodejs在网页程序开发中，具有的最大的优势是前后端开发语言是一种，因此对象传递过来后，不需要像java在服务器短进行data binding，以及做前后端验证用两套逻辑。在nodejs的世界里，完全有可能用一套逻辑进行验证判断。

当然如果后端的业务逻辑复杂，业务系统庞大，我们还是不建议用nodejs进行开发。这更多的从产业开发结构考虑，而非语言本身。
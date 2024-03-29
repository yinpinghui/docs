#html介绍
**本文重点介绍HTML5的一些新特性，大家可以依次考虑在使用中的场景**


相信大家都听过html5，互联网上大肆宣扬，甚至都有html5拯救世界，形成大一统的趋势。html5之所以如此的被提及，被热炒，是与移动互联的快速发展密不可分的。当移动互联与传统互联相互交织的时候，技术上，我们希望PC端，平板端，手机端，以及大家可能接触不到的其他外设，触屏等都可以快速有效的开发。而html5恰恰可以在UI层面，可以统一整个开发。

>**<b style="color:red">UI一定要用HTML去解决</b>**

传统意义上，HTML+JAVASCRIPT+CSS只是应用到浏览器上的语言组合，而如今，在pad，手机上，也可以利用这些进行开发。当然，本质上，依然是这些语言组合跑在一个浏览器上，这个浏览器可以有PC机浏览器提供，也可以由app的内置浏览器提供，同理，我们也可以开发出PC的客户端程序，利用一个内嵌的浏览器，外部包装一个壳，由壳解决所有的文件存储，设备读取，与操作系统打交道，而所有的显示，全部由内置的浏览器展示的html代码解决。

广义上，我们理解HTML5，不要仅仅从HTML5的字面意思去理解，更应该放之到整个支持HTML5的生态环境中去考虑，比如浏览器，Javascript包，操作系统，程序员，应用商店，生产厂商，终端用户等等多方位去考虑。保持与最新的技术同步，不仅仅可以了解世界最前沿的技术，也可以将这些使用场景，应用到我们的教育领域中。新的技术带来的是新的眼界，新的用户体验，新的软硬件结合模式，以及新的开发工具，开发方式。

>**<b style="color:red">一切的技术都是要为业务服务的，至少在我们当下，切不可本末倒置</b>**



详细的html5的介绍可以参考[这里](https://speakerdeck.com/adamlu/html5gai-lan)，对于html5的特点，我的总结如下。



- 简单有效
- 语法一脉相承
- 功能强大
- 显示效果丰富
- 多种设备支持
- 更多的社区，更多的案例
- 衔接未来

对于上面的ppt，是比较全面的介绍了html5对于html5的新特性，包括语法层面，css3，javascript的新api，以下我重点介绍几个，我个人认为能与我们实际相结合的。当然一定不要局限到我介绍的这些点上，因为对于是否我们可以结合，是限于我这周的观察以及对未来的预期得到的。对于产品的认知，大家都要比我更清晰，因此，如何发现技术能给我们带来的新奇，是需要大家<b style="color:red">擦亮双眼，开动脑筋，仔细思考后</b>才能获得的。

***

###本地存储(localstorage,sessionStorage,indexedDB,application cache) ###

我们知道，传统的浏览器因为安全考虑，唯一能访问硬盘的地方就是cookie，而cookie存放的大小是收到限制的。在html5后，支持html5的浏览器将本地存储的能力扩大了，通过localstorage，indexedDB等多种存储机制，可以将很大一部分信息存放在本地，严格的说,html5的程序在离线(offline)的状态下，也是可以达到运行的能力的(依赖开发人员的开发)。可以想象，用户在没有网络，或者网络环境不好的情况下，也是可以使用程序的，当网络重新连接后(online),可以将用户操作的数据传递到服务器端。

看到这里，大家想起了什么？离线游戏，还是google gear?没错，google gear最初的设想就是这样，不过随着html5的出现，google的这个项目也宣告关闭。利用这个特性，也方便开发出离线的html5游戏，不需要网络连接即可使用。

当然，如果通过上面提到的，对于自主开发的PC客户端，或者混合式app，都是通过一个壳+内置浏览器的机制实现的，这个壳就有了更多的文件读取能力(os file, local db)，则可以不完全依赖这些机制，或者相当于继续扩展了文件读写能力，设备读写能力。我们熟知的豌豆荚PC端，就是通过这个方式开发的。类似的qq程序的qq空间也是这个思路。

我们自己的客户端软件，无论是PC端的教师程序，还是android端的学生程序，都是可以这个思路考虑。由于加入了离线存储能力，相应的，不用所有资源每次都从服务器索取，自然的减少了对服务器的压力，从一点上，就自然的获取了更大的并发的解决方案。

>online,offline也都是html5的api


###画布(canvas,css3,webgl) ###
canvas是html的一个新特性，基于此，能创造出无与伦比的图形，比如[d3.js](http://d3js.org/)
。通过canvas，结合一些合适的js引擎，可以制作出很多游戏，而这些游戏的性能表现都还不错，结合webgl的能力，可以制作出一些大场面的游戏。虽然这些游戏相比于原生的，基于openGL的一些游戏，流畅性还有差距，但是简单的游戏还不是问题。

当然我们关注的不是游戏，而是关注的人机互动性。canvas的出现，恰恰是html5用来对抗flash的工具。flash相当于元件+时间轴+ActionScript,而对应到html5就是图片素材+canvas+javascript。相比于flash的开发，js的优势很是明显

- js语言前端程序员自然掌握，不需要重新学习as
- 设备适配，只要是支持html5的设备都支持，Flash需要额外插件(iphone,ipad不支持)
- 省电


画布不仅仅能够实现2d的绘画，同样也可以制作3d的绘画，这在一些自然学科中，相当有用，数学，几何，物理，自然，地理，包括统计分析结果等，都可以使用。

由于使用的是js语言，因此，与网页开发中的各种事件能够一脉相承，比如鼠标单击，双击，手指触控，放大缩小，滑动，等各种动作，因此通过这些特性，可以带来更加的互动性，能够用来制作出更通用，更趣味，更有价值的课件，素材。


###网络通信(websocket) ###
传统的浏览器，我们知道客户端与服务器端的访问，都是通过http协议进行通信，http协议是一个(req/res)模式的通信协议，也就是说，客户端发送一个请求(GET,HEAD,POST,PUT,DELETE,OPTIONS,TRACE,CONNECT)，服务器端回复这个请求，当回复完毕，这个请求完毕，连接关闭，下一个请求，重新连接，并且与上次请求没有任何关联（也就是无状态协议）。

html5的出现，提供了websocket协议，使得在这些请求的基础上，我们可以利用更加底层的socket连接，与服务器进行通信。这在一些实时性的应用中得到了充分的体现，比如聊天室等等。

websocket的出现算是一个具有划时代意义的特性，由于它的出现，使得浏览器具有了C/S的一些能力，比如server端可以进行push操作，这在以前，必须通过http的轮询才能达到这种效果，轮询的时间间隔短了，对于服务器造成了不必要的压力，轮询的时间间隔长了，达不到实时的push的效果。

通过websocket，服务器可以将许多信息实施的推送到前端，典型的而案例就是广播，服务器端可以将信息统一的发送给一个群体。

由于websocket是socket连接，传输的数据可以是字节流，在结合视频，音频标签，可以进行双向的语音视频传播。

当前，用websocket结合canvas，可以做出大型的基于网页的html5在线游戏，刨除游戏本身不考虑，其技术架构也就是我们要做的技术框架。


###视频,音频,摄像头(video，audio,camera) ###
以往在浏览器上展示视频，音频，比如内嵌一个插件，无论这个插件是activex的，还是flash，都是需要一个外置的工具才能播放。对于PC端，由于大家基本默认都安装了flash的插件，因此大家也都习惯了声音和视频的展示，以为这是理所应当的，而在android和ipad上，这些就不是必备的了。

而html5的video,audio确可以内置的解决了这个问题，只有支持html5的浏览器，都可以支持
video,audio的标签，都可以自然播放视频和音频，当然，不是所有的视频和音频格式都支持，不过，这已经是非常方便了。



###响应式设计 ###

严格说，这个并不是html5的特性，这只是html5大行其道之后，对于页面开发时，提出的要求。为了减少开发工作量，我们希望一段html代码，可以在多个设备上不同屏幕大小上，都可以表现出合理的，美观的页面，于是，便提出了响应式设计的理念。

基于响应式设计的最著名的开发框架，应该是twitter的[bootstrap](http://getbootstrap.com/)，当然类似的开发框架也很多，只是都不如bootstrap的资源多。



由于移动互联的广泛开展，各种新技术的层出不穷，技术与技术之间的交织，JAVA8，spring4，nodejs，html5，cocos2dx等等。为了构建公司层面的技术框架，我们需要对多种技术有所了解和认知，才能做出相对正确的决定。


curl -H 1.zip -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjhkOWM2NjQwLThkNDEtMTFlYi1iYTMyLTU1ZmZjYTExOTcwZSIsInVzZXJuYW1lIjoieWFuZ2ciLCJjb21wYW55Ijp7ImNyZWRpdENvZGUiOiI5MTExMDAwMDEwMDAxMjg4NTUifSwiZnVsbE5hbWUiOiLmnajmtLgiLCJ0ZWwiOm51bGwsIm1vYmlsZSI6IjMwMjMyIiwidXNlcklkZW50aXR5Ijp7ImF1dGhvcml0eSI6InVzZXIifSwic3lzdGVtX2NvZGUiOiJPQSIsImlhdCI6MTY0MDU2ODI3MywiZXhwIjoxNjQwNjExNDczfQ.hrdl_9WHwlZmKNlz2MUhHkSMvKHp3R7UyIGE2tgpqM8' https://devoa.poly.com.cn/api/file/upload
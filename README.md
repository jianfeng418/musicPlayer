# musicPlayer
h5 编写的音乐频谱播放器
利用h5的Audio的API对音乐源文件进行解码，得到频谱信息，进行canvas绘图，得到频谱图：

通过fileReader读取音乐数据，在音乐到达播放器进行播放前对其进行拦截，这个拦截工作是由window.AudioContext来做的，我们所有对音频的操作都基于这个对象。通过AudioContext可以创建不同各类的AudioNode，即音频节点，不同节点作用不同，对音频数据进行频谱分析即本文要用到的(AnalyserNode)，得到的数据频谱数据进行canvas绘制，要让整个画面动起来，需要更新频谱数据，window.requestAnimationFrame()正好提供了更新画面得到动画效果的功能。


![Image text]( /vtree.png )

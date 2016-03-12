# MemoEveryDay

##ios6、ios7、ios8、ios9 auto layout cell

FDTemplateLayoutCell



##ios run loop mode
NSDefaultRunLoopMode:    App默认Mode,当没有接收到ScrollView滚动是，主线程通常使用这个Mode
NSTrackingRunLoopMode:  到接收到ScroolView或其子类的时候，主线程就会切换到这个模式下运行。
UIInitializationRunLoopMode：当App启动时使用的第一个Mode,当启动完成后不再使用。
NSRunLoopCommonModes，是一个tag,本质上不是一个Mode,默认                    
NSDefaultRunLoopMode和NSTrackingRunLoopMode都绑定这个tag。
　　(应用场景：有时候我们需要添加一个NSTimer在RunLoop,在这时需要制定一个Modes，现在的  需求是:我们既要在默认模式下要监听，在滚动模式下也要监听，但只能制定一个模式，这是可以制定这个CommonMode)
GSEventReceiveRunLoopMode：接受系统内部的Mode,通常做不到。

处理不同事件使用不同的Mode，可以最大限度的把性能的最大化处理不同分类的事件，提高性能。

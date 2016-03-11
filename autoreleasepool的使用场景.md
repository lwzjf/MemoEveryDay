# MemoEveryDay

来源：苹果官方文档

Cocoa always expects code to be executed within an autorelease pool block, otherwise autoreleased objects do not get released and your application leaks memory. 
(If you send an autorelease message outside of an autorelease pool block, Cocoa logs a suitable error message.)
The AppKit and UIKit frameworks process each event-loop iteration (such as a mouse down event or a tap) within an autorelease pool block.
Therefore you typically do not have to create an autorelease pool block yourself, or even see the code that is used to create one.
There are, however, three occasions when you might use your own autorelease pool blocks:

  ・ If you are writing a program that is not based on a UI framework, such as a command-line tool.

  ・ If you write a loop that creates many temporary objects.

  ・ You may use an autorelease pool block inside the loop to dispose of those objects before the next iteration. Using an autorelease pool block in the loop helps to reduce the maximum memory footprint of the application.

  ・ If you spawn a secondary thread.

  ・ You must create your own autorelease pool block as soon as the thread begins executing; otherwise, your application will leak objects. (See Autorelease Pool Blocks and Threads for details.)


NodesCoordinates
================

SpriteKit坐标系  


为了测试SpriteKit中SKNode及其子类而写的小程序  

主要逻辑都在Button类，通过组合的方式加入了SKNode和SKSharpNode对象，用来绘制在正中央的Node和其原点  

运行后看到屏幕下方有五行字，好吧也是五个按钮，按一下显示对应的Node，再按一下擦除  

这五个Button都继承自Button类，便于拓展，通过类名构造对象的代码如下：  

``` 
- (id) createInstanceByClassName: (NSString *)className {
    Class aClass = NSClassFromString(className);
    id anInstance = [[aClass alloc] init];
    return anInstance;
}
``` 

Button类中还加了个original协议作为代理，其实也没多大用处，只是考虑为了以后拓展复用代码方便而已

对应文章地址：http://yulingtianxia.com/blog/2014/05/04/spritekitzuo-biao-xi/  


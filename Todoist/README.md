# Todoist

## 这是什么

这个是对于国外的todoist网站的仿站练习，暂时只考虑做基础功能，不考虑高级功能。并且由于是静态页面，所以数据库暂时只能使用indexedDB，这个只能存储在本地，但是只是为了练习js。

暂时不想要的功能：
    1.  拖动
    2.  标签
    3.  过滤器
    


## 现在的进度
    现在左侧的项目栏已经可以添加项目了



## 8月2日的更新
    创建了indexedbd数据库，并且创建了两个存储对象，
    一个用来存储每一个任务的相关数据
    另一个用来存储项目、优先级、标签
    今天并没写完左边栏，是一大败笔，明天一定要将页面的内容全部写完。

## 8月6日的更新
    修改了数据库的结构
    改变了对于项目的原有计划，在功能的实现上有了删减
    封装了一个用来修改class的函数，暂时功能只有添加和删除。
    但是对于数据库的结构还是不满意，所以还是没有将数据写进去。
## 8月7日的更新

    完善了数据库的结构
    实现了将项目添加进数据库中，使得左侧项目可以添加内容 
    完善了addClass方法，增加了修改功能现在有三个功能：添加、删除、修改
    封装了控制数据库的方法，暂时只有添加的功能

## 8月10日更新
    了解到了函数内部的arguments这个内置对象，可以帮我解决class数量不确定的问题。
    增加了数据库的删除方法  
    可以添加和删除项目，但是存在一定的问题，不管是删除韩式添加都会导致整个项目栏闪烁一下
    当视口在750px宽度以下，会自动隐藏左侧菜单，通过点击左上角可以控制出现和隐藏
## 8月22日更新
    用了好几天，将代码大改了一次，因为之前为了图省事曹成了非常多的bug，这几天基本上全部解决了
        1，每一次点击创建新的项目会导致所有存在的项目闪烁一次（已解决）大幅改动了之前的代码
        2，点击删除图标的同时，会导致同时触发修改项目标签背景色的事件（已解决）   使用 e.cancelBubble = true;
        3，点击创建或者删除后，项目标签背景色会消失或者异常（已解决）主要是因为之前添加项目的代码和和展示的代码分开写了
        4，使用addeventlistener的时候会重复监听多次同一个事件（已解决）部分使用onclick
    再次完善了changeclass方法，可以为不存在class的元素添加class。
    又掌握了一种定宽+自适应的实现方法，之前都是一侧浮动+设置margin，这次使用了table的方式。


# 8月24日更新
    发现border-collapse: collapse;和border-radiu会发生冲突，套外壳，给外壳加圆角

# 功能的主体已经完成

    经历了前两个版本的失败，终于解决了重重困难，实现了自己想要的功能。
    几个主要功能：
    1，可以正确的添加任务
    2，可以根据项目将任务分类
    3，可以根据日期将任务分开（暂时还不完善）
    
    
# 现在基本上已经是完成版

    经历了这次的成功版本我对于indexedDB的认识又加深了，对于异步编程我还差的很远，比不过我已经了解了回调这个概念，算是一个进步。
    现在数据库的结构非常不好，这是我之前对于indexedDB的认识过浅导致的。日后对于它的使用，我已经有了更好的思路。
        现在实现的功能：1，几个存贮任务的位置：收件箱、今天、标签（可以自主创建删除标签）
                     2，可以增删改任务，上面的快速查找功能并不可用。
                     3，响应式界面，左侧菜单在屏幕可见宽度小于750px是会自动隐藏，可通过点击左上方按钮控制appear&hide
                     
    


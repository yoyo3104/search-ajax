# search-ajax

利用fiddler完成本地网页在同一个域名
http://www.cnblogs.com/youhong/p/6081495.html


jquery的val（） 和 text（）
$.get(url,function,‘json’）
'http://api.bing.com/qsonhs.aspx?q='+searchText  传参怎么写
location.href跳转

jsonp格式 跨域
$.ajax({
    type : 'GET',
    url : 'http://sg1.api.bing.com/qsonhs.aspx?type=cb&cb=callback&q='+inputTxt,
    dataType : 'jsonp',
    jsonp : 'cb',
    success : function(){},
    error : function(){}
})



   url: 'http://api.bing.com/qsonhs.aspx?type=cb&cb=callBack&q='+text,
   
   
   
   jquery几种事件绑定方式的比较




---恢复内容开始---
 
比较和联系:

1.bind()函数只能针对已经存在的元素进行事件的设置；但是live(),on(),delegate()均支持未来新添加元素的事件设置；

2.bind()函数在jquery1.7版本以前比较受推崇，1.7版本出来之后，官方已经不推荐用bind()，替代函数为on(),这也是1.7版本新添加的函数，同样，可以

　用来代替live()函数，live()函数在1.9版本已经删除；

3.live()函数和delegate()函数两者类似，但是live()函数在执行速度，灵活性和CSS选择器支持方面较delegate()差些，想了解具体情况，请戳这：

　http://kb.cnblogs.com/page/94469/

4.bind()支持Jquery所有版本；live()支持jquery1.9-；delegate()支持jquery1.4.2+；on()支持jquery1.7+；
 
 更推荐on()


1、ajax和jsonp这两种技术在调用方式上”看起来”很像，目的也一样，都是请求一个url，然后把服务器返回的数据进行处理，因此jquery和ext等框架都把jsonp作为ajax的一种形式进行了封装。

2、但ajax和jsonp其实本质上是不同的东西。ajax的核心是通过XmlHttpRequest获取非本页内容，而jsonp的核心则是动态添加

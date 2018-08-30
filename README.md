# WebViewLoadH5
H5最大的优势是跨平台，开发者无需太多的适配工作，用户无需下载，打开一个 网 址 即可，就能访问了。 开发简单，开发成本低，入门门槛低，周期短，给小团队更多的机会。传播作用好，h5页面最大的优势是传播能力极强，有非常好的传播作用，是企业商家做的曝光，产品宣传的利器。

H5页面适合场景：
把手机网站当成网络上的“电子产品介绍手册”。手机网站更适合用户“主动百度搜索”或者“主动访问”，适合于陌生用户的低频或初次访问，让用户更完整和详细的获得快速介绍。通常用户使用搜索引擎、手动输入网址等形式进行访问。

H5页面不足的地方表现在软件运行速度容易受网络影响，对于摄像头、陀螺仪等硬件支持较差，开发出来的应用性能较差，不适合处理较复杂的逻辑等等。

H5的优势：

1、页面丰硕简练。H5技巧完成的网站也等于常说的相应式计划，改良了页面多媒体元素的应用成绩，以前建站页面主意削减动画、视频等的应用，因为所占的网站资本空间多，招致页面加载速率慢的环境，但现在应用H5建站，不只能够勇敢应用这些元素，且无需担忧阅读不顺畅的成绩，同时让页面显得加倍丰硕，又能包管其整齐性。

2、有利于网站优化。一个网站若不克不及很好的应用互联网资本，那末建站的代价就已不复存在，此中搜索引擎这个大平台便是资本应用的一个好渠道，由此网站必定少不了优化。H5技巧所应用的代码法式相对付旧时的编程来讲要简练得多，且应用多媒体的环境下，对搜索引擎的抓取也是异常友好的，是以网站优化起来加倍轻松。

3、进步用户体验。H5的出现，改良了网页内容被插件约束的场合排场，发明了丰硕多彩的网站，满意了用户视觉上的审美请求，且能够或许包管网站的加载速率，更重要的是以后的各类阅读器的推出，对付分歧的用户有分歧的应用习气，H5很好地兼容了各类阅读器的，让网站的出现后果不会因装备的分歧而转变，大大进步了用户体验。

4、增长用户流量。因为H5技巧完成了网站跨平台的应用，特别挪动装备的多样化，包含各类屏幕大小的手机，平板等等，毫无疑问，在挪动互联网的趋向下，泰半的用户流量将来源于挪动端的用户，H5网站的扶植，轻松拓展了用户阅读渠道，企业无需别的开辟挪动网站来得到用户流量，也异样能够或许分得挪动用户群体的蛋糕，无形中给网站增长了流量。

5、H5页面最大的优势是跨平台，开发者无需太多的适配工作，用户无需下载，打开一个网址即可，就能访问了。

6、H5页面开发简单，开发成本低，入门门槛低，周期短，给小团队更多的机会。并且维护更新简单，无需用户更新客户端，只在网站更新即可。

7、H5页面推广成本降低，推广的只是一个URL链接，二维码，不需要几十兆，几百兆的安装包去推广。

8、传播效果好，h5页面最大的优势是传播能力极强，有非常好的传播效果，是企业商家做品牌曝光，产品宣传的利器。

9、现在市面上有大量的h5页面制作软件，不需要敲代码就可以制作h5页面。大大节省开发时间。
h5页面的优势优点有很多，关键是你能发挥出来多少，h5页面是否受欢迎，是由你的内容决定的，好的内容，能让人参与进来，就是好的h5页面。因此，妙集在为客户制作H5页面时，会挖掘与品牌有关的价值信息，合理运用技术，为消费者打造流畅的互动体验。从而提高品牌的用户黏度。

webview加载H5，简单显示：

1、布局文件中添加控件（或动态添加）activity中生成控件 

2、webview必须设置支持js的属性：webview.getSettings().setJavaScriptEnabled(true); 这里还可以设置其它更多的属性 

3、加载显示页面：webView.loadUrl(“······”);

webview与H5交互：

1、js调用Android中的函数 
webView.addJavascriptInterface(obj,str); 
参数一：android中的实例对象 
参数二：js中别名 
注：如果js中调用此对象的某方法，须在此公有方法前加上注解@JavascriptInterface，否则访问不了，目前只知道这种写法只能调用对象的方法。 
如果不加webView.setWebChromeClient()这个方法，js中的alert对话框将不会提示。 
js中使用str.xx()/window.str.xx()调用android中的方法 
注：Android中的list须转换成json的字符串形式传入到js中，用eval(json)进行获取 

2、android调用js中的函数 
js中编写带参或不带参的方法 如
function init(){
    alert("js中方法显示");
}

用webView.loadUrl(“javascript:init()”);进行调用显示即可

webview中必要的属性设置：

WebSettings webSettings =  myWebView.getSettings(); 

webSettings.setDefaultTextEncodingName("utf-8");//设置编码格式

webSettings.setWebViewClient(newWebViewClient());//限制在webview中打开网页，不用默认浏览器

webSettings.getSettings().setBuiltInZoomControls();//设置是否支持缩放

webSettings.addJavascriptInterface(obj,str);//向html页面注入java对象

webSettings.setUseWideViewPort(true);//设置此属性，可任意比例缩放

webSettings.setLoadWithOverviewMode(true);// 页面支持缩放：

webSettings.setJavaScriptEnabled(true);  

webSettings.setBuiltInZoomControls(true);

webUrl.requestFocusFromTouch(); //如果webView中需要用户手动输入用户名、密码或其他，则webview必须设置支持获取手势焦点。

webSettings.setJavaScriptEnabled(true);  //支持js     

webSettings.setUseWideViewPort(false);  //将图片调整到适合webview的大小 

webSettings.setSupportZoom(true);  //支持缩放    webSettings.setLayoutAlgorithm(LayoutAlgorithm.SINGLE_COLUMN); //支持内容重新布局  

webSettings.supportMultipleWindows();  //多窗口 

webSettings.setCacheMode(WebSettings.LOAD_CACHE_ELSE_NETWORK);  //关闭webview中缓存 

webSettings.setAllowFileAccess(true);  //设置可以访问文件 

webSettings.setNeedInitialFocus(true); //当webview调用requestFocus时为webview设置节点

webSettings.setJavaScriptCanOpenWindowsAutomatically(true); //支持通过JS打开新窗口 

webSettings.setLoadWithOverviewMode(true); // 缩放至屏幕的大小

webSettings.setLoadsImagesAutomatically(true);  //支持自动加载图片



想和h5交互我使用的是webview首先就是将网页给加载出来然后再讲自己的数据传递给h5.接着再让h5调用自己的方法。

第一步：显示页面

    private void loadWebPage(String path) {
        //WebView加载web资源
        //覆盖WebView默认使用第三方或系统默认浏览器打开网页的行为，使网页用WebView打开
        //启用支持javascript
        WebSettings settings = webPage.getSettings();
        settings.setJavaScriptEnabled(true);
//        settings.setCacheMode(WebSettings.LOAD_NO_CACHE);
//        settings.setBlockNetworkImage(false);
        // 设置可以支持缩放
        settings.setSupportZoom(true);
        settings.setDefaultZoom(WebSettings.ZoomDensity.FAR);
        //能够实现交互让js拿到Android的对象
        webPage.addJavascriptInterface(new JsBrige(this), "android");

        webPage.setWebViewClient(new WebViewClient() {
            //开始和结束可以用于加载进度条
            @Override
            public void onPageStarted(WebView view, String url, Bitmap favicon) {
                super.onPageStarted(view, url, favicon);
            }

            @Override
            public void onPageFinished(WebView view, String url) {
                super.onPageFinished(view, url);
                //触发加载
                getSessionId();
            }

            //加载失败的情况下
            @Override
            public void onReceivedError(WebView view, WebResourceRequest request, WebResourceError error) {
                super.onReceivedError(view, request, error);
            }
        });
        String url = Constants.WEBURL + path;
        LogUtils.i("url..." + url);
        webPage.loadUrl(url);
    }

上面的代码基本就是对于网页的加载了。你仅仅需要传递一个加载路径。就可以将页面加载出来。

settings.setBlockNetworkImage(false);
这句代码的意思就是等待着页面加载完毕，加载图片。但是我使用过程中。会导致最后图片加载不出来。查资料发现这句话是针对低版本进行的设置。对于现在使用来说可以不用添加。


webPage.setWebViewClient(new WebViewClient() {
            //开始和结束可以用于加载进度条
            @Override
            public void onPageStarted(WebView view, String url, Bitmap favicon) {
                super.onPageStarted(view, url, favicon);
            }

            @Override
            public void onPageFinished(WebView view, String url) {
                super.onPageFinished(view, url);
                //触发加载
                getSessionId();
            }

            //加载失败的情况下
            @Override
            public void onReceivedError(WebView view, WebResourceRequest request, WebResourceError error) {
                super.onReceivedError(view, request, error);
            }
        });

这段代码是对于webview添加的监听事件主要包含onPageStarted.onPageFinished.onRecercvedError.三个方法其实监听里面还有很多的方法。

started方法是在页面加载的时候进行执行。如果你需要更换加载进度条。可以在这个方法中启动你想要的进度条格式，在finish或error方法中进行关闭就可以了，

finish方法是再页面加载完成的时候进行操作。我这个地方是再页面加载完成的时候。将我Android的唯一表示sessionid传递给h5页面。如果传递后面会说到。

error方法就是网页加载出错进行的出错处理。如果你想要对加载的网页进行拦截处理的话。你可以添加
/** 
 * 拦截 url 跳转,在里边添加点击链接跳转或者操作 
 */  
public boolean shouldOverrideUrlLoading(WebView view, String url)  
进行路径的拦截等操作。

第二步和js进行交互。同js进行交互的话需要添加

       settings.setJavaScriptEnabled(true);
       
这行代码。这个地方就是支持和js交互能力。如果忘记。就无法和h5页面进行数据的交互。

第三步：将数据传递给h5页面（这个地方需要和h5进行沟通。需要h5页面写一个方法然后你调用该方法并传递数据）

/**
* 获取到sessionid,postid
 */
public void getSessionId() {
    String sessionid = (String) SPUtils.get(this, "sessionid", "");
    //调用js中的函数：showInfoFromJava(msg)
    LogUtils.i("webActivity.." + sessionid + "jiji" + postid);
    webPage.loadUrl("javascript:submitComments('" + sessionid + "','" + postid + "')");
}

和h5交互的时候。需要向h5页面传递一个是唯一表示sessionid一个是编号postid.submitComments（）这个方法是h5页面的给创建的方便。

写法基本都是webview(对象).loadUrl("javascript:h5端的方法名（'"+参数+"'）")一个参数形式。如果你想要多个参数。那么就是我上面代码的2个参数的形式一样。往后添加就可以了。（如果你和h5交互的时候发现数据一直传递不过去。请问一下h5是否将页面部署到服务器。因为我开发过程中。h5新手没有部署服务器浪费了很多时间），通过上面的代码现在就可以将你的数据发送给h5页面。我这个地方是在加载完网页的时候将数据传递过去。所以我写在了finish方法中。你的项目可以根据你的具体情况来使用。

第四步：让h5页面调用Android的方法

public class JsBrige {
    WebAcitivty acitivty;

    public JsBrige(WebAcitivty acitivty) {
        this.acitivty = acitivty;
    }

    /**
     * 关闭当前的页面
     */
    @JavascriptInterface
    public void closePage() {
        acitivty.finish();
    }

    //js给Android 传递数据
    @JavascriptInterface
    public void print(String mes) {
        ToastUtil.show(WebAcitivty.this, mes);
    }

    @JavascriptInterface
    public void swicth() {//跳转页面
        Intent intent = new Intent(WebAcitivty.this, LoginActivtiy.class);
        WebAcitivty.this.startActivityForResult(intent,100);
    }

}

这个地方我封装了一个内部类。可能刚接触的会问为啥要创建一个内部类呢？主要原因还是为了安全。因为如果你不写内部类很可能被一些不法分子将你本类的其他方法的功能给窃取走造成一些不必要的麻烦。这个地方写一个内部类。让h5页面仅仅能够访问内部类相对就安全多了。上面的代码中时我项目中h5对我页面的操作。页面跳转和关闭等，@JavascriptInterface这个注解的作用也是起到安全的效果。主要是在页面注入的时候防止攻击提供的一个方式。

//能够实现交互让js拿到Android的对象：
webPage.addJavascriptInterface(new JsBrige(this), "android");
这行代码就是让h5页面拿到你的内部类然后调用相关的方法执行对应的操作。“android”这个是h5页面拿去的你的对应。相当于new JsBrige(this)这个。基本到这里就已经实现了h5和Android的交互。


常见问题：如果还没有实现交互。

可能：

1.就是h5页面没有进行数据的部署。

2.就是你写的交互方法单词错误。

3.没有同意js交互（setJavascriptEnabled(true）)

4.仔细检查你的代码。如果确定没有问题，就让h5对他的代码进行检查。或者找ios端看看他是否能够交互。


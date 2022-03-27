
# learn path

<a href="https://ibb.co/R6YFQsj"><img src="https://i.ibb.co/FYmr8yH/angule.png" alt="angule" border="0"></a>

# 在线书籍
* [Angular开发入门与实战 2021](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8c)

# 博客

[精尽 Angular 学习指南](http://svip.iocoder.cn/Angular/tutorials/)|[Angularjs进阶](https://www.kancloud.cn/digest/angularjs-sunny1989)|
---|---|

[Element for Angular](https://github.com/ElemeFE/element-angular)|
----|


# 目录
* 基础
  * [Node.js和npm基础 ](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck98f3284021498f137082c2e)
  * [TypeScript基础知识](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck33e3289021c33e75ff09694)
* Angular---Angular的架构采用MVVM模式设计
  * [Angular项目的启动过程](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck64232b60230642e92efb54c)
  * 1 [Angular模块---Angular模块是带有@NgModule()装饰器声明的类，Angular模块的主要作用是管理指令、管道、组件](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8c)
      * 从技术角度将Angular模块分类
        * Angular根模块---根模块是系统默认生成的      
        * Angular特性模块---特性模块是由用户在开发过程中逐个增加的 
        * [常用内置模块](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck32b321d024832bb90e89958)---无论是根模块还是特性模块，其实都可以引用这些内置模块
      * [从业务角度对Angular模块进一步分类](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckd2d32c50249d2ddea18fb39)
        * 根模块（AppModule）
        * 核心模块（CoreModule）---，因此在核心模块中定义的服务就是单例服务,核心模块又可以称为核心服务模块。只有根模块AppModule才能导入核心模块。如果一个其他特性模块也导入了它，该Web应用程序就会为该服务生成多个实例
          * [防止重复导入核心模块 ](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckd2d32c50249d2ddea18fb39)
        * [共享模块（SharedModule）](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckd2d32c50249d2ddea18fb39)
        * 其他特性模块 
      * [如何正确地分割模块---这里采用的核心模块是Service模块，而共享模块是Widget模块。核心模块只在根模块AppModule中导入一次，共享模块在需要它的所有特性模块中导入](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckad63251024aad61ab143c7e)
  * 2 Angular对象
    * [2.1 Angular组件对象](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckc0c320a0232c0c7c76d365a)
      * [Angular组件设计就是采用的MVVM模式](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckc7432af0210c74d97b01b1c) 
        * [MVVM模式的优点](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckc7432af0210c74d97b01b1c) 
        * M（Model）：模型---双向绑定技术：当Model变化时，ViewModel会自动更新，View也会自动变化
          * Model是Component类中的数据
        * V（View）：视图，它专注于界面的显示和渲染，Angular中的View就是组件模板---低耦合：各层职责分开，可以各干各的事情，如View可以独立于Model变化和修改
          * [Component中的组件模板就是MVVM模式中的V，它扮演的是一个视图的角色，简单来说就是展示给用户看的部分](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck9a132c802349a1158154a83)
            * [组件模板的样式](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckd8232f00235d82c8d161fb2) 
            * [Angular模板语言](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck0723244023c072b030ba601)
              * 插值
              * Angular模板表达式
              * 模板语句
              * 数据绑定 
        * VM（ViewModel）：视图模型，ViewModel是用来连接View和Model的桥梁，View Model将Model中的数据提供给View用于展示，同时将View中用户更改的数据同步到Model中 ---1 可重用性：View的计算逻辑放在ViewModel里，让很多View可以重用这段计算逻辑, 2 独立开发：开发者可以专注于业务逻辑和数据的开发（ViewModel），设计人员可以专注于界面的设计, 3 测试方便：可以针对ViewModel来对界面进行测试。
          * [Angular中的组件类就是MVVM模式中的VM（ViewModel，视图模型），ViewModel是View和Model的结合体，负责View和Model的交互和协作。组件类的作用是控制模板渲染,ViewModel是Component类中的代码](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka6832360236a684eceeee20) 
      * [组件类与模板的数据绑定方式](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckb5332110237b53b3a3d68d2) 
        * 单向数据绑定
          * [Angular模板语言](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck0723244023c072b030ba601)
            * 插值
            * Angular模板表达式
            * 模板语句
            * 数据绑定 
          * 使用插值显示属性的值---数据绑定方向是从组件类到视图, 在模板视图中显示组件类的属性，最简单的方式就是通过插值绑定属性名。插值的语法就是把属性名写在双花括号里，如{{message}}
          * 属性绑定方式---数据绑定方向是从组件类到视图
            * DOM属性绑定
            * HTML特性绑定
              * HTML特性绑定
              * Class样式绑定
              * Style样式绑定  
          * 事件绑定---数据绑定方向是从视图到组件类  
        * 双向数据绑定---双向数据绑定为Web应用程序提供了一种在组件类及其模板之间共享数据的方式
      * [组件的交互](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck72b327f023972b32a1f7e2d)
        * 装饰器
          * @Component()装饰器
          * @Output()装饰器
          * @Input()装饰器
          * [@ViewChild()装饰器](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck44f328c023e44f683a8420b)
          * [@ViewChildren()装饰器](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck44f328c023e44f683a8420b)
          * [@ContentChildren()装饰器](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck73532580243735b90b45ac8)
          * [@ContentChild()装饰器](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck73532580243735b90b45ac8)
          * [@Directive()装饰器](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka3f32db0244a3f390d88bb9) 
          * [@HostBinding()装饰器](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka3f32db0244a3f390d88bb9)
          * [@HostListener()装饰器](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka3f32db0244a3f390d88bb9)
          * @NgModule()装饰器
    * [2.2 ElementRef对象](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka3f32db0244a3f390d88bb9)---ElementRef对象：可以通过ElementRef对象的nativeElement属性直接访问应用该指令的DOM元素
    * [2.3 Renderer2对象](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka3f32db0244a3f390d88bb9)---Renderer2对象：Renderer2对象可实现自定义渲染器，它提供了许多辅助方法，如可以通过该对象修改DOM元素的样式。
   * [3 Angular指令](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckfc432fb0241fc490ca45614)---指令是DOM元素上的标记（如属性），它告诉Angular要将指定的行为附加到现有DOM元素。指令的核心是一个函数，只要Angular编译器在DOM元素中找到指令，该指令就执行。指令通过赋予HTML新语法来扩展其功能
        * [结构型指令---这些指令可以通过添加和删除视图DOM元素来更改DOM布局](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck32932b102423295c76ac7d9)
          * NgIf
          * NgFor
          * NgSwitch
          * ng-container分组元素
        * [属性型指令---只是改变一个DOM元素的外观或行为](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck73532580243735b90b45ac8)
          * NgClass
          * NgStyle
          * NgContent 
        * [在指令中监听事件](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka3f32db0244a3f390d88bb9)
   * 4 管道 
# Angular 项目实战
* [Angular 10 Tutorial](https://www.javaguides.net/p/angular-10-tutorial.html)
* [Free Open Source Angular Projects or Templates 系列](https://www.javaguides.net/2019/04/free-open-source-angular-projects-or-templates.html)
* [Free Spring Boot Angular Open Source Projects 系列](https://www.javaguides.net/2020/06/free-spring-boot-angular-open-source-projects-github.html)
* [Spring Boot + Angular 8 + WebSocket Example Tutorial](https://www.javaguides.net/2019/06/spring-boot-angular-8-websocket-example-tutorial.html)
* [Angular + Spring Boot CRUD Full Stack Application](https://www.youtube.com/playlist?list=PLGRDMO4rOGcNzi3CpBWsCdQSzbjdWWy-f)
* [Angular + Spring Boot REST API Example Tutorial ](https://www.youtube.com/watch?v=_rMAnZIcRiU)
* [Angular + Spring Boot + MySQL CRUD Example](https://www.javaguides.net/2020/07/spring-boot-angular-10-crud-example-tutorial.html)
* [Spring Boot + Angular 10 CRUD Full Stack - Part #1 - Build CRUD Rest APIs with Spring Boot and MySQL](https://www.javaguides.net/2020/07/spring-boot-angular-10-crud-part-1-develop-springboot-crud-rest-apis.html)
* [Spring Boot + Angular 10 CRUD Full Stack - Part #2 - Create Angular 10 App](https://www.javaguides.net/2020/07/spring-boot-angular-10-crud-part-2-create-angular-10-app.html)
* [Spring Boot + Angular 10 CRUD Full Stack - Part #3 - Develop Angular 8 CRUD Operations](https://www.javaguides.net/2020/07/spring-boot-angular-10-crud-part-3-develop-angular-10-crud-operations.html)
* [Spring Boot + Angular 10 CRUD Full Stack - Part #4 - Angular 10 App Configuration](https://www.javaguides.net/2020/07/spring-boot-angular-10-crud-part-4-angular-10-crud-app-configuration.html)
* [Spring Boot + Angular 10 CRUD Full Stack - Part #5 - Running Angular 10 CRUD App](https://www.javaguides.net/2020/07/spring-boot-angular-10-crud-part-5-running-angular-10-crud-app.html)
* [Spring Boot + Angular + MongoDB CRUD Example](https://www.javaguides.net/2021/08/spring-boot-angular-mongodb-crud-example.html)
* [Angular Spring Boot Login and Logout Example](https://www.javaguides.net/2021/08/angular-spring-boot-login-and-logout.html)
* [Spring Boot + Angular + PostgreSQL CRUD Example](https://www.javaguides.net/2021/08/spring-boot-angular-postgresql-crud.html)

# Angular 例子程序
* [AngularJS Hello World Example](http://websystique.com/angularjs/angularjs-hello-world-example/)
* [AngularJS Modules Explained Example](http://websystique.com/angularjs/angularjs-modules-explained/)
* [AngularJS Controllers Explained with Examples](http://websystique.com/angularjs/angularjs-controllers-explained-with-examples/)
* [AngularJS Form Validation Example](http://websystique.com/angularjs/angularjs-form-validation-example/)
* [AngularJS Services Dissected](http://websystique.com/angularjs/angularjs-services-dissected/)
* [AngularJS $http service example-server communication](http://websystique.com/angularjs/angularjs-http-service-example-server-communication/)
* [Angularjs Server Communication using ngResource-CRUD Application](http://websystique.com/angularjs/angularjs-crud-application-using-ngresource/)
* [AngularJS Built-in+Custom Filters Dissected](http://websystique.com/angularjs/angularjs-filters-explained-builtin-custom-filter-example/)
* [AngularJS Routing Tutorial using ngRoute](http://websystique.com/angularjs/angularjs-routing-tutorial-using-ngroute/)
* [Angularjs Routing Tutorial using ui-router](http://websystique.com/angularjs/angularjs-routing-tutorial-using-ui-router/)
* [AngularJS Directives Tutorial](http://websystique.com/angularjs/angularjs-directives-tutorial/)
* []()
* []()


# 视频

* [尚硅谷_AngularJS视频](https://www.bilibili.com/video/av27138197?from=search&seid=14365941790008031585)
* [尚硅谷前端：AngularJS+Zepto框架学习](https://www.bilibili.com/video/av67369734?from=search&seid=1207868749551698080)

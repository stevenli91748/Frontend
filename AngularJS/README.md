
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
* Angular理论---Angular的架构采用MVVM模式设计
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
    * [2.1 Angular组件对象---组件应只负责用户体验，不应该负责如何去直接或间接地获取数据，也不应该关心自己展示的数据是真实的还是模拟的假数据](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckc0c320a0232c0c7c76d365a)
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
          * @Injectable()装饰器
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
   * [4 管道---管道的作用是对模板表达式的结果进行一些转换，如将文本更改为大写、格式化日期显示、将数字显示为本地货币格式，或过滤列表并对其进行排序等,在整个Web应用程序中，管道用于获取数据，转换数据，然后把这些数据显示给用户 ](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck76d325c028076dc611d6d8c)
     * [内置管道](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck9b832a602829b86192511b5)
       * 异步管道
       * 金额管道
       * 百分比管道
       * JSON管道
       * 大小写转换管道
       * 日期格式转换管道 
       * i18nSelect管道
     * [自定义管道 ](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck1af32e502831afa34a7fe44)
*  Angular应用
   * 5 [Angular路由功能---Angular路由（Router）使开发者可以构建具有多个视图的单页应用程序，并允许用户在这些视图之间导航 ](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck35f3251024e35f4a8d46404)
       * 路由配置
       * 路由器出口 
         * 主路由出口
         * 命名路由出口
         * [使用路由器链接](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckf03328d0250f033ab37c722)
           * 路由链接的激活状态
           * 路由器状态---路由器状态在Angular中用RouterState对象表示，RouterState对象维护的是一个路由器状态树，表示所有的路由器状态
           * [在路由中传递参数](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck977321c02529778d5d2116b)
             * [传递配置参数](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8c)
             * [传递路径参数](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8c)
               * 必选参数
               * 可选参数  
               * 传递查询参数
            * [路由器触发的事件](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck43e327b025143ec517d680b)
             * NavigationStart事件---表示导航周期的开始。
             * NavigationCancel事件---取消导航，如可用在路由守卫（Route Guards）中，拒绝用户访问此路由。
             * RoutesRecognized事件---当URL与路由匹配时，触发此事件。
             * NavigationEnd事件---在导航成功结束时触发 
           * [路由守卫--守卫的意义是判断当前用户在进入路由或者离开路由的时候，是否有权限或者有未完成的操作](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckfe932230253fe9fc289c8a3)
             * CanActivate守卫，用来处理导航到某路由的逻辑
             * CanActivateChild守卫，用来处理导航到某子路由的逻辑
             * CanDeactivate守卫，用来处理从当前路由离开的逻辑
             * Resolve守卫，用来在路由激活之前获取业务数据
             * CanLoad守卫，用来处理异步导航到某特性模块的逻辑 
           * [路由器的延迟加载](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck68d3221025468d30a95982e)
           * 快照对象
           * ActivatedRoute对象
   * 6 服务和依赖注入
       * [服务---组件只需要展示数据就可以了，获取和处理数据的工作应该让服务来完成](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckc7e326d0257c7e1249ff682)
       * [依赖注入---Angular通过依赖注入更容易将Web应用程序逻辑分解为服务，并使这些服务可用于各个组件中 ](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck2a3327002582a38a4a932bf)
         * 通过注入Injector类对象实例获取依赖
           * [注入器--Angular在启动过程中会自动为每个模块创建一个注入器，注入器是一个树结构](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck2a3327002582a38a4a932bf)
             * 根注入器---根注入器会提供依赖的一个单例对象，可以把这个单例对象注入多个组件中
             * 模块级别的注入器---模块和组件级别的注入器可以为它们的组件及其子组件提供同一个依赖的不同实例
             * 组件级别的注入器---模块和组件级别的注入器可以为它们的组件及其子组件提供同一个依赖的不同实例,组件可以从它自己的注入器中获取服务、从其祖先组件的注入器中获取服务、从其父模块（NgModule类）级别的注入器中获取服务，或从根注入器中获取服务
             * [不同级别的注入器创建的依赖服务有不同的作用域---表示该服务在Web应用程序中的可见性。不同级别的注入器创建的依赖服务对应着Web应用程序中的不同可见性](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck861322a025a8613985ec87a)
               * root ---表示选择的是根注入器，根注入器在整个Web应用程序中仅创建服务的一个单例对象，可以把这个单例对象注入任何想要它的类中
               * platform---
               * any---是模块注入器，这意味着同一服务可能有多个实例
             * [配置提供商---在Angular中有3个地方可以配置提供商,以便在Web应用程序的不同层级使用提供商来配置注入器](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck5423294025b54229abfc040)
               * Angular中有3个地方可以配置提供商
                 * 在服务本身的@Injectable()装饰器中
                 * 在模块类的@NgModule()装饰器中
                 * 在组件类的@Component()装饰器中
               * Angular中有6种类型的提供商
                 * TypeProvider
                 * ValueProvider
                 * ClassProvider
                 * ConstructorProvider
                 * ExistingProvider
                 * FactoryProvider   
         * [直接使用Injector类创建依赖](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck98d321b025d98dce83da05a)
   * 7 RxJS响应式编程基础
   * [8 表单---用户通过表单与服务进行交互, Angular表单从数据结构上分为视图层与模型层,在视图层，Angular表单处理用户与表单的交互；在模型层，Angular表单创建了专门的容器对象负责跟踪、处理和存储表单数据](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck65b326f026965b9eea6e6e1)
     * 模板驱动表单
       * [模板驱动表单指令](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8c)
         * NgForm
         * NgModel
         * NgModelGroup 
     * 响应式表单
       * [响应式表单指令](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck5f9323e026e5f93f9835418)
         * FormControlDirective
         * FormGroupDirective
         * FormControlName
         * FormGroupName
         * FormArrayName
     * [表单模型](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckf09320f026af0935e4cd23d)
       * AbstractControl
       * FormControl
       * FormGroup
       * FormArray 
     * [表单指令---指令被视为视图层与模型层（AbstractControl类的子类：FormControl类、FormArray类和FormGroup类）之间连接的桥梁](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka973204026ba97da629bd12)
       * [ControlValueAccessor类(视图层)---表单数据访问器,用于在Angular的FormControl类和原生DOM元素之间创建一个桥梁](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka3c320b026ca3c65c297000)
         * Angular的内置表单数据访问器有7种 
           * CheckboxControlValueAccessor
           * DefaultValueAccessor
           * NumberValueAccessor
           * RadioControlValueAccessor
           * RangeValueAccessor
           * SelectControlValueAccessor
           * SelectMultipleControlValueAccessor 
       * AbstractControlDirective类（中间层 ）
       * AbstractControl类（模型层） 
     * [表单验证](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck7f632b502707f6ffaa6bf2e)
       * 自定义验证器
       * 内置的常用验证器
         * required
         * pattern
         * email
         * min
         * max
         * minLength
         * maxLength
       * 表单控件状态的CSS样式类    
       * [使用ngSubmit事件提交表单](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck7323297027173278a4a8f1d)
   * [9 HttpClient模块](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckeb132680275eb160de1d35c)
     * [创建RESTful API服务](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckda432420278da4fb5c6e9ad)
       * 方法一：使用json-server模拟RESTful API服务
       * 方法二：使用Angular内存数据库模拟服务器 （in-memory-web-api）
     * HTTP
       * HTTP请求方法
         * 从服务器获取数据的请求
           * [GET---它是幂等（Idempotent）的，意思是发出多个相同的GET请求与发出单个GET请求具有相同的效果](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck4c5327a02794c56ff4ce24c)
             * [HttpClient模块的请求头配置 ](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka0a32dd027aa0a080f42962)
               * 添加请求头
               * 修改请求头
               * 配置请求参数 
               * [跨域访问控制](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka0a32dd027aa0a080f42962) 
                 * 跨域资源共享（CORS）
                 * 请求JSON数据---当服务器不支持跨域资源共享协议(CORS）时，JSONP是目前应用最为广泛的技术解决方案之一
                 * 请求非JSON数据 
         * 修改型的请求
           * [POST---它不是幂等的，意思是多次调用相同的POST请求与调用一次的效果不同](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckc8f3245027cc8ffe9a588b8)
           * [PUT---它是幂等的，意思是多次调用相同的PUT请求与调用一次的效果相同](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckc8f3245027cc8ffe9a588b8)
           * PATCH
           * [DELETE ---它不是幂等的，意思是多次调用相同的DELETE请求与调用一次的效果不同](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ckc8f3245027cc8ffe9a588b8)
       * HTTP响应
         * [读取完整的响应信息](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8cka0a32dd027aa0a080f42962)
         * [ HttpClient模块与RxJS配合](https://weread.qq.com/web/reader/7f332f2072462dd67f32c8ck2023270027b202cb962a56f)
           * 错误处理
           * 重试 
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

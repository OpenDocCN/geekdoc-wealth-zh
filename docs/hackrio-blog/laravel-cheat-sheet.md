# Laravel 备忘单:下载 PDF 快速参考[指南]

> 原文：<https://hackr.io/blog/laravel-cheat-sheet>

想用 PHP 开发一个响应式网站？Laravel 是最好的选择，因为它是全球使用最广泛的 PHP web 框架之一。

这篇 Laravel 备忘单探究了开发 web 应用程序所需的所有必要概念。对新手和专业人士都有帮助。

在阅读备忘单之前，我们将首先向您简要介绍 Laravel 到底是什么以及它的优点。

## 什么是 Laravel？

Laravel 是一个 PHP web 框架，为开发高质量的 web 应用程序提供了一整套有用的工具和资源。它遵循模型-视图-控制器(MVC)架构设计模式。

Laravel 框架由 Taylor Otwell 创建，并获得了 MIT 的许可。

它包含了内置特性和各种兼容的包和扩展，使它成为最流行的 PHP web 框架之一。

## Laravel 的优势

以下是使用 Laravel 框架的一些主要优势。

*   Laravel 框架易于使用，简单快捷。由于它是使用最广泛的 PHP 框架之一，许多有经验的开发人员都熟悉它，并且可能开发过交互式 web 应用程序。

*   它提供了先进的安全功能，使开发者能够保护他们的网站免受网络攻击。它使用 Bcrypt 哈希算法，这意味着它不会在数据库中保存任何密码。
*   Laravel 支持开箱即用的缓存，这大大提高了网站的性能。此外，开发人员可以毫不费力地执行其他速度优化技术，如数据库索引和内存使用减少。
*   这个框架有一个内置的网站，可以有效地处理网站的流量。所以对于流量处理也是有好处的。
*   使用 Laravel，开发人员可以构建成熟的、响应迅速的电子商务网站或 B2B 网站。
*   Laravel 有干净的 API，让你的网站和第三方应用集成起来更容易。

## Laravel 备忘单

### 拉勒维尔的路线

```
Route::get('func', function(){});
Route::get('func', 'ControllerName@function');
Route::controller('func', 'argController');
```

RESTful 控制器

```
Route::resource('posts','PostsController');
```

指定要在路线上处理的动作子集

```
Route::resource('user', 'UserController',['only' => ['index', 'show']]);
Route::resource('project', 'ProjectController',['except' => ['update', 'destroy']]);
```

触发错误

```
App::abort(404);
$handler->missing(...) in ErrorServiceProvider::boot();
throw new NotFoundHttpException;
```

路线参数

```
Route::get('func/', function($arg){});
Route::get('func/', function($arg = 'arg'){});
```

HTTP 动词

```
Route::any('func', function(){});
Route::post('func', function(){});
Route::put('func', function(){});
Route::patch('func', function(){});
Route::delete('func', function(){});
```

平静的行动

```
Route::resource('func', 'FuncController');
```

为多个动词注册路由

```
Route::match(['get', 'post'], '/', function(){});
```

安全路线(TBD)

```
Route::get('func', array('https', function(){}));
```

路线约束

```
Route::get('func/', function($arg){})
->where('arg', '[0-9]+');
Route::get('func//', function($arg, $arg2){})
->where(array('arg' => '[0-9]+', 'arg2' => '[A-Za-z]'))
```

设置要跨路线使用的模式

```
Route::pattern('arg', '[0-9]+')
```

### HTTP 中间件

将中间件分配给路由

```
Route::get('admin/profile', ['middleware' => 'auth', function(){}]);
```

命名路线

```
Route::currentRouteName();
Route::get('func/arg', array('as' => 'args', function(){}));
Route::get('user/profile', [
 'as' => 'profile', 'uses' => 'UserController@showProfile'
]);
$url = route('profile');
$redirect = redirect()->route('profile');
```

路由前缀

```
Route::group(['prefix' => 'admin'], function()
{
 Route::get('users', function(){
 return 'Matches The "/admin/users" URL';
 });
});
```

路线名称间距

此路由组将带有命名空间“arg1\arg2”

```
Route::group(array('namespace' => 'arg1\arg2'), function(){})
```

子域路由

将被传递到闭包

```
Route::group(array('domain' => '.example.com'), function(){});
```

### 行列

消息队列

```
$ Queue::push('SendMail', array('message' => $message));
$ Queue::push('SendEmail@send', array('message' => $message));
$ Queue::push(function($job) use $id {});
```

处理队列的前端作业

```
$ php artisan queue:work
```

开始队列的监听操作

```
$ php artisan queue:listen
$ php artisan queue:listen connection
$ php artisan queue:listen --timeout=20
```

获取失败的作业

```
$ php artisan queue:failed
```

刷新失败的作业

```
$ php artisan queue:flush
```

通过指定 ID 刷新失败的作业

```
$ php artisan queue:forget [id]
```

向多个接收器发送相同的有效载荷

```
$ Queue::bulk(array('SendEmail', 'NotifyUser'), $payload);
```

将工作进程作为守护进程启动

```
$ php artisan queue:work --daemon
```

## Laravel 重定向

将响应重定向到以前的位置

```
return Redirect::to('arg1/arg2');
return Redirect::to('arg1/arg2')->with('key', 'value');
return Redirect::to('arg1/arg2')->withInput(Input::get());
return Redirect::to('arg1/arg2')->withInput(Input::except('password'));
return Redirect::to('arg1/arg2')->withErrors($validator);
```

已命名路由的重定向响应

```
return Redirect::back();
```

重定向对控制器操作的响应

```
return Redirect::route('arg');
return Redirect::route('arg', array('value'));
return Redirect::route('arg', array('key' => 'value'));
```

默认路由，如果未定义指定的路由

```
return Redirect::action('ArgController@index');
return Redirect::action('ArgController@arg2', array('value'));
return Redirect::action('ArgController@arg2', array('key' => 'value'));​
```

```
return Redirect::intended('arg1/arg2');
```

拉勒韦尔高速缓存

### 旅行邮件

```
Cache::put('key', 'value', $minutes);
Cache::add('key', 'value', $minutes);
Cache::forever('key', 'value');
Cache::remember('key', $minutes, function(){ return 'value' });
Cache::rememberForever('key', function(){ return 'value' });
Cache::forget('key');
Cache::has('key');
Cache::get('key');
Cache::get('key', 'default');
Cache::get('key', function(){ return 'default'; });
Cache::tags('my-tag')->put('key','value', $minutes);
Cache::tags('my-tag')->has('key');
Cache::tags('my-tag')->get('key');
Cache::tags('my-tag')->forget('key');
Cache::tags('my-tag')->flush();
Cache::increment('key');
Cache::increment('key', $amount);
Cache::decrement('key');
Cache::decrement('key', $amount);
Cache::section('group')->put('key', $value);
Cache::section('group')->get('key');
Cache::section('group')->flush();
```

### 把所有的邮件都写到日志里，而不是发送出去

```
Mail::send('email.view', $data, function($message){});
Mail::send(array('html.view', 'text.view'), $data, $callback);
Mail::queue('email.view', $data, function($message){});
Mail::queueOn('queue-name', 'email.view', $data, $callback);
Mail::later(5, 'email.view', $data, function($message){});
```

拉勒韦尔反应

```
Mail::pretend();
```

### 创建响应并修改标题值

```
return Response::make($contents);
return Response::make($contents, 200);
return Response::json(array('key' => 'value'));
return Response::json(array('key' => 'value'))
->setCallback(Input::get('callback'));
return Response::download($filepath);
return Response::download($filepath, $filename, $headers);
```

将 cookie 附加到响应中

```
$response = Response::make($contents, 200);
$response->header('Content-Type', 'application/json');
return $response;
```

拉勒韦尔日志

```
return Response::make($content)
->withCookie(Cookie::make('key', 'value'));
```

### 记录器提供了 RFC 5424 中定义的七个日志记录级别:调试、信息、通知、警告、错误、严重和警报。

获取独白实例

```
Log::info('info');
Log::info('info',array('context'=>'additional info'));
Log::error('error');
Log::warning('warning');
```

添加监听程序

```
Log::getMonolog();
```

Laravel 输入

```
Log::listen(function($level, $message, $context) {});
```

### 如果缺少密钥，则为默认值

```
Input::get('key');
```

获取输入时仅检索“arg”和“arg1”

```
Input::get('key', 'default');
Input::has('key');
Input::all();
```

获取输入时丢弃“arg”

```
Input::only('arg', 'arg1');
```

拉勒韦尔环境

```
Input::except('arg');
Input::flush();
```

### 环境是地方性的

```
$environment = app()->environment();
$environment = App::environment();
$environment = $app->environment();
```

环境可以是本地的，也可以是暂存的…

```
if ($app->environment('local')){}
```

拉威尔刀片式服务器

```
if ($app->environment('local', 'staging')){}
```

### 在模板中显示节

开始一节

```
@yield('name')
@extends('layout.name')
```

结束一节

```
@section('name')
```

结束一节并让步

```
@stop
```

forelse 4.2 功能

```
@section('sidearg1')
@show
@parent
@include('view.name')
@include('view.name', array('key' => 'value'));
@lang('messages.name')
@choice('messages.name', 1);
@if
@else
@elseif
@endif
@unless
@endunless
@for
@endfor
@foreach
@endforeach
@while
@endwhile
```

打印内容

```
@forelse($users as $user)
@empty
@endforelse
```

打印转义内容

```
{{ $var }}
```

打印非转义内容；5.0 功能

```
{{{ $var }}}
```

检查数据是否存在后打印数据

```
{!! $var !!}
{{-- Blade Comment --}}
```

用花括号显示原始文本

```
{{{ $name or 'Default' }}}
```

Laravel URL

```
@{{ This will not be processed by Blade }}
```

### 需要不适当的名称空间

```
URL::full();
URL::current();
URL::previous();
URL::to('arg/arg1', $parameters, $secure);
URL::action('UserController@item', ['id'=>123]);
```

Laravel HTML

```
URL::action('Auth\AuthController@logout');
URL::action('argController@method', $parameters, $absolute);
URL::route('arg', $parameters, $absolute);
URL::secure('arg1/arg2', $parameters);
URL::asset('css/arg.css', $secure);
URL::secureAsset('css/arg.css');
URL::isValidUrl('http://example.com');
URL::getRequest();
URL::setRequest($request);
```

### 将 HTML 字符串转换为实体

```
HTML::macro('name', function(){});
```

将实体转换为 HTML 字符

```
HTML::entities($value);
```

生成指向 JavaScript 文件的链接

```
HTML::decode($value);
```

生成指向 CSS 文件的链接

```
HTML::script($url, $attributes);
```

生成 HTML 图像元素

```
HTML::style($url, $attributes);
```

生成 HTML 链接

```
HTML::image($url, $alt, $attributes);
```

生成 HTTPS HTML 链接

```
HTML::link($url, 'title', $attributes, $secure);
```

生成指向资产的 HTML 链接

```
HTML::secureLink($url, 'title', $attributes);
```

生成指向资产的 HTTPS HTML 链接

```
HTML::linkAsset($url, 'title', $attributes, $secure);
```

生成指向命名路由的 HTML 链接

```
HTML::linkSecureAsset($url, 'title', $attributes);
```

生成一个指向控制器动作的 HTML 链接

```
HTML::linkRoute($name, 'title', $parameters, $attributes);
```

生成指向电子邮件地址的 HTML 链接

```
HTML::linkAction($action, 'title', $parameters, $attributes);
```

混淆电子邮件地址，以防止垃圾邮件机器人嗅探它

```
HTML::mailto($email, 'title', $attributes);
```

生成有序的项目列表

```
HTML::email($email);
```

生成一个无序的项目列表

```
HTML::ol($list, $attributes);
```

创建一个列表 HTML 元素

```
HTML::ul($list, $attributes);
```

为列表元素创建 HTML

```
HTML::listing($type, $list, $attributes);
```

为嵌套列表属性创建 HTML

```
HTML::listingElement($key, $type, $value);
```

从数组构建 HTML 属性字符串

```
HTML::nestedListing($key, $type, $value);
```

构建单个属性元素

```
HTML::attributes($attributes);
```

混淆字符串以防止垃圾邮件机器人嗅探它

```
HTML::attributeElement($key, $value);
```

软删除

```
HTML::obfuscate($value);
```

### 在结果中包括软删除的模型

```
Model::withTrashed()->where('users', 2)->get();
```

强制结果集仅包含软删除

```
Model::withTrashed()->where('users', 2)->restore();
Model::where('users', 2)->forceDelete();
```

事件

```
Model::onlyTrashed()->where('users', 2)->get();
```

### 拉勒维尔加入

```
Model::creating(function($model){});
Model::created(function($model){});
Model::updating(function($model){});
Model::updated(function($model){});
Model::saving(function($model){});
Model::saved(function($model){});
Model::deleting(function($model){});
Model::deleted(function($model){});
Model::observe(new argObserver);
```

### Join 语句

左连接语句

```
DB::table('users')
         ->join('contacts', 'users.id', '=', 'contacts.user_id')
         ->join('orders', 'users.id', '=', 'orders.user_id')
         ->select('users.id', 'contacts.phone', 'orders.price')
         ->get();
```

拉勒韦尔骨料

```
DB::table('users')
     ->leftJoin('posts', 'users.id', '=', 'posts.user_id')
     ->get();

select * from users where name = 'Name' or (points > 200 
and title <> 'Admin')
```

```
DB::table('users')
         ->where('name', '=', 'John')
         ->orWhere(function($query)
         {
             $query->where('votes', '>', 100)
                   ->where('title', '<>', 'Admin');
         })
         ->get();
```

### Laravel 原始表达式

```
$users = DB::table('game')->count();
$price = DB::table('game')->max('points');
$price = DB::table('game')->min('points');
$price = DB::table('game')->avg('points');
$total = DB::table('game')->sum('points');
```

### 返回行

```
DB::table('name')->remember(5)->get();
DB::table('name')->remember(5, 'cache-key-name')->get();
DB::table('name')->cacheTags('my-key')->remember(5)->get();
DB::table('name')->cacheTags(array('my-first-key','my-second-key'))->remember(5)->
```

```
$users = DB::table('users')
                  ->select(DB::raw('count(*) as user_count, status'))
                  ->where('status', '<>', 1)
                  ->groupBy('status')
                  ->get();
```

返回受影响的行

```
DB::select('SELECT * FROM users WHERE id = ?', array('value'));
```

返回无效

```
DB::insert('insert into arg set arg1=2');
DB::update('update arg set arg1=2');
DB::delete('delete from arg1');
```

语句中的原始表达式

```
DB::statement('update arg set arg1=2');
```

Laravel 插入/更新/删除/联合/悲观锁定

```
DB::table('name')->select(DB::raw('count(*) as count, column2'))->get();
```

### 插入

更新

```
DB::table('users')->insert(
 ['email' => 'email@host.com', 'votes' => 0]
);
$id = DB::table('users')->insertGetId(
 ['email' => 'email@host.com', 'votes' => 0]
);
DB::table('users')->insert([
 ['email' => 'email@host.com', 'votes' => 0],
 ['email' => 'email@host.com', 'votes' => 0]
]);
```

删除

```
DB::table('users')
         ->where('id', 1)
         ->update(['votes' => 1]);
DB::table('users')->increment('votes');
DB::table('users')->increment('votes', 5);
DB::table('users')->decrement('votes');
DB::table('users')->decrement('votes', 5);
DB::table('users')->increment('votes', 1, ['name' => 'Name']);
```

联盟

```
DB::table('users')->where('votes', '<', 100)->delete();
DB::table('users')->delete();
DB::table('users')->truncate();
```

悲观锁定

```
$first = DB::table('users')->whereNull('first_name');
$users = DB::table('users')->whereNull('last_name')->union($first)->get();
```

Laravel 验证

```
DB::table('users')->where('votes', '>', 100)->sharedLock()->get();
DB::table('users')->where('votes', '>', 100)->lockForUpdate()->get();
```

### 拉勒维尔规则

```
Validator::make(
   array('key' => 'arg'),
   array('key' => 'required|in:arg')
);
Validator::extend('arg', function($attribute, $value, $params){});
Validator::extend('arg', 'argValidator@validate');
Validator::resolver(function($translator, $data, $rules, $msgs)
{
   return new argValidator($translator, $data, $rules, $msgs);
});
```

Laravel 配置

```
accepted
active_url
after:YYYY-MM-DD
before:YYYY-MM-DD
alpha
alpha_dash
alpha_num
array
between:1,10
confirmed
date
date_format:YYYY-MM-DD
different:fieldname
digits:value
digits_between:min,max
boolean
email
exists:table,column
image
in:arg,arg1,...
not_in:arg,arg1,...
integer
numeric
ip
max:value
min:value
mimes:jpeg,png
regex:[0-9]
required
required_if:field,value
required_with:arg,arg1,...
required_with_all:arg,arg1,...
required_without:arg,arg1,...
required_without_all:arg,arg1,...
same:field
size:value
timezone
unique:table,column,except,idColumn
Url
```

### 使用默认值获取

```
Config::get('app.timezone');
```

设置配置

```
Config::get('app.timezone', 'UTC');
```

Laravel DB 备忘单

```
Config::set('database.default', 'sqlite');
```

### 基本数据库使用

运行选择查询

```
DB::connection('connection_name');
```

运行一般语句

```
$results = DB::select('select * from users where id = ?', [1]);
$results = DB::select('select * from users where id = :id', ['id' => 1]);
```

监听查询事件

```
DB::statement('drop table users');
```

数据库事务

```
DB::listen(function($sql, $bindings, $time){ code_here; });
```

Laravel 作曲命令

```
DB::transaction(function()
{
DB::table('users')->update(['votes' => 1]);
DB::table('posts')->delete();
});
DB::beginTransaction();
DB::rollback();
DB::commit();
```

### Laravel 消息

```
composer create-project laravel/laravel folder_name
composer install
composer update
composer dump-autoload [--optimize]
composer self-update
composer require [options] [--] [vender/packages]...
```

### 这些可以用在传入的$message 实例上

这使用内存中的数据作为附件

```
Mail::send() or Mail::queue()
$message->from('email@xyz.com', 'Name');
$message->sender('email@xyz.com', 'Name');
$message->returnPath('email@xyz.com');
$message->to('email@xyz.com', 'Name');
$message->cc('email@xyz.com', 'Name');
$message->bcc('email@xyz.com', 'Name');
$message->replyTo('email@xyz.com', 'Name');
$message->subject('Congratulations');
$message->priority(2);
$message->attach('arg\arg1.txt', $options);
```

在消息中嵌入文件并获取 CID

```
$message->attachData('arg1', 'Data Name', $options);
```

获取基础 Swift 报文实例

```
$message->embed('arg\arg1.txt');
$message->embedData('arg', 'Data Name', $options);
```

Laravel 请求

```
$message->getSwiftMessage();
```

### 返回用户的 IP

```
url: http://a.com/b/c
```

```
Request::url();
```

```
path: /a/b
```

```
Request::path();
```

```
getRequestUri: /a/b/?c=d
```

```
Request::getRequestUri();
```

获取请求的端口方案(如 80、443 等。)

```
Request::getClientIp();
```

```
getUri: http://xyz.com/a/b/?c=d
```

```
Request::getUri();
```

```
getQueryString: c=d
```

```
Request::getQueryString();
```

确定当前请求 URI 是否与模式匹配

```
Request::getPort();
```

从 URI 中获取一个片段(基于 1 的索引)

```
Request::is('arg/*');
```

从请求中检索标头

```
Request::segment(1);
```

从请求中检索服务器变量

```
Request::header('Content-Type');
```

确定请求是否是 AJAX 调用的结果

```
Request::server('PATH_INFO');
```

确定该请求是否针对 HTTPS

```
Request::ajax();
```

获取请求方法

```
Request::secure();
```

检查请求方法是否属于指定的类型

```
Request::method();
```

获取原始发布数据

```
Request::isMethod('post');
```

获取请求的响应格式

```
Request::instance()->getContent();
```

如果 HTTP 内容类型标头包含*/json，则为 true

```
Request::format();
```

如果 HTTP Accept 头是 application/json，则为 true

```
Request::isJson();
```

Laravel 认证

```
Request::wantsJson();
```

### Laravel 认证

确定当前用户是否经过身份验证

获取当前已验证的用户

```
Auth::check();
```

获取当前通过身份验证的用户的 ID

```
Auth::user();
```

尝试使用给定的凭据验证用户

```
Auth::id();
```

通过将 true 传递给 Auth::attempt()来实现“记住我”

```
Auth::attempt(array('email' => $email, 'password' => $password));
```

为单个请求登录

```
Auth::attempt($credentials, true);
```

让用户登录应用程序

```
Auth::once($credentials);
```

将给定的用户 ID 登录到应用程序中

```
Auth::login(User::find(1));
```

将用户从应用程序中注销

```
Auth::loginUsingId(1);
```

验证用户的凭据

```
Auth::logout();
```

尝试使用 HTTP 基本验证进行验证

```
Auth::basic('username');
```

执行无状态 HTTP 基本登录尝试

```
Auth::validate($credentials);
```

向用户发送密码提醒

```
Auth::onceBasic();
```

Laravel 授权

```
Password::remind($credentials, function($message, $user){});
```

定义能力

传递多个参数

```
Gate::define('update-post', 'Class@method');
Gate::define('update-post', function ($user, $post) {...});
```

检查能力

```
Gate::define('delete-comment', function ($user, $post, $comment) {});
```

指定了要检查的用户

```
Gate::denies('update-post', $post);
Gate::allows('update-post', $post);
Gate::check('update-post', $post);
```

通过用户模型，使用可授权特征

```
Gate::forUser($user)->allows('update-post', $post);
```

拦截授权检查

```
User::find(1)->can('update-post', $post);
User::find(1)->cannot('update-post', $post);
```

检入刀片模板

```
Gate::before(function ($user, $ability) {});
Gate::after(function ($user, $ability) {});
```

生成策略

```
@can('update-post', $post)
@endcan
// with else@can('update-post', $post)
@else
@endcan
```

“策略”助手功能

```
php artisan make:policy PostPolicy
```

控制器授权

```
policy($post)->update($user, $post)
```

对于$用户

```
$this->authorize('update', $post);
```

自动神奇分页

```
$this->authorizeForUser($user, 'update', $post);
```

仅“下一个”和“上一个”

```
Model::paginate(15);
Model::where('cars', 2)->paginate(15);
```

手动分页器

```
Model::where('cars', 2)->simplePaginate(15);
```

打印视图中的页面导航器

```
Paginator::make($items, $totalItems, $perPage);
```

面向初学者的 PHP 与 Laravel——成为 Laravel 大师

```
$variable->links();
```

结论

## 以上总结了在开始使用 Laravel 开发应用程序之前，您应该了解的所有必要的 Laravel 概念。

Laravel 框架通过提供快速路由引擎、直观的数据库 ORM、实时事件广播、健壮的依赖注入容器和数据库 agnistic 模式迁移器，能够简化任何 web 项目中涉及的多项任务。它是一个理想的框架，提供了开发大型 web 应用程序所需的健壮工具。

**人也在读:**

**People are also reading:**
# Think-Blade
Blade template engine with thinkphp 5. (component & slot support)

# Installation
```
composer require evan-li/think-blade
```

### 配置
template.php:
```php
return [

    // 模板引擎类型 支持 php think 支持扩展
    'type'         => 'Blade',
    // 视图基础目录（集中式）
    'view_base'   => '',
    // 是否开启模板编译缓存,设为false则每次都会重新编译
    'tpl_cache'          => true,
    // 模板起始路径
    'view_path'   => '',
    'tpl_begin'   => '{{',
    'tpl_end'   => '}}',
    'tpl_raw_begin'   => '{!!',
    'tpl_raw_end'   => '!!}',
    'view_cache_path'   =>  Env::get('runtime_path') . 'temp' . DIRECTORY_SEPARATOR, // 模板缓存目录
    // 模板文件后缀
    'view_suffix' => 'blade.php',

];
```

# Usage
```html
<header id="navbar">
	<div class="row navbar-inner">
		<div class="col-xs-6 brand-block">
			<h4><a href="{{ url('/admin') }}"><img src="/assets/admin/images/logo.png"></a> · 管理后台
			</h4>
			<a href="javascript:;" class="cd_nav_trigger"><span></span></a>
		</div>
		<div class="col-xs-6 text-right user-block">
			你好，{{ $manage_user->nickname }}({{ $manage_user->username }})
			<span class="gap-line"></span>
			<a href="{{ url('/manage/index/account') }}" class="item">修改资料</a>
			<span class="gap-line"></span>
			<a href="{{ url('/manage/start/logout') }}" class="confirm item" title="确认要退出吗？">退出</a>
		</div>
	</div>
</header>
```

# DOC

https://laravel.com/docs/5.4/blade

http://d.laravel-china.org/docs/5.4/blade (中文)

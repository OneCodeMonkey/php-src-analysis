# PHP7

## 二.源码结构(v7.4)

```c
TSRM:
  |——TSRM.c
  |——TSRM.h
  |——config.w32
  |——threads.m4
  |——tsrm.m4
  |——tsrm_win32.c
  |——tsrm_win32.h
  
Zend:
  |——tests:
  |——Makefile.frag
  |——Zend.m4
  |——bench.php
  |——micro_bench.php
  |——zend.c
  |——zend.h
  |——zend_API.c
  |——zend_API.h
  |——zend_alloc.c
  |——zend_alloc.h
  |——zend_alloc_sizes.h
  |——zend_arena.h
  |——zend_ast.c
  |——zend_ast.h
  |——zend_bitset.h
  |——zend_build.h
  |——zend_builtin_functions.c
  |——zend_builtin_functions.h
  |——zend_closures.c
  |——zend_closures.h
  |——zend_compile.c
  |——zend_compile.h
  |——zend_config.w32.h
  |——zend_constants.c
  |——zend_constants.h
  |——zend_cpuinfo.c
  |——zend_cpuinfo.h
  |——zend_default_classes.c
  |——zend_dtrace.c
  |——zend_dtrace.d
  |——zend_dtrace.h
  |——zend_errors.h
  |——zend_exceptions.c
  |——zend_exceptions.h
  |——zend_execute.c
  |——zend_execute.h
  |——zend_execute_API.c
  |——zend_extensions.c
  |——zend_extensions.h
  |——zend_float.c
  |——zend_float.h
  |——zend_gc.c
  |——zend_gc.h
  |——zend_generators.c
  |——zend_generators.h
  |——zend_globals.h
  |——zend_globals_macros.h
  |——zend_hash.c
  |——zend_hash.h
  |——zend_highlight.c
  |——zend_highlight.h
  |——zend_inheritance.c
  |——zend_inheritance.h
  |——zend_ini.c
  |——zend_ini.h
  |——zend_ini_parser.y
  |——zend_ini_scanner.h
  |——zend_ini_scanner.l
  |——zend_interfaces.c
  |——zend_interfaces.h
  |——zend_istdiostream.h
  |——zend_iterators.c
  |——zend_iterators.h
  |——zend_language_parser.y
  |——zend_language_scanner.h
  |——zend_language_scanner.l
  |——zend_list.c
  |——zend_list.h
  |——zend_llist.c
  |——zend_llist.h
  |——zend_long.h
  |——zend_map_ptr.h
  |——zend_modules.h
  |——zend_multibyte.c
  |——zend_multibyte.h
  |——zend_multiply.h
  |——zend_object_handles.c
  |——zend_object_handles.h
  |——zend_objects.c
  |——zend_objects.h
  |——zend_objects_API.c
  |——zend_objects_API.h
  |——zend_opcode.c
  |——zend_operators.c
  |——zend_operators.h
  |——zend_portability.c
  |——zend_ptr_stack.c
  |——zend_ptr_stack.h
  |——zend_range_check.h
  |——zend_signal.c
  |——zend_signal.h
  |——zend_smart_str.c
  |——zend_smart_str.h
  |——zend_smart_str_public.h
  |——zend_smart_string.h
  |——zend_smart_string_public.h
  |——zend_sort.c
  |——zend_sort.h
  |——zend_stack.c
  |——zend_stack.h
  |——zend_stream.c
  |——zend_stream.h
  |——zend_string.c
  |——zend_string.h
  |——zend_strtod.c
  |——zend_strtod.h
  |——zend_strtod_int.h
  |——zend_ts_hash.c
  |——zend_ts_hash.h
  |——zend_type_info.h
  |——zend_types.h
  |——zend_variables.c
  |——zend_variables.h
  |——zend_virtual_cwd.c
  |——zend_virtual_cwd.h
  |——zend_vm.h
  |——zend_vm_def.h
  |——zend_vm_execute.h
  |——zend_vm_execute.skl
  |——zend_vm_gen.php
  |——zend_vm_handlers.h
  |——zend_vm_opcodes.c
  |——zend_vm_opcodes.h
  |——zend_vm_trace_handlers.h
  |——zend_vm_trace_map.h
  |——zend_weakrefs.c
  |——zend_weakrefs.h
build:
  |——Makefile.gcov
  |——Makefile.global
  |——ax_check_compile_flag.m4
  |——ax_func_which_gethostbyname_r.m4
  |——ax_gcc_func_attribute.m4
  |——config-stubs
  |——config.guess
  |——config.sub
  |——genif.sh
  |——libtool.m4
  |——ltmain.sh
  |——order_by_dep.awk
  |——php.m4
  |——php_cxx_compile_stdcxx.m4
  |——pkg.m4
  |——print_include.awk
  |——shtool
docs:
  |——input-filter.md
  |——mailinglist-rules.md
  |——output-api.md
  |——parameter-parsing-api.md
  |——release-process.md
  |——self-contained-extensions.md
  |——streams.md
  |——unix-build-system.md
ext:
  |——(too many, not list at this time。。。)
main:
  |——streams：
  	|——cast.c
  	|——filter.c
  	|——glob_wrapper.c
  	|——memory.c
  	|——mmap.c
  	|——php_stream_context.h
  	|——php_stream_filter_api.h
  	|——php_stream_glob_wrapper.h
  	|——php_stream_mmap.h
  	|——php_stream_plain_wrapper.h
  	|——php_stream_transport.h
  	|——php_stream_userspace.h
  	|——php_streams_int.h
  	|——plain_wrapper.c
  	|——streams.c
  	|——transports.c
  	|——userspace.c
  	|——xp_socket.c
  |——SAPI.c
  |——SAPI.h
  |——alloca.c
  |——build-defs.h.in
  |——explicit_bzero.c
  |——fastcgi.c
  |——fastcgi.h
  |——fopen_wrappers.c
  |——fopen_wrappers.h
  |——getopt.c
  |——http_status_codes.h
  |——internal_functions.c.in
  |——internal_functions_win32.c
  |——main.c
  |——mergesort.c
  |——network.c
  |——output.c
  |——php.h
  |——php_compat.h
  |——php_content_types.c
  |——php_content_types.h
  |——php_getopt.h
  |——php_globals.h
  |——php_ini.c
  |——php_ini.h
  |——php_main.h
  |——php_memory_streams.h
  |——php-network.h
  |——php_open_temporary_file.c
  |——php_open_temporary_file.h
  |——php_output.c
  |——php_reentrancy.h
  |——php_scandir.c
  |——php_scandir.h
  |——php_stdint.h
  |——php_streams.h
  |——php_syslog.c
  |——php_syslog.h
  |——php_ticks.c
  |——php_ticks.h
  |——php_variables.c
  |——php_variables.h
  |——php_version.h
  |——reentrancy.c
  |——rfc1867.c
  |——rfc1867.h
  |——snprintf.c
  |——snprintf.h
  |——spprintf.c
  |——spprintf.h
  |——strlcat.c
  |——strlcpy.c
pear:
  |——Makefile.frag
  |——fetch.php
  |——install-pear.txt
sapi:
  |——apache2handler:
    |——
  |——cgi:
    |——tests:
	|——Makefile.frag
	|——cgi_main.c
	|——config.w32
	|——config9.m4
	|——php-cgi.1.in
	|——php.sym
  |——cli:
    |——tests:
	|——Makefile.frag
	|——cli.h
	|——cli_win32.c
	|——config.m4
	|——config.w32
	|——generate_mime_type_map.php
	|——mime_type_map.h
	|——php.1.in
	|——php_cli.c
	|——php_cli_process_title.c
	|——php_cli_process_title.h
	|——php_cli_server.c
	|——php_cli_server.h
	|——php_http_parser.c
	|——php_http_parser.h
	|——ps_title.c
	|——ps_title.h
  |——embed:
    |——
  |——fpm:
	|——fpm:
	  |——events:
	    |——devpoll.c
	    |——devpoll.h
	    |——epoll.c
	    |——epoll.h
	    |——kqueue.c
	    |——kqueue.h
	    |——poll.c
	    |——poll.h
	    |——port.c
	    |——port.h
	    |——select.c
	    |——select.h
	  |——fpm.c
	  |——fpm.h
	  |——fpm_arrays.h
	  |——fpm_atomic.h
	  |——fpm_children.c
	  |——fpm_children.h
	  |——fpm_cleanup.c
	  |——fpm_cleanup.h
	  |——fpm_clock.c
	  |——fpm_clock.h
	  |——fpm_conf.c
	  |——fpm_conf.h
	  |——fpm_config.h
	  |——fpm_env.c
	  |——fpm_env.h
	  |——fpm_events.c
	  |——fpm_events.h
	  |——fpm_log.c
	  |——fpm_log.h
	  |——fpm_main.c
	  |——fpm_php.c
	  |——fpm_php.h
	  |——fpm_php_trace.c
	  |——fpm_php_trace.h
	  |——fpm_process_ctl.c
	  |——fpm_process_ctl.h
	  |——fpm_request.c
	  |——fpm_request.h
	  |——fpm_scoreboard.c
	  |——fpm_scoreboard.h
	  |——fpm_shm.c
	  |——fpm_shm.h
	  |——fpm_signals.c
	  |——fpm_signals.h
	  |——fpm_sockets.c
	  |——fpm_sockets.h
	  |——fpm_status.c
	  |——fpm_status.h
	  |——fpm_stdio.c
	  |——fpm_stdio.h
	  |——fpm_str.h
	  |——fpm_systemd.c
	  |——fpm_systemd.h
	  |——fpm_trace.c
	  |——fpm_trace.h
	  |——fpm_trace_mach.c
	  |——fpm_trace_pread.c
	  |——fpm_trace_ptrace.c
	  |——fpm_unix.c
	  |——fpm_unix.h
	  |——fpm_worker_pool.c
	  |——fpm_worker_pool.h
	  |——zlog.c
	  |——zlog.h
    |——tests:
	  |——
	|——Makefile.frag
	|——config.m4
	|——init.d.php-fpm.in
	|——php-fpm.8.in
	|——php-fpm.conf.in
	|——php-fpm.service.in
	|——status.html.in
	|——www.conf.in
  |——litespeed:
    |——
  |——phpdbg:
	|——
scripts:
  |——dev:
	|——
  |——man1:
	|——
  |——Makefile.frag
  |——php-config.in
  |——phpize.in
  |——phpize.m4
tests:
  |——
buildconf
configure.ac
php.ini-development
php.ini-production
run-tests.php

```



## 一.PHP7->PHP5 写法用法变更

1.脚本使用何种类型控制方式的声明：

主要有两种方式，一种是严格类型模式，一种是弱类型模式

`declare(strict_types = 1)` : 严格类型模式

`declare(strict_types = 0)` : 弱类型模式

2.`??` 和 `<=>` 运算符

`??` :  $a ?? $b  等同于以往的这种写法 —— isset($a) ? $a : $b;  (注意区分 `?:` 和 `??`)

`<=>` : $var = $a <=> $b，当 $a > $b 时，$var = 1. 当 $a = $b 时，$var = 0. 当 $a < $b 时，$var = -1.

3.define 不只能定义单值常量，也能定义数组型常量。

```php
define('a', [
    1,
    2,
    4,
    5,
]);
echo a[3];	// 5
```

5.支持定义匿名类

6.为已存在的类绑定一个匿名函数的新版写法：

```php
<?php
class A{
	private $var = 'aaaa';
    public function foo() {
        return 'bbbb';
    }
}
// 老版写法：绑定一个匿名函数
$newFunc = function() {
    echo $this->x;
    return $this->foo();
}
$bindFunc = $newFunc->bindTo(new A, 'A');
echo $bindFunc();		// 'aaaa''bbbb'

// 新版写法
echo $newFunc->call(new A);		// 'aaaa''bbbb'
```

7.新的伪随机数生成器

PHP7 引入了几个 CSPRNG 函数来提供一种简单的机制，以生成密码学上强壮的随机数。（具体差异后面再补充）

random_bytes() —— 生成伪随机字符串

random_int() —— 生成伪随机整数。

8.use 语句，可以一次引入同一个 namespace 下的多个类

`use A\{classB, classC, classD[ as E]}`

9.session函数用法变化

```php
1.session_start() 可定义数组参数
    session_start([
        'cache_limiter' => 'private',
        'read_and_close' => true,
    ]);
2.引入一个新的 php 配置 session.lazy_write，默认此配置为 true，代表只有 session 数据发生变化时才写入。
```

10.移除部分扩展：`ereg`, `mssql`, `mysql`, `sybase_ct`

## 二.Crafts:（此为零散碎片思路整理，仅供后续整理系统化提供参考。中有纰漏恳请指出）

1.为什么 php7 比 php5 性能有大幅提升？

  1）变量存储字节减少，减少内存占用，提升了变量操作速度。

  2）改善数组结构，数组元素和哈希映射表被分配在同一片内存里，降低了内存占用，提升了 cpu 缓存的命中率

  3）改善函数的调用机制，通过优化参数传递的环节，减少了一些指令执行，提高 cpu 的执行效率


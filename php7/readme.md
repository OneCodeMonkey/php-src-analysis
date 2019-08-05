# PHP7

## 一.PHP7->PHP5 写法用法变更

1.脚本使用何种类型控制方式的声明：

主要有两种方式，一种是严格类型模式，一种是弱类型模式

`declare(strict_types = 1)` : 严格类型模式

`declare(strict_types = 0)` : 弱类型模式

2.`??` 和 `<=>` 运算符

`?:` :  $a ?? $b  等同于以往的这种写法 —— isset($a) ? $a : $b;  (注意区分 `?:` 和 `??`)

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


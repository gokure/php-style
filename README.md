如果使用第三方框架，并且有提供代码样式说明，则遵循其代码样式标准，否则如下！

## 格式：

* 使用UTF-8编码

* 使用4个空格缩进，禁止使用Tab

* Unix样式换行符（LF）

* 在逗号、冒号和分号操作符使用空格

* 在 (，[ 后面、]，) 前面不使用空格

* 在代码块中使用4个空格缩进

* 采用层级缩进

* 在return方法的返回值前使用空行（除非只有一行代码）以及在两个方法中使用空行区分

* 在两个大的逻辑代码段之间使用空行区分

* 保持行字数在80字以内，最多不超过120

* 使用标准的PHP标签定界，禁止使用短标签（<? //... ?>），对于只包含有PHP代码的文
件，禁止使用PHP结束标志（"?>"），文件末尾使用注释说明"/* End of file <filename.php> */"

* 单行代码也必须使用分号（;）结束

## 命名：

* 文件名使用snake_case方式，禁止使用臃肿的文件名

* 变量名使用snake_case方式，禁止使用臃肿的变量名
  * 禁止使用单字符做为局部变量（如$i），在for循环中除外
  * 禁止使用大写字母做为全局变量，如使用大写字母，应使用SCREAMING_SNAKE_CASE方式

* 类名使用CamelCase方式，方法名使用camelCase方式（保持像HTTP，RFC，XML缩写词的大写）

* 常量名使用SCREAMING_SNAKE_CASE方式

  ```php
  <?php
  // bad
  superclass.php
  SuperClass.php
  superClass.php

  $i = "foobar";  // 单字符变量只充许使用在for循环中
  $bufferdText   // 驼峰式变量，并且意思可以再精简些
  $groupid        // 两个单词之间需要下划线分开
  $name_of_last_city_used // 太长

  MyConstant       // 应该用下划线并且字母没有全大写
  N                     // 单字符
  S_C_VER           // 意思不清楚

  class superclass
  class superClass

  function fileproperties() // 意思不清楚并且没有驼峰式命名
  function fileProperties() // 意思不清楚
  function getfileproperties() // 好些了，但没有驼峰式命名

  // good
  super_class.php

  for ($i = 0; $i < 10; $i++)
  $buffer
  $group_id
  $last_city

  MY_CONSTANT
  NEWLINE
  SUPER_CLASS_VERSION

  class SuperClass

  function getFileProperties()
  ```
## 语法：

对于嵌入HTML中的PHP代码，对于像if, for, foreach, while等代码块，采用if: ... endif; for: ... endfor; foreach: ... endforeach;以及 while: ... endwhile;方法块

  ```php
  ...
  <?php if ($user->isLoggedIn()): // checking logged in ?>
  <!-- HTML goes here. -->
  <?php endif; // end checking logged in ?>

  <?php foreach ($users as $user): // loop users ?>
  <!-- HTML goes here. -->
  <?php endforeach; // end loop users ?>
  ...
  ```

## 注释：

* 文档块必须和phpDocumentor格式兼容，请参考： [url]http://phpdoc.org/[/url]

* 避免多余的意见

  ```php
  <?php
  /**
   * 控制器类说明信息
   */
  class Controller {
      private static $instance;

      public function __construct()  {
          ...
      }

      /**
       * 函数说明信息
       */
      public static function &get_instance() {
          ...
      }

  /* End of file controller.php */
  ```

## 其他：

* 保持代码简单

* 保持一致性


## 参考：
[CodeIgniter](http://codeigniter.com/user_guide/general/styleguide.html)
[Zend Framework](http://framework.zend.com/manual/zh/coding-standard.coding-style.html)
[WordPress](http://codex.wordpress.org/WordPress_Coding_Standards)

[Javascript 代码样式参见](http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml)

[Ruby 样式参见](https://github.com/chneukirchen/styleguide/blob/master/RUBY-STYLE)

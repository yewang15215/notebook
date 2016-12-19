# PHP 学习笔记


* 遍历对象
    - 例如用 foreach 语句，默认情况下，所有**可见属性**都将被用于遍历。
* array_merge 和 array_push
    ```
    <?php
    $a = [[1, 2], [3, 4]];
    $b = [5, 6];
    $test1 = array_push($a, $b);
    $test2 = array_merge($a, $b);
    ```
    var_dump($test1);
    结果是：
    ```
    int(3)
    ```
    var_dump($test2);
    结果是：
    ```
    int(3)
    array(5) {
      [0]=>
      array(2) {
        [0]=>
        int(1)
        [1]=>
        int(2)
      }
      [1]=>
      array(2) {
        [0]=>
        int(3)
        [1]=>
        int(4)
      }
      [2]=>
      array(2) {
        [0]=>
        int(5)
        [1]=>
        int(6)
      }
      [3]=>
      int(5)
      [4]=>
      int(6)
    }
    ```

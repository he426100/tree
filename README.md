php递归无限级树形数据
====  

```PHP
include dirname(__DIR__).'/Tree.php';
$data = include __DIR__."/data.php";
//设置主键、节点名称
//Tree::setConfig($primary = '', $parentId = '', $child = '');
print_r(Tree::makeTree($data));
```
运行结果

``` PHP
Array
(
    [0] = Array
   (
      [id] = 1
       [city] = 中国
        [parent_id] = 0
        [child] = Array
         (
                 [0] = Array
                      (
                             [id] = 2
                            [city] = 北京
                             [parent_id] = 1
                             [child] = Array
                                (
                                 [0] = Array
                                         (
                                             [id] = 3
                                            [city] = 北京市
                                            [parent_id] = 2
                                            [child] = Array
                                                (
                                                   [0] = Array
                                                       (
                                                            [id] = 4
                                                            [city] = 东城区
                                                            [parent_id] = 3
                                                        )

                                                   
                                                )

                                        )

                                )

                        )

                    [1] = Array
                        (
                            [id] = 11
                            [city] = 上海
                            [parent_id] = 1
                            [child] = Array
                                (
                                    [0] = Array
                                        (
                                            [id] = 12
                                            [city] = 上海市
                                            [parent_id] = 11
                                        )


                                )

                        )

                )

        )

)
```

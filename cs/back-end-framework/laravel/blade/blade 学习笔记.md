# blade 学习笔记 


## 语法
* 注释

    `{{-- This comment will not be present in the rendered HTML --}}`

* @section 和 @yield 的区别
    > @yield 是不可扩展的，如果你要定义的部分没有**默认内容**让子模板扩展的，那么用 @yield($name, $default) 的形式会比较方便，如果你在子模板中并没有指定这个区块的内容，它就会显示默认内容，如果定义了，就会显示你定义的内容。非此即彼。
    
    > @section 则既可以被替代，又可以被扩展。

    * layout 使用 
        ```@yield```
        继承之后，使用 
        ```@section('title', 'value')```
    * layout 使用 
        ```
        @section
        value
        @show
        ```
        继承之后，使用
        ```
        @section 
        value
        @show 或者 @endsection
        ```

* @show 与 @stop 的区别
    > 通常来说，在**首次**定义某个 section 的时候，应该用 @show，而在替换它或者扩展它的时候，不应该用 @show，应该用 @stop。
    
    > @show 指的是执行到此处时将该 section 中的内容输出到页面，而 @stop 则只是进行内容解析，并且不再处理当前模板中后续对该 section 的处理，除非用 @override覆盖。

* @append 和 @override
    > @append 表明 “此处的内容添加到”，因此内容会不断扩展。如果之前使用了 @stop，@append 不会生效。
    
    > @override 的意思就是 “覆盖之前的所有定义，以这次的为准”。
    
    > 当神奇的 @parent 出现后，@append 的功能显得不是很有必要，因为完全可以使用 @parent 完成相同的功能。

* @endsection 和 @stop 的区别
    > [@endsection became @stop in L4, just as @yieldSection became @show。](http://stackoverflow.com/questions/21199412/laravel-blade-endsection-vs-stop)
    > 最新的版本里，@endsection 还是可以用的，甚至5.3版本的文档还是用 @endsection。

## 参考：
* [Blade 模板中有关 section 的那些事](https://ofcss.com/2014/12/16/blade-keywords-yield-section-show-stop-override-append.html)

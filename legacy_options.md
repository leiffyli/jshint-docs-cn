# JSHint legacy options

    说明：这些选项继承至JSLint.
    
#### * nomen

    作用：是否允许变量名以"_"开头或结尾，false -- 允许，true -- 不允许.
    
    示例：值为true时
    
        /* jshint nomen:true */
        var _a = 1;
        alert(_a); // JSHint校验结果：Unexpected dangling '_' in '_a'.
        
        /* jshint nomen:true */
        var a_ = 1;
        alert(a_); // JSHint校验结果：Unexpected dangling '_' in 'a_'.
        
        /* jshint nomen:true */
        var a_b = 1; 
        alert(a_b); // JSHint校验结果：ok
        
#### * onevar

    作用：允许每个函数中只有一个var语句（如var a,b,c;）.
    
#### * passfail

    作用：让JSHint停在第一个错误/警告处，true -- 启用，false -- 不启用.
    
    示例：启用
    
        /* jshint passfail:true */
        function show() {
            var b = 1;
            alert(a); // JSHint校验结果：Stopping. (87% scanned).
        }

#### * white

    作用：让JSHint检查你的代码是否违反道格拉斯的JS编码风格.

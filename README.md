# MliybsToolKit
Mliybs的C#扩展工具包 写了一堆逆天类和逆天扩展方法

使用dotnet add package MliybsToolKit安装此包

# 扩展方法
## 整型
为整型（非负数）扩展了GetEnumerator方法 有了该方法后整型就可以使用foreach进行遍历 具体作用相当于产生一个0到该整型的整数集合

示例代码：
```CSharp
using System;
using Mliybs.MliybsToolKit;

namespace Namespace
{
    class Program
    {
        public static void Main(string[] args)
        {
            foreach (var item in 5) Console.WriteLine(item);
        }
    }
}
```

输出结果：0 1 2 3 4 5

## 元组
为ValueTuple&lt;int begin, int end&gt;和ValueTuple&lt;int begin, int end, int step&gt;扩展了GetEnumerator方法 可以进行遍历 其中begin表示起始值 end表示结束值 step表示步长 指每隔几个值进行取值 不可为0 可为负

示例代码：
```CSharp
using System;
using Mliybs.MliybsToolKit;

namespace Namespace
{
    class Program
    {
        public static void Main(string[] args)
        {
            foreach (var item in (20, 5, -3)) Console.WriteLine(item);
        }
    }
}
```

输出结果：20 17 14 11 8 5
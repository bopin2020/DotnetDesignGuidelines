# DotnetDesignGuidelines
.NET 设计规范

> 参考    
> https://learn.microsoft.com/en-us/dotnet/standard/design-guidelines/      

> Notes https://github.com/bopin2020/DotnetDesignGuidelines/wiki    

## Special Notes
> 对于静态类 在设计框架或者编写库时, 不建议使用
> 关于静态类一节  https://github.com/bopin2020/DotnetDesignGuidelines/wiki/2.-%E7%B1%BB%E5%9E%8B%E8%AE%BE%E8%AE%A1%E8%A7%84%E8%8C%83#static-class-design      
> stackoverflow上有一节  don't use static class in c#   
> https://softwareengineering.stackexchange.com/questions/161222/dont-use-static-in-c 
> 同时据我目前个人观点, 无论是写工具还是库，项目中出现1/3及以上的静态方法 静态类，严重阻碍着面向对象思想，考虑重构。   
> 静态类唯一使用的地方是  全局性，没有上下文依赖的场景中  
> 比如生成随机字符串 可以使用；但是生成不同种类的随机字符串，很明显输入具有不同的类型，输出是根据输入而定的，形成了上下文依赖关系，那么不建议使用静态方法，同时可以方便单元测试。  

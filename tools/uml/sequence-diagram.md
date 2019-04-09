# [《MHS 学习笔记》] > [《时序图》] > 开始 (mhs2019.4.3)

- [信息]
- [类型]
- [颜色]
- [分组]

## <span id="message">信息</span>
> 1. 实例间消息传递
> 2. header/footer/title
> 3. group --- 信息自定义
> 4. ref over --- 引用
> 5. ...xxx... --- 延时
@startuml
header Header
footer Footer
title Title

participant A
participant B
A -> B: req1
group if(Async)
  group if(Login successfully)
  A <- B: rt1
  end
  group else if(Login failed)
  A <- B: rt2
  end
  group else(Error)
  A <- B: rt3
  end
end
@enduml
> 代码：
```
@startuml
participant A
participant B
A -> B: req1
group if
  group if(Login successfully)
  A <- B: rt1
  end
  group else if(Login failed)
  A <- B: rt2
  end
  group else
  A <- B: rt3
  end
end
@enduml
```

## <span id="type">类型</span>
> 使用<<和>>定义类型
@startuml
participant A <<Actor>>
participant B <<Boundary>>
participant C <<Control>>
participant D <<Entity>>
participant E <<Database>>
hide footbox
@enduml
> 代码：
```
@startuml
participant A <<Actor>>
participant B <<Boundary>>
participant C <<Control>>
participant D <<Entity>>
participant E <<Database>>
hide footbox
@enduml
```

## <span id="colour">颜色</span>
> 颜色[浅绿(#aqua)|黑(#black)|蓝(#blue)|紫红(#fuchsia)|灰(#gray)|绿(#green)|石灰(#lime)|褐红(#maroon)|海蓝(#navy)|橄榄(#olive)|紫(#purple)|红(#red)|银(#silver)|蓝绿(#teal)|白(#white)|黄(#yellow)]
@startuml
participant aqua #aqua
participant black #black
participant blue #blue
participant fuchsia #fuchsia
participant gray #gray
participant green #green
participant lime #lime
participant maroon #maroon
participant navy #navy
participant olive #olive
participant purple #purple
participant red #red
participant silver #silver
participant teal #teal
participant white #white
participant yellow #yellow
hide footbox
@enduml
> 代码：
```
@startuml
participant aqua #aqua
participant black #black
participant blue #blue
participant fuchsia #fuchsia
participant gray #gray
participant green #green
participant lime #lime
participant maroon #maroon
participant navy #navy
participant olive #olive
participant purple #purple
participant red #red
participant silver #silver
participant teal #teal
participant white #white
participant yellow #yellow
hide footbox
@enduml
```

## <span id="group">分组</span>
> 用(box|end box)添加分组|标题|背景色
@startuml
participant A #red
box "B And C" #silver
	participant B #green
  participant C #blue
end box
hide footbox
@enduml
> 代码：
```
@startuml
participant A #red
box "B And C" #silver
	participant B #green
  participant C #blue
end box
hide footbox
@enduml
```

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《时序图》]: https://mhsnet.github.io/mhsstudynotes/tools/uml/sequence-diagram.html "《时序图》"

[信息]: https://mhsnet.github.io/mhsstudynotes/tools/uml/sequence-diagram.html#message "信息"
[类型]: https://mhsnet.github.io/mhsstudynotes/tools/uml/sequence-diagram.html#type "类型"
[颜色]: https://mhsnet.github.io/mhsstudynotes/tools/uml/sequence-diagram.html#colour "颜色"
[分组]: https://mhsnet.github.io/mhsstudynotes/tools/uml/sequence-diagram.html#group "分组"

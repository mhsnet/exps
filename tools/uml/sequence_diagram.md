# 《时序图》 [Home] (更新 mhs2019.1.23)

## 1. 参与对象
1. 无 --- 普通
2. actor(角色) --- 人|系统|子系统
3. boundary(边界) --- 交互界面
4. control(控制) --- 控制
5. entity(实体) --- 永久|长期（文件等）
6. database(数据库) --- 数据库
7. collections(集合) --- 集合
```
// 对象命名（3）：
// 1. 对象 --- 长期存在
// 2. 对象:类 --- 一般
// 3. 类 --- 匿名对象
// as --- 重命名
// #red|#999999 --- 背景色
// order --- 排序
@startuml
participant x1 as "x1:X1" order 10 #999999
actor x2 as "X2"
boundary x3 as "x3:X3"
control x4 as "x4:X4"
entity x5 as "x5"
database x6 as "x6"
collections x7 as "x7"
@enduml
```

## 2. 消息
###### 1. 箭头样式（可反向）
1. -> 同步发
2. --> 同步回
3. ->> 异步发
4. -->> 异步回
5. ->o 同步发（无需回）
6. ->>o 异步发（无需回）
7. ->x 同步发（失败）
8. ->>x 同步发（失败）
```
// [#red|#999999] --- 箭头颜色
// autonumber start --- 消息编号（开始）
// newpage 'titel' --- 分割图
// note left|note right xxx end note --- 消息注释
// [...|...10s...] --- 延时
// == 分隔 == --- 分隔
// [|||or||20||] --- 空间
@startuml
autonumber 1
X1 -[#red]> X2: hello
note left 
注释信息
end note
X1 -[#999999]-> X2
autonumber 1
X1 ->> X2
X1 -->> X2
X1 ->o X2
X1 ->>o X2
...10s...
== 分隔 ==
||20||
X1 ->x X2
newpage '新页面'
X1 ->>x X2
@enduml
```

## 3. 组合消息
1. alt/else/../end --- [switch语句|if语句]
2. opt/end --- [简单if语句]
3. loop/end --- [for|forEach|while循环]
4. break/end --- [中断]
5. par/end --- [并行]
6. Critical/end --- [不交错]
7. group/end --- [自定义分组]
```
@startuml
== if语句 ==
alt if(x < 10)
a -[#red]> b: req1
else else if(x > 100) 
a -[#red]> b: req2
else else
a -[#red]> b: req3
end
== switch语句 ==
alt switch(x) case 'a':
a -[#blue]> b: req1
break break;
end
else case 'b':
a -[#blue]> b: req2
break break;
end
else default:
a -[#blue]> b: req3
end
== 简单if语句 ==
opt if(x > 0)
a -[#green]> b: req
end
== 循环 ==
group 循环for(var i = 0; i < 5; i=i+1){}
loop for(var i = 0; i < 5; i++)
a -[#DarkGreen]> b: req
end
end
group 循环for(var i in collection){}
loop for(var i in collection)
a -[#DarkGreen]> b: req
end
end
group 循环collection.forEach((x)=>{});
loop collection.forEach(x)
a -[#DarkGreen]> b: req
end
end
group 循环while(){}
loop while(x > 0)
a -[#DarkGreen]> b: req
end
end
group 循环do{}while();
loop do while(x > 0)
a -[#DarkGreen]> b: req
end
end
== 并行【不交错】 ==
par
Critical
a -[#Yellow]>> b: req1
a -[#Yellow]>> b: req2
end
a -[#Yellow]>> b: req3
end
== 自定义分组 ==
group 任务1
a -[#Gray]>> b: req1
a -[#Gray]>> b: req2
end
@enduml
```
![组合信息][UML图组合信息]

##

[UML图组合信息]: https://mhsnet.github.io/note/diagrams/out/tools_uml_sequence_diagram_composite_message.png "UML图组合信息"


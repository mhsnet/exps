# 从数据库读取 [Home] [Aqueduct] (mhs2019.2.21)

- [对象关系映射]
- [建立数据模型]
- [定义上下文]

## <span id="object-relational-mapping">对象关系映射(Object-Relational Mapping)</span> [Top]
> 关系数据库(如PostgreSQL)以table存数据，table表示某种实体，columns描述实体属性；row是实体的一个实例。

> ORM将数据库中的rows与应用程序中的objects相互转换，Class-Table，Instance-Row，Property-Column。

## <span id="building-a-data-model">建立数据模型(Building a Data Model)</span> [Top]
> 例（lib/model/users.dart）：
```
import 'package:dart_study_server/dart_study_server.dart';

class User extends ManagedObject<_User> implements _User {}

class _User {
  @primaryKey
  int id;

  @Column(unique: true)
  String name;
}
```
> 声明实体，有2个类组成：
> 1. _User是表的直接映射，表与类名相同，属性对应列；实体的表定义，除了描述数据表，不会对其它内容使用。
> 2. User(ManagedObject\<T\>子类)在代码中使用，数据库获取users是User实例；实体的实例类型。
> 3. 实例类型必须实现其表定义，实例类型必须扩展ManagedObject\<T\>，ManagedObject\<T\>具有自动将对象传输到database 和back（其他内容）的行为。

## <span id="defining-a-context">定义上下文(Defining a Context)</span> [Top]
> 应用程序需要知道2件事来执行数据库查询：
> 1. 数据模型（实体集合）？
> 2. 连接到哪个数据库？

##
[Home]: https://mhsnet.github.io/mhsstudynotes/ "《MHS技术栈学习笔记》"
[Aqueduct]: https://mhsnet.github.io/mhsstudynotes/framework/aqueduct/index.html "《Aqueduct》"
[Top]: https://mhsnet.github.io/mhsstudynotes/framework/aqueduct/tutorial/reading_from_a_database.html "从数据库读取"

[对象关系映射]: https://mhsnet.github.io/mhsstudynotes/framework/aqueduct/tutorial/reading_from_a_database.html#object-relational-mapping "对象关系映射(Object-Relational Mapping)"
[建立数据模型]: https://mhsnet.github.io/mhsstudynotes/framework/aqueduct/tutorial/reading_from_a_database.html#building-a-data-model "建立数据模型(Building a Data Model)"
[定义上下文]: https://mhsnet.github.io/mhsstudynotes/framework/aqueduct/tutorial/reading_from_a_database.html#defining-a-context "定义上下文(Defining a Context)"
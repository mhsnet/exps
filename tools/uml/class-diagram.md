# [《MHS 学习笔记》] > [《类图》] > 开始 (mhs2019.4.3)

- [类关系]

## <span id="class">类</span>
@startuml
class User {
  - name
}
@enduml

## <span id="relation">类关系</span>
> 1. <|-- --- 实现(implements)|继承(extends)
> 2. o-- --- 聚合|关联|依赖
> 3. *-- --- 组合

@startuml
interface CompanyI
class Company
abstract DepartmentA
class SaleD
class ProduceD
abstract MemberA
class SaleM
class ProduceM

CompanyI <|-- Company
DepartmentA <|-- SaleD
DepartmentA <|-- ProduceD
MemberA <|-- SaleM
MemberA <|-- ProduceM

Company "1" *-- "n" DepartmentA
DepartmentA "1" o-- "n" MemberA
@enduml

##
[《MHS 学习笔记》]: https://mhsnet.github.io/mhsstudynotes/ "《MHS 学习笔记》"
[《类图》]: https://mhsnet.github.io/mhsstudynotes/tools/uml/class-diagram.html "《类图》"

[类关系]: https://mhsnet.github.io/mhsstudynotes/tools/uml/class-diagram.html#relation "类关系"

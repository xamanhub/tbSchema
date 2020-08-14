# 表单属性和控件
## 一、属性
* `type`:控件类型
* `dataName`:数据名称
  * 在取数据时props.mds.moduleData.dataName
* `invisible`:控件不可见
  * bool类型 false为可见，true为不可见
* `label`:控件标签 
  * `description`:标签描述
    *  `icon`:图标描述
    * `desc`:文字描述
  * `title`:标签标题
* `validateProps`:控件验证规则
  * `dataType`:数据类型
  * `required`:是否必填
  *  `validate`:是否验证填写数据类型和dataType类型匹配
* `style`:控件样式
* `wrapperStyle`:控件包装样式，border、padding等
* `extension`:扩展属性(每种控件扩展属性都有区别)
## 二、input控件
```json

```

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
* `wrapperStyle`:整个控件容器的样式
* `extension`:扩展属性(每种控件扩展属性都有区别)
  * `relateData`:如需跳转其他页面地址操作  需要携带的数据  如需其他控件的数据 使用控件id.dataName
  * `dialogType`:跳转其他页面时打开方式  dialog(弹窗)
  * `sendDataType`:打开的弹窗是否展示内容  只要不为空字符串 都是true
  * `url`:打开的弹窗展示内容地址
  * `defaultValue`:默认值
  * `dataSource`:数据选择源 数组类型
  * `limitHeight`:当控件是image时 是否保持上传的图片尺寸必须和第一张相同
  * `multiple`:是否显示多行
  * 。。。。。
## 三、rules
* `conditio`:匹配规则 
* `components`:参与的组件
  * 组件id:{
  	属性:值
  }
  * 例：
```json
{
	"condition": "${moduleData.mode}==1",  
	"components": {
		"arrayConSetting": {
			"invisible": false
		},
		"otherSetting": {
			"invisible": true
		}
	},
	"desc": ""
}
```
## 三、控件
### 1、Container控件
```json
"1569315122982_1": {
	"wrapperStyle": {
		"height": "10px"
	},
	"invisible": false,
	"style": {
		"width": "auto",
		"height": "auto"
	},
	"label": {
		"description": "",
		"title": ""
	},
	"type": "Container"
}
```
### 2、Input控件
```json
"1519127662740_1": {
	"extension": {
		"useReg": false,
		"multiple": true,
		"placeholder": "请输入关键字"
	},
	"wrapperStyle": {},
	"dataName": "text_content",
	"style": {
		"width": "auto",
		"height": "auto"
	},
	"label": {
		"description": {
			"icon": "",
			"desc": ""
		},
		"title": "文本内容"
	},
	"type": "Input",
	"validateProps": {
		"max": 100.0,
		"dataType": "Text",
		"required": true,
		"validate": true
	}
}
```
### 3、InteractVideo控件
```json
"1519810282589_4": {
	"extension": {},
	"wrapperStyle": {},
	"dataName": "videoInfo",
	"style": {},
	"label": {
		"description": {
			"icon": "",
			"desc": "支持商品小卡、优惠券、红包等在视频上展现视频最小尺寸640x360，长度2分钟以内"
		},
		"title": "选择互动视频"
	},
	"type": "InteractVideo",
	"validateProps": {
		"dataType": "Map",
		"required": true,
		"validate": true
	}
}
```
### 4、Range控件
```json
"1519822104586_4": {
	"extension": {
		"dataMap": {
			"start": "startPrice",
			"end": "endPrice"
		},
		"startText": "过滤价格",
		"placeholder": "￥",
		"endText": "元"
	},
	"wrapperStyle": {},
	"dataName": "filterPrice",
	"style": {
		"width": "auto",
		"height": "auto"
	},
	"label": {
		"description": {
			"icon": "",
			"desc": ""
		},
		"title": ""
	},
	"type": "Range",
	"validateProps": {
		"dataType": "Map",
		"required": false,
		"validate": false
	}
}
```
### 5、Skip控件
```json
"1519822104586_2": {
	"extension": {
		"text": "新建分类",
		"url": "//siteadmin.tmall.com/category/index.htm"
	},
	"wrapperStyle": {
		"marginTop": "-10px"
	},
	"dataName": "skip",
	"style": {
		"width": "auto",
		"height": "auto"
	},
	"label": {
		"description": {
			"icon": "",
			"endIcon": "arrow-double-right",
			"desc": ""
		},
		"title": ""
	},
	"type": "Skip",
	"validateProps": {
		"dataType": "",
		"required": false,
		"validate": false
	}
}
```

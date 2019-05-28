#### 1.租售列表（sale/list）

##### 入参：

| 参数名 | 类型 | 必传 | 含义 | 备注 |
| --- | --- | --- | --- | --- |
| saleStyle | int | √ | 租售类型 | 1.新房 2.二手房 3.租房 |
| city | string | × | 城市 | 310000：上海市 |
| district | string | × | 区 | 310110：宝山区 |
| priceSort | int | × | 价格排序 | 1.从低到高 2.从高到低 (不传或空按照默认顺序排序) |
| areaType | string | × | 户型 | 1.一居室 2.二居室 3.三居室 4.四居室及以上 (多选，多个值以’,’号分割，如：1,2,3) |
| propertyType | string | × | 更多 | 1.平层 2.洋房 3.别墅 4.公寓 5.门面 (多选，多个值以’,’号分割，如：1,2,3) |
| searchName | string | × | 模糊搜索小区名称 |  |
| page | int | × | 页码 | 1/2/3 …    不传默认第一页 |
| limit | int | × | 每次拉取个数 | 5/10…    不传默认一页10个 |

##### 返回值示例：

``` json
{
	"code": 0,
	"message": "success",
	"data": {
		"pager": {
			"limit": 10,
			"start": 0,
			"count": 1
		},
		"list": [{
			"id": 1,
			"name": "花园洋房",
			"villageAddress": "上海市xxx区xxx路x号x",
			"villageImage": "http://ct.cn/uploads/eeb625c7e19167d73e461ffa0202640a.png",
			"saleState": 2,
			"activeDesc": "老住户98折",
			"tags": [{
				"name": "近商圈",
				"level": 2,
				"style": 1
			}, {
				"name": "开发区",
				"level": 2,
				"style": 1
			}, {
				"name": "公园旁",
				"level": 1,
				"style": 1
			}],
			"price": 110000,
			"priceUnit": "元/m²",
			"area": "100~200m²"
		}]
	}
}
```


# 用户数据文件
## 说明
- data目录下面存放的是用户的北京通数据，数据格式为[JSON](https://baike.baidu.com/item/JSON/2462549?fr=aladdin)格式，文件后缀为 **.json**
- 文件名以用户手机号/登录账号命名
- JSON数据格式校验 https://www.sojson.com/  ，拷贝文件内容到输入框中，点击“校验/格式化”即可，如果是绿色说明格式正确，反之错误需要修改

## json数据模板举例说明

**注意**：
- **信息文件必须是.json，譬如：13546887137.json**
- **不要拷贝以下内容到数据文件中，仅此查看字段说明，如果非要拷贝必须要把“//” 注释删掉，请做好json数据格式校验（见说明）**
- **公积金缴纳详细信息一定要按照opt_day从大到小(时间倒序)有序排列**

```javascript
{
	// 登录用户名
	"username":"13678335612",
	// 登录用户名
	"pwd":"123456",
	// 真实姓名
	"real_name":"张荣",
	// 性别
	"sex":"女",
	// 民族
	"ethnic_group":"汉",
	// 生日
	"birthday":"1988-06-07",
	// 社保卡号
	"card":"527039982678",
	// 身份证号
	"id_card":"3427**********2415",
	// 社保
	"social_insurance":{
		// 参保单位
		"companies":[
			"百度",
			"搜狗"
		],
		// 参保区县
		"area":"北京市朝阳区社会保险基金管理中心",
		// 缴费人员类别
		"payer_category":"外阜城镇职工",
		// 医疗参保人员类别
		"insurer_category":"在职职工",
		// 养老保险实际缴费年限
		"pension_years":"8 年 8 个月",
		// 医疗保险实际缴费年限
		"medical_years":"8 年 9 个月",
		// 申报工资
		"declare":{
			"salary":"32000",
			"insurances":[
				{
					"type":"养老",
					"state":"正常(缴费)",
					"base":"23435"
				},
				{
					"type":"失业",
					"state":"正常(缴费)",
					"base":"23435"
				},
				{
					"type":"工伤",
					"state":"正常(缴费)",
					"base":"23435"
				},
				{
					"type":"生育",
					"state":"正常(缴费)",
					"base":"29129"
				},
				{
					"type":"医疗",
					"state":"正常(缴费)",
					"base":"29129"
				}
			]
		},
		// 医疗待遇
		"treatment":"享受实时结算",
		// 统计
		"count":{
			"year":"2020",
			// 门诊
			"clinic":{
				// 大额
				"big":"0",
				// 医保
				"medical":"0"
			},
			// 住院
			"hospitalized":{
				// 统筹
				"whole":"0",
				// 大额
				"big":"0",
				// 医保
				"medical":"0"
			}
		},
		// 社保记录
		"records":[
			{
				"year_month":"2001-08",
				"company":"阿里巴巴",
				"area":"北京市朝阳区社会保险基金管理中心",
				"insurances":[
					{
						"type":"养老",
						"base":"23435",
						"company_deposit":"222",
						"personal_deposit":"2334"
					},
					{
						"type":"失业",
						"base":"23435",
						"company_deposit":"222",
						"personal_deposit":"2334"
					},
					{
						"type":"工伤",
						"base":"23435",
						"company_deposit":"222",
						"personal_deposit":"2334"
					},
					{
						"type":"医疗",
						"base":"23435",
						"company_deposit":"222",
						"personal_deposit":"2334"
					}
				]
			},
			{
				"year_month":"2001-08",
				"company":"阿里巴巴",
				"area":"北京市朝阳区社会保险基金管理中心",
				"insurances":[
					{
						"type":"养老",
						"base":"23435",
						"company_deposit":"222",
						"personal_deposit":"2334"
					},
					{
						"type":"失业",
						"base":"23435",
						"company_deposit":"222",
						"personal_deposit":"2334"
					},
					{
						"type":"工伤",
						"base":"23435",
						"company_deposit":"222",
						"personal_deposit":"2334"
					},
					{
						"type":"生育",
						"base":"23435",
						"company_deposit":"222",
						"personal_deposit":"2334"
					},
					{
						"type":"医疗",
						"base":"23435",
						"company_deposit":"222",
						"personal_deposit":"2334"
					}
				]
			}
		]
	},
	// 公积金
	"accumulation_fund":{
		// 总账信息
		"general":{
			"account":"公积金账号",
			"company":"单位名称",
			"register_number":"单位登记号",
			"department":"所属部门",
			"balance":"账户余额",
			"state":"缴存状态",
			"current_deposit":"当年缴存金额",
			"current_withdraw":"当年提取余额",
			"last_settlement":"上年结转余额(元)",
			"company_rate":"单位缴存比例",
			"personal_rate":"个人缴存比例",
			"month_company_deposit":"单位月缴存额(元)",
			"month_personal_deposit":"单位月缴存额(元)",
			"base":"个人缴存基数(元)",
			"month_deposit":"月缴存额(元)"
		},
		// 公积金缴纳详细信息，保证opt_day时间从大到小有序
		"details":[
			{
				// 余额
				"balance":"6678",
				// 存入
				"deposit":"5000",
				// 汇缴月份
				"opt_month":"2020-10",
				"opt_money":"-0",
				// 发送业务日期
				"opt_day":"2020-12-04",
				// 类型
				"opt_type":"汇缴分配",
				// 汇缴单位
				"opt_company":"百度科技有限公司"
			},
			{
				"balance":"8678",
				"deposit":"6000",
				"opt_month":"2020-10",
				"opt_money":"-0",
				"opt_day":"2020-11-14",
				"opt_type":"汇缴分配",
				"opt_company":"百度科技有限公司"
			},
			{
				"balance":"8678",
				"deposit":"6000",
				"opt_month":"2020-10",
				"opt_money":"-0",
				"opt_day":"2020-11-14",
				"opt_type":"汇缴分配",
				"opt_company":"百度科技有限公司"
			}
		],
		// 对账单
		"bills":[
			{
				"year_range":"2019-2020",
				"amount":"14343.23",
				"detail":{
					"last_settlement":"20000",
					"current_deposit":"10000",
					"current_withdraw":"10000",
					"interest":"50"
				}
			},
			{
				"year_range":"2018-2019",
				"amount":"14343.23",
				"detail":{
					"last_settlement":"20000",
					"current_deposit":"10000",
					"current_withdraw":"10000",
					"interest":"50"
				}
			},
			{
				"year_range":"2017-2018",
				"amount":"14343.23",
				"detail":{
					"last_settlement":"30000",
					"current_deposit":"10000",
					"current_withdraw":"6000",
					"interest":"60"
				}
			},
			{
				"year_range":"2016-2017",
				"amount":"14343.23",
				"detail":{
					"last_settlement":"50000",
					"current_deposit":"20000",
					"current_withdraw":"10000",
					"interest":"70"
				}
			},
			{
				"year_range":"2015-2016",
				"amount":"14343.23",
				"detail":{
					"last_settlement":"50000",
					"current_deposit":"20000",
					"current_withdraw":"10000",
					"interest":"70"
				}
			}
		]
	}
}
```

# AliPay

支付宝即时到账demo，功能包含
- 支付
- 支付异步通知
- 退款
- 退款异步通知

## 业务流程 ##

>业务流程说明：
 
1. 输入对应参数，调用接口生成html表单提交代码。

2. 前台使用返回的html代码，生成新网页，改网页自动跳转到支付页面。

2. 用户选择支付方式并支付订单。

3. 支付宝后台处理交易。

4. 交易处理完成后支付宝异步通知商户后台结果。

5. 商户后台根据返回的支付结果进行其业务逻辑。

## 接口参数 ##

| 参数 | 参数说明 | 样例 |
| --- | --- | --- |
|service|支付宝生成订单接口名称|create_direct_pay_by_user|
|partner|合作者身份ID|2088101011913539|
|seller_id|卖家支付宝用户号|2088002007018966|
|payment_type|支付类型,只支持取值为1（商品购买）|1|
|notify_url|服务器异步通知页面路径|http://o2o.cloume.com/client-web/api/ali/result |
|out_trade_no|商户网站唯一订单号|6843192280647118|
|subject|商品的标题/交易标题/订单标题/订单关键字等。|Ipad mini|
|total_fee|该笔订单的资金总额，单位为RMB-Yuan。取值范围为[0.01，100000000.00]，精确到小数点后两位|100|
|body|商品描述|Ipad mini  16G  白色|

更多参数请参考[即时到账交易接口](https://doc.open.alipay.com/doc2/detail.htm?spm=a219a.7629140.0.0.IYBx0s&treeId=62&articleId=104743&docType=1#)

## 信息配置 ##

在AlipayConfig配置支付宝支付的一些信息
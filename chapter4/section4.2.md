# 微服务接口

**GET '/spiderProtocol'**

获取该爬虫微服务的相关信息, 用于验证其可用性

##### 请求结果示例 
~~~
{
    "code": 0,
    "protocol": {
        "version": "0.1",
        "name": "FULL_FLEDGED_NET_SPIDER_PROTOCOL"
    },
    "config": {
        "singleContent": {
            "url": "not_created",
            "frequency": 5
        },
        "contentList": {
            "url": "localhost:9001/content",
            "frequency": 5,
            "pageSize": 10
        }
    }
}
~~~

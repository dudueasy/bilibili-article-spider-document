# 数据接口

### 获取爬虫数据
**GET '/content'**

获取爬取到的资源, 默认一次返回10条

##### 查询参数:
pageSize:  定义每次获取的资源条数

latestId: 资源 id, 表示上一次访问该接口获取到的最后一个资源 id, 用于保存上次获取资源在数据库中的位置


##### 请求结果

~~~
{
  contentList:{
    resourceId,
    title,
    contentType,
    content: {
      html,
      text,
    },
    tags,
    contentId,
    originalCreatedAt, 
  }
}
~~~

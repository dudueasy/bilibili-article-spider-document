# 爬虫服务

### 命令
~~~
node scripts/spider.js command [parameters]
~~~

##### 命令选项和参数
~~~
// 生成资源 id
generate_ids startNumber endNumber

// 批量爬取资源
start_getting_articles totalCount

// 获取单条资据
get_single_article resourceId 
~~~

##### 示例
~~~
// 生成 0 - 100W 区间的 id
node scripts/spider.js generate_ids 0 100

// 获取 1000 条文章资源
node scripts/spider.js start_getting_articles 1000

// 获取 id 为 2 的文章资源
node scripts/spider.js get_single_article 2
~~~



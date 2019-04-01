# 详细配置
请在项目根目录下创建 .env 文件, 并在文件中定义以下配置项

###  Nodejs 服务器配置 
HOST: 域名 

PORT: 端口

### mongodb 数据库配置
DB_RESOURCE_DB:  爬虫使用的数据库

DB_COLLECTION: 爬虫使用的数据表/collection

DB_URL: mongodb 连接地址

### 爬虫配置 
DEFAULT_TASK: 默认的爬虫任务

RESOURCE_URL_PREFIX: 资源 url 的前置部分 (用来拼接资源 id)

CONTENT_SELECTOR: 资源主体的 css 选择题 (存入数据库的部分)

TARGET_COUNT: 每次要爬取的资源数量

INTERVAL: 爬取每个资源的等待间隔, 以 ms 为单位


### redis 配置 
REDIS_SERVER_HOST: redis 服务器所在域名

REDIS_SERVER_PORT: redis 服务器运行的端口

ID_SET_TO_REDIS_KEY: 用作 id 缓存的集合键名

RETRIEVED_ID_SET_TO_REDIS_KEY: 获取到的资源 id 集合键名

FAILED_ID_SET_TO_REDIS_KEY : 获取失败的资源 id 集合键名


### 配置示例 
~~~ 
# server configuration
HOST = 'localhost'
PORT = 9001

# mongodb configuration
DB_RESOURCE_DB = 'bilibili'
DB_COLLECTION = 'articles'
DB_URL = 'mongodb://localhost:27017'

# spider configuration
DEFAULT_TASK='start_getting_articles'
RESOURCE_URL_PREFIX = 'https://www.bilibili.com/read/cv'
CONTENT_SELECTOR = '.article-holder'
TARGET_COUNT = '100'
INTERVAL = 1000

# Redis options 
# -- redis server host & port 
REDIS_SERVER_HOST = 127.0.0.1
REDIS_SERVER_PORT = 6379

# -- the key of resource Ids set in redis
ID_SET_TO_REDIS_KEY = bilibili_article_id_set

# --the key of retrieved resource Ids set in redis
RETRIEVED_ID_SET_TO_REDIS_KEY = bilibili_article_got_id_set

# --the key of failed resource Ids set in redis
FAILED_ID_SET_TO_REDIS_KEY = bilibili_article_failed_id_set
~~~


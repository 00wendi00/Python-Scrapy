# python-Scrapy
Scrapy框架的使用和研习


一. Scrapy使用说明 :

1. pip install Scrapy .在此目录下已经安装了Scrapy和依赖, 并已经加入环境变量 . E:\wendi1\pyplace\scraping

2. 创建项目(注意项目目录).  scrapy startproject scrapy_example E:\wendi1\pyplace\scrapy_example

3. 进入scrapy_example根目录.
a.定义模型item.py,
b.创建爬虫 scrapy genspider country example.webscraping.com --template=crawl    并完善/spiders/country.py -- rules,parse_item
c.优化设置settings.py

4. 测试爬虫scrapy crawl country -s LOG_LEVEL=DEBUG   可在shell中抓取

5. 执行爬虫,输出结果到csv.  scrapy crawl country --output=countries.csv -s LOG_LEVEL=INFO

6. 可中断和回复的执行. scrapy crawl country --output=countries.csv -s LOG_LEVEL=INFO -s JOBDIR=crawls/country

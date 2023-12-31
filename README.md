# query-domain-icp-python

Python 获取域名 ICP 备案信息 自动破解滑动验证码 支持翻页

数据来源工信部备案系统 https://beian.miit.gov.cn/

本项目仅供学习交流请勿用于非法用途

![](https://p.sda1.dev/13/ebfc449f759b9aa2065245cedcbeb422/GIF%202023-10-31%2016-53-09.gif)

## 安装
```shell
pip install query-domain-icp
```
## 示例

```python
from query_domain_icp import Miit

miit = Miit(debug=False, retry_sleep=0)

##### 查询域名或单位名称
unitName = input("请输入单位名称：")

result = miit.query(unitName)

print(result)


##### 在基础查询上翻页
result = miit.getNextPage(unitName, sign=result["sign"], pageNum=result["nextPage"])

print(result)

```

## 环境

测试环境：python=3.7.9

## 更多

Node.js 版本 https://github.com/qiangmouren/query-domain-icp-nodejs

Java 版本 https://github.com/qiangmouren/query-domain-icp-java

Python 版本 https://github.com/qiangmouren/query-domain-icp-python

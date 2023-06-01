# gh-api-doc (springdoc功能包)

### 配置
```
spring:
  servlet:
    multipart:
      # 单个文件最大大小
      max-file-size: 100MB
      # 单次请求最大大小
      max-request-size: 100MB
springdoc:
  swagger-ui:
    path: /swagger-ui.html
    tags-sorter: alpha
    operations-sorter: alpha
    show-extensions: true
  api-docs:
    path: /v3/api-docs
  group-configs:
    - group: '测试'
      paths-to-match: '/test/**'
      packages-to-scan: com.gh.boot
  default-flat-param-object: false
knife4j:
  enable: true
  setting:
    language: zh_cn
    swagger-model-name: 实体类列表
  documents:
    - name: 标题1
      locations: classpath:markdown/*
      group: default
    - name: 标题2
      locations: classpath:markdown1/*
      group: 用户模块
  basic:
    enable: false
    username: zhangsan
    password: lisi
gh-api-doc:
  title: 测试api接口文档
  description: 在线测试api接口文档
  terms-of-service: https://github.com/ghuan
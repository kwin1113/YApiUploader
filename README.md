# YApi J

## 简介

根据规范的JavaDoc/注解解析接口文档，一键上传至YApi。
使用前请先进行YApi相关配置，及解析规则配置。

### 使用



### 配置

* **YApi地址：**必填。
* **过滤列表：**允许为空。添加类的全限定名以过滤，在解析接口文档时不对列表中的类进行解析，通常用于内部网关上下文等对象的过滤。
* **项目列表：**必填，在配置前请先配置YApi列表并保存。添加YApi项目的token，将自动将其解析为项目名称（进入配置页时将进行刷新，请及时删除无效token）。
* **配置模板：**必填。配置接口文档的解析规则。

#### 模板的具体配置方式

* **规则名称：**该字段全局唯一，以区分不同的接口文档解析规则。

* **basePath定位：**该配置允许为空。用于定位接口的基本路径，将解析接口类上的注释/注解。

* **method定位：**该配置允许为空。用于定位接口的请求方式，允许为空以支持内部统一网关接口注册方式，将默认以POST方式注册到YApi。

* **path定位：**必填。用于定位接口路径。当定位方式为注解时，依次填入注解中接口路径定位对应属性，例如value，及注解类全限定名；当定位方式为注释时，请填入注释对应tag。



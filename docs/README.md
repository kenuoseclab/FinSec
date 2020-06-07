
# 最新漏洞修复方案

## Fastjson <= 1.2.68 安全风险
* 漏洞成因：/
* 漏洞影响：/
* 公开时间：20200528
* 漏洞等级：高危
* 影响范围：Fastjson <= 1.2.68, Fastjson sec版本 <= sec9
* 修复方案：
  * 1.升级Fastjson到1.2.69版本以上
  * 2.升级Fastjson到1.2.68，并开启safeMode,禁用autoType（https://github.com/alibaba/fastjson/wiki/fastjson_safemode）, 遇到兼容性问题可直接升级到sec10小版本

```
1.1.15~1.1.31 -> 1.1.31.sec10
1.1.32~1.1.33 -> 1.1.33.sec10
1.1.34 -> 1.1.34.sec10
1.1.35~1.1.46 -> 1.1.46.sec10
1.2.0~1.2.2 -> 1.2.2.sec10 因为1.2.3之后的版本Map是没有排序输出的，如果不关注这个兼容问题，升级到1.2.70
1.2.3~1.2.7 -> 1.2.7.sec10 因为1.2.7使用最多特别提供，也可以直接使用1.2.8.sec10
1.2.8 -> 1.2.8.sec10
1.2.9~1.2.29 -> 1.2.29.sec10
1.2.30~1.2.48 -> 1.2.48.sec10
1.2.49~1.2.68 -> 1.2.69或1.2.70 中间有很多sec10小版本，建议直接升级到1.2.69或1.2.70，如果遇到兼容再考虑sec10版本
如果还遇到其他兼容问题，这里有更多的sec10版本 https://repo1.maven.org/maven2/com/alibaba/fastjson/

```
* 参考：
    * https://github.com/alibaba/fastjson/releases/tag/1.2.68
    * https://github.com/alibaba/fastjson/wiki/fastjson_safemode
    * 【安全通告】Fastjson <=1.2.68全版本远程代码执行漏洞通告 http://www.bqq8.com/index.php?id=2354


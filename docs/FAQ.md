# 问题

## 问题1：原始数据的分辨率为1min，通过求平均值重采样为15min时，重采样后的时间标签与采样前数据时段对应关系是什么？
解答：例如：重采样后的00:00的值等于00:00 - 00:15的平均值
程序文件： project_code/resample/resample_data.py

## 问题2：在使用https://www.visualcrossing.com/usage 的天气数据前提下，网站每日天气免费下载量不够日内负荷预测算法消耗，需额外付费不划算？
解答：
日内提前4小时负荷预测算法运行一轮需要消耗26条下载量，运行一日约消耗2496下载量
网站每日免费下载量为1000，收费标准为0.0007元/条，倘若使用该数据每日新增消费1.05元

## 问题3：在当前的特征工程策略下，https://www.visualcrossing.com/usage 的天气数据对负荷预测精度几乎没有提升，建议弃用？
解答： 打算弃用

## 问题4：是否考虑在数据清洗(预处理)阶段，使用回溯方法处理异常/缺失值？
解答：https://skforecast.org/0.10.1/user_guides/backtesting.html  Backtesting回溯测试

## 项目依赖的第三方库导出方式？
解答：在项目根目录用pipreqs ./ --encoding=utf-8
https://zhuanlan.zhihu.com/p/385402838 pip与pipreqs打包区别

# 参考文档
https://zhuanlan.zhihu.com/p/341842461  python开发基础----目录结构层次

https://cloud.tencent.com/developer/article/1175298  python 软件目录结构规范

https://markdown.com.cn/basic-syntax/code.html  markdown语法

https://www.cnblogs.com/abc-x/p/13470575.html  Markdown基本语法及生成目录结构的方法

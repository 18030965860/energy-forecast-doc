# 预测算法简介
萧山单个微电网日前短期负荷预测：预测未来24小时的每15分钟的负荷功率；<br>
萧山单个微电网日内短期负荷预测：预测未来4小时的每15分钟的负荷功率；<br>
萧山单个微电网日内超短期负荷预测：预测未来1小时的每5分钟的负荷功率；

## 输入参数
   1. 输入参数配置文件地址<br>
    `E:\0_CODE\Github\VPP_xiaoshan-LoadForecast\project_code\static_params\parameters.py`
   3. 根据场景需求与条件配置好相关参数

### **参数1**
|参数|变量名|数据类型|缺省值|备注|
|--|:--:|--:|--:|--:|
根目录|`root_directory`|`str`|`"../"`
预测时间长度|`forecast_days`|`float`|`1.0`
预测数据分辨率|`target_freq`|`str`|`'15min'`|`{5min,15min}`
采用自定义特征工程的变量|`custom_features`|`list`|`['temp1','temp2','temp3','temp4']`
采用滞后特征工程的变量|`lags_features`|`list`|`["t_p"]`
采用外生特征工程的变量|`exogenous_features`|`list`|`['temp1','temp2','temp3','temp4']`
模型名称|`model_name`|`str`|`lgb`|`{SVR,linerRegressor,xgb,lgb}`
集成策略|`ensemble`|`str`|`none`|`{bagging,stacking,ensemble,none}`
多步策略|`strategy`|`str`|`none`|`{direct,recursive,multioutput,directRecursive,none}`
启动训练|`training`|`bool`|`1`
在线训练|`fine_tune`|`bool`|`0`
验证集百分比|`percetage`|`float`|`0.3`|`[0,0.5]`




### **读取E云平台天气数据**
|参数|变量名|数据类型|缺省值|备注|
|--|:--:|--:|--:|--:|
sn|`weather_api_sn`|`int`|`1110700443226525`
url|`weather_api_url`|`str`|`..`
token|`weather_api_token`|`str`|`..`
field|`weather_api_field`|`list`|`['temp1','temp2','temp3','temp4']`
数据分辨率|`weather_api_freq`|`str`|`'1min'`

### **读取E云平台负荷数据**
|参数|变量名|数据类型|缺省值|备注|
|--|:--:|--:|--:|--:|
sn|`load_api_sn`|`int`|`1110700265169510`
url|`load_api_url`|`str`|`..`
token|`load_api_token`|`str`|`..`
field|`load_api_field`|`list`|`['t_p']`
数据分辨率|`load_api_freq`|`str`|`'1min'`


### **读取第三方平台天气数据**
|参数|变量名|数据类型|缺省值|备注|
|--|:--:|--:|--:|--:|
url|`exogenous_api_url`|`str`|`..`
token|`exogenous_api_token`|`str`|`..`
经纬度|`exogenous_api_location`|`dict`|`{'lon':120.32,'lat':30.22}`





## 预测文件
|类型|位置|
|--|:--:|
日前短期负荷预测|`'./VPP_xiaoshan_load/sn_1110700265169510/Short_ahead_96/forecast_results/y_preds.csv'`
日内短期负荷预测|`'./VPP_xiaoshan_load/sn_1110700265169510/Short_ahead_16/forecast_results/y_preds.csv'`
日内超短期负荷预测|`'./VPP_xiaoshan_load/sn_1110700265169510/Ultra_Short_ahead_16/forecast_results/y_preds.csv'`


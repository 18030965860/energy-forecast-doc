# 部署
##  python环境 & 第三方包
python == 3.7.7<br>
chinese_calendar==1.8.0<br>
joblib==0.14.1<br>
lightgbm==2.3.1<br>
Logger==1.4<br>
matplotlib==3.3.0<br>
numpy==1.26.1<br>
pandas==1.3.5<br>
pip==23.3.1<br>
requests==2.28.1<br>
schedule==1.1.0<br>
scikit_learn==1.3.2<br>
seaborn==0.11.2<br>
setuptools==65.5.1<br>
sktime==0.16.0<br>
xgboost==1.6.2

## Linux系统
1. 路径切换至项目文件夹根目录;
2. 根目录下创建虚拟环境(注意：虚拟环境的python版本!!!)<br>
`python -m venv venv`
3. 启动虚拟环境<br>
	`source ./venv/scripts/activate`
4. 下载第三方库<br>
`pip install -r requirements.txt`
1. 路径切换至算法文件夹<br>
`cd ./project_code/`
1. 启动后台自动运行<br>
`nohup python main.py`
1. 设置开机自启动（？）
2. 部署完成

## windows 系统
1. 路径切换至项目文件夹根目录
2. 根目录下创建虚拟环境(注意：虚拟环境的python版本!!!)<br>
`python -m venv venv`
3. 启动虚拟环境<br>
`./venv/scripts/activate`
4. 下载第三方库<br>
`pip install -r requirements.txt`
5. 路径切换至算法文件夹<br>
`cd ./project_code/`
6. 启动后台自动运行<br>
`pythonw main.py`
7. 部署完成
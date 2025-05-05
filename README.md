# 代码

## GRU

1. gru.py : 训练模型的python文件

2. gru_test.py : 模型测试的python文件

3. gru_model1.pth ：辣椒类产品的最优GRU模型文件；**gru_model**后的数字若为2-6则依次是花叶、水生根、食用菌、花菜、茄类的最优GRU模型文件

4. data1.pt：辣椒类产品数据集划分结果；**data**后的数字若为2-6则依次是花叶、水生根、食用菌、花菜、茄类的数据集划分结果

5. log1.out.tfevents.1744971254.Bing.13740.0：辣椒类产品对应的GRU模型在训练时tensorboard记录下的信息文件；**log**后的数字若为2-6则依次是花叶、水生根、食用菌、花菜、茄类对应的GRU模型在训练时tensorboard记录下的信息文件

6. log1.log：记录辣椒类产品的最优GRU模型的参数以及该模型的训练信息；**log**后的数字若为2-6则依次记录的是花叶、水生根、食用菌、花菜、茄类最优GRU模型的参数以及该模型的训练信息
   
   

## RF

1. rf.py ：训练模型的python文件

2. rf_test.py：模型测试的python文件

3. hyperparameter_results_day_1.csv：辣椒类产品的每个RF模型超参数组合对应的评价指标值；**hyperparameter_results_day_** 后的数字若为2-6则依次是花叶、水生根、食用菌、花菜、茄类每个RF模型超参数组合对应的评价指标值，0代表的是蔬菜单品的每个RF模型超参数组合对应的评价指标值

4. rf_day_1.pkl : 辣椒类产品的最优RF模型文件；**rf_day_** 后的数字若为2-6则依次是花叶、水生根、食用菌、花菜、茄类产品的最优RF模型文件



## XGBoost

1. models.xgboost.py : 训练模型的python文件

2. XGB_test.py ：模型测试的python文件

3. xgboost_pred.py ：模型预测的python文件

4. hyperparameter_results_day_1.csv ：辣椒类产品的每个XGBoost模型超参数组合对应的评价指标值；**hyperparameter_results_day_** 后的数字若为2-6则依次是花叶、水生根、食用菌、花菜、茄类每个XGBoost模型超参数组合对应的评价指标值，0代表的是蔬菜单品的每个XGBoost模型超参数组合对应的评价指标值

5. xgboost_best_model1.pkl ：辣椒类产品的最优XGBoost模型文件;**xgboost_best_model**  后的数字若为2-6则依次是花叶、水生根、食用菌、花菜、茄类产品的最优XGBoost模型文件



## 特征选择

select_features.py ：针对每一个大类以及蔬菜单品选择影响其需求量的重要特征

## 数据处理与描述性统计

1. 数据处理与描述统计.r ：数据处理以及描述性统计的R语言文件

2. holiday.py：数据处理中筛选中国节假日的python文件



# 数据

## 原始数据

附件1-3包含了蔬菜订单的具体情况，需要将这三组数据进行汇总整合

## 处理后的数据

### all—蔬菜单品

1. data : 数据处理后的数据，每一天不同蔬菜单品销售情况

2. all_data : data删除"code_name"和“classify_name”两列，真正可以用于训练的数据

3. train_selected_ml_day.csv、val_selected_ml_day.csv、test_selected_ml_day.csv：输入all_data进行特征选择，基于筛选出的重要特征，划分训练集、验证集、测试集

4. 预测数据集pred_single.csv：用于预测的数据集（基于筛选出的46个单品）

5. all.png：影响辣椒类产品需求量的特征的重要性(直方图)

### 大类—每个种类

以辣椒为例

1. classify_1_dataset_day.csv ：辣椒类产品每天的销售情况

2. train_selected_ml_day.csv、val_selected_ml_day.csv、test_selected_ml_day.csv：输入classify_1_dataset_day.csv进行特征选择，基于筛选出的重要特征，划分训练集、验证集、测试集

3. 预测数据集pred_1.csv ：辣椒类产品用于预测的数据集

4. 1.辣椒.png ：影响辣椒类产品需求量的特征的重要性(直方图)



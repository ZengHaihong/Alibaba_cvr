April 7, 2018 11:48 PM
提交一份baseline,成绩为276，0.08178

---
April 8, 2018 10:49 PM
1、采取17~22的数据来训练，23的数据来做验证，24的数据来测试
2、不采取one-hot编码
3、离散连续值


- - -


April 11, 2018 11:21 PM
工作超级忙，两天不提交，排名已经300名开外了
version2 采用了20~22的转化率，20-22的数据训练，23日做验证，24的数据做测试
lightgbm的参数调节措施：
```python 
boosting_type='gbdt', num_leaves=15, max_depth=6, learning_rate=0.01, n_estimators=10000,max_bin=425, subsample_for_bin=50000, objective='binary', min_split_gain=0,min_child_weight=5, min_child_samples=10, subsample=1, subsample_freq=1,min_data_in_leaf = 2000,bagging_fraction =0.7,bagging_freq = 1,
colsample_bytree=1, reg_alpha=3, reg_lambda=5, seed=1000, nthread=-1, silent=True
```
**线下测评结果** 
```python
[1113]	training's binary_logloss: 0.0801181	valid_1's binary_logloss: 0.0793828
```


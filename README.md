# o2o
welcome

###2019.2.13


0.添加辅助列
coupon_use	是否用券购买	int（1-是  0-否）  【 y-预测列 】  
coupon_not_use	是否未领取优惠券但购买了	int（1-是  0-否）  
not_buy	是否领取优惠券但未购买	int（1-是  0-否）  



1. 添加用户特征
total_count	该用户共有几条记录  
coupon_count	该用户共领了几张券（2）  
buy_count	该用户共购买几次  
use_count	该用户共用券购买了几次 （3）  
coupon_not_use_count	用户对coupon_not_use=1的统计  
not_buy_count	用户对not_buy=1的统计  

2. 添加优惠券特征  
Discount_rate_num	优惠券的优惠率	dtype: float64  

3. 第一次预测结果 0.58052498  



###2019.2.14  
目标：添加更多特征  
a. 用户领取优惠券后的核销率（4） use_count/coupon_count  相关度0.41(大大提高)  
b. 辅助特征：满减区间0-50, 50-200, 200-500  
c. 统计用户在三个区间的核销率  

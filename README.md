# YBStockChartView

### 效果图
<div align=center><img src="http://upload-images.jianshu.io/upload_images/2887144-6f2410310de3f681.gif?imageMogr2/auto-orient/strip"/></div>

### 注: 因为用的是新浪的接口, 在每天09:30之前demo会因为对新浪的数据处理不合理会crash

### 初始化K线图, 分时图和五日视图初始化方式差不多
```
// 初始化K线图:
self.stockChartView = [[YBStockChartView alloc] initWithFrame:CGRectMake(0, 150, [UIScreen mainScreen].bounds.size.width, 300)];
// 上下模块比例
self.stockChartView.prop = 0.7;
// 设置代理
self.stockChartView.delegate = self;
// 内边距
self.stockChartView.padding = UIEdgeInsetsMake(10, 10, 0, 10);
[self.view addSubview:self.stockChartView];

// modelArray存放的是YBStockChartModel对象的模型数组
self.stockChartView.dataArray = modelArray; // 赋值
[self.stockChartView setNeedsDisplay];  //  刷新界面

```


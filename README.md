# Pro-City-County
一款原生开源的 javascript 插件，用于生成省市区选择器，基本用法十分简单。
## 使用方法
最简单的使用只需要两个步骤：

1. 放置容器，引入依赖

		<!--存放省市区数据的三个 select-->
		<select id="province"></select>
		<select id="city"></select>
		<select id="district"></select>
		
		<!--引入插件-->
		<script src="./cj-pcd-1.0.1.min.js"></script>

2. 调用方法

 		var pcd = new CJPCD('province','city','district');
 ## API
 1. 初始化
		/**
			provinceId ：省份 select id
			cityId     ：城市 select id
			districtId ：县区 select id
		*/
    
   		var pcd = new CJPCD(provinceId,cityId,districtId);
2. 重置
		pcd.reSet();
3. 获取值
		pcd.getValue('json');//指定以json对象返回
		pcd.getValue();//默认以json对象返回,效果同上
	 json 对象返回如下：
		{"province":"广东省","city":"广州市","district":"越秀区"};
    
	指定拼接成一定格式的字符串进行返回,以逗号为例(当然也可以使用其他字符串)
		pcd.getValue(',');//结果使用逗号拼接成字符串
	返回值如下
		"广东省,广州市,越秀区"

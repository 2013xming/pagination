 # pagination
 分页插件，依赖于jquery。
 功能说明：
 1、插件自身不包括分页请求数据功能，仅实现样式显示功能；但是支持用户自定义点击操作函数，支持分页显示逻辑和分页回调操作的分离。
2、插件可以调整页码总数，显示页数，上一页，下一页参数的替换和跳转功能的隐藏。
使用说明：
 在引入css文件和js 文件后，

var options = {
	fixedDiff : 5, 
	currentPage : 1,
	totalPage : 15,
	showPageSlector:true,
	prePageText:'<<',
	nextPageText:'>>',
	pageClick : function(e,num){
		console.log(num);
	},
	submit: function(e,num){
		console.log(num);
	}
}
var page = new pagingPlugin(options,"pagination");

options 是参数对象，"pagination"是Dom ID，fixedDiff 是显示的页码数量，页码是中间部分时，前后出现 "..." 表示;currentPage：初始时当前页码;
totalPage：初始时总页码数;showPageSlector：是否显示跳转栏，默认为true;prePageText:'上一页'按钮字符，默认是"<上一页";
 nextPageText:'下一页'按钮字符，默认是"下一页>";pageClick:用户自定义点选 上一页、下一页或者数字页时的事件函数，并传入event和 页码两个参数，用户可以自定义在此做拉取数据显示的操作，不会影响样式；
#submit：用户自定义跳转页面的事件函数，并传入event和 页码两个参数，用户可以自定义在此做拉取数据显示的操作，不会影响样式；

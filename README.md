# echart漏斗图
[预览](https://xh747364.github.io/echartfunnel/index.html "悬停显示")<br>
![image](https://github.com/xh747364/echartfunnel/blob/master/example.png)
```javascript
var myChart = echarts.init(document.getElementById('chart'));
var option = {
	tooltip: {
		trigger: 'item',
		formatter: "{a} <br/>{b} : {c}"
	},
	calculable: true,
	color: ['#EE6765','#3FA0FF','#50CB74','#FAD344','#7720B2'],
	series: [
		{   //中间显示的数字
			name: '漏斗图',
			type: 'funnel',
			left: '10px',
			top: 10,
			bottom: 20,
			width: '60%',
			min: 0,
			max: 100,
			minSize: '20%',
			maxSize: '100%',
			sort: 'descending',
			gap: 2,
			label: {
				normal: {
					show: true,
					position: 'inside',
					formatter: "{c}"
				}
			},
			labelLine: {
				normal: {
					length: 100,
					lineStyle: {
						width: 1,
						type: 'solid'
					}
				}
			},
			itemStyle: {
				normal: {
					show: true,
					position: 'inside',
					borderWidth: 0
				}
			},
			data: [
				{value: 60, name: '变量1'},
				{value: 40, name: '变量2'},
				{value: 20, name: '变量3'},
				{value: 80, name: '变量4'},
				{value: 90, name: '变量5'}
			]
		},
		{   //右边显示文字
			name: '漏斗图',
			type: 'funnel',
			left: '10px',
			top: 0,
			bottom: 20,
			width: '60%',
			min: 0,
			max: 100,
			minSize: '20%',
			maxSize: '100%',
			sort: 'descending',
			gap: 2,
			label: {
				normal: {
					show: true,
					position: 'right',
					color: 'rgba(0,0,0,.65)',
					formatter: `{b}`
				}
			},
			labelLine: {
				normal: {
					length: 100,
					lineStyle: {
						width: 1,
						type: 'solid'
					}
				}
			},
			itemStyle: {   //隐藏漏斗图
				normal: {
					opacity: 0,
					position: 'inside',
					borderWidth: 0
				}
			},
			data: [
				{value: 60, name: '变量1'},
				{value: 40, name: '变量2'},
				{value: 20, name: '变量3'},
				{value: 80, name: '变量4'},
				{value: 90, name: '变量5'}
			]
		},
		{   //右边显示的数字 并调整位置
			name: '漏斗图',
			type: 'funnel',
			left: '10px',
			top: 20,
			bottom: 0,
			width: '60%',
			min: 0,
			max: 100,
			minSize: '20%',
			maxSize: '100%',
			sort: 'descending',
			gap: 2,
			label: {
				normal: {
					show: true,
					position: 'right',
					color: '#EE6765',
					fontFamily: 'Akzidenz-Grotesk-BQ',
					fontSize: '20',
					formatter: `{c}`
				}
			},
			labelLine: {
				normal: {
					length: 100,
					lineStyle: {
						width: 0,
						type: 'solid'
					}
				}
			},
			itemStyle: {  //隐藏漏斗图
				normal: {
					opacity: 0,
					position: 'inside',
					borderWidth: 0
				}
			},
			data: [
				{value: 60, name: '变量1'},
				{value: 40, name: '变量2'},
				{value: 20, name: '变量3'},
				{value: 80, name: '变量4'},
				{value: 90, name: '变量5'}
			]
		}
	]
}
myChart.setOption(option);
```
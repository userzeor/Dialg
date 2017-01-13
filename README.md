1.html
<section>
	<button id="t_btn">警告框</button>
	<button id="t_btn1">对话框</button>
	<button id="t_btn2">输入框</button>
	<button id="t_btn3">消息提示框</button>
	<button id="t_btn4">等待加载框</button>
</section>

2.js
var t_btn = document.querySelector('#t_btn');
var t_btn1 = document.querySelector('#t_btn1');
var t_btn2 = document.querySelector('#t_btn2');
var t_btn3 = document.querySelector('#t_btn3');
var t_btn4 = document.querySelector('#t_btn4');
t_btn.addEventListener('click',function () {
	AMI.alert('温馨提示','是否关闭?','确定',function () {
		
	});
});
t_btn1.addEventListener('click',function () {
	AMI.confirm('温馨提示','是否关闭?',['是','否'],function (e) {
		if (e.index==0) {
			alert('0');
		}
		if (e.index==1) {
			alert('1');
		}
	});
});
t_btn2.addEventListener('click',function () {
	AMI.prompt('温馨提示','是否关闭?','确定',function (e) {
		alert(e.value);
	});
});
t_btn3.addEventListener('click',function () {
	AMI.toast('是否成功');
});
t_btn4.addEventListener('click',function () {
	AMI.showloading('玩命加载中...');
	setTimeout(function () {
		AMI.hiddenloading();
	},2000);
});
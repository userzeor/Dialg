1.html
<section>
	<button id="t_btn">�����</button>
	<button id="t_btn1">�Ի���</button>
	<button id="t_btn2">�����</button>
	<button id="t_btn3">��Ϣ��ʾ��</button>
	<button id="t_btn4">�ȴ����ؿ�</button>
</section>

2.js
var t_btn = document.querySelector('#t_btn');
var t_btn1 = document.querySelector('#t_btn1');
var t_btn2 = document.querySelector('#t_btn2');
var t_btn3 = document.querySelector('#t_btn3');
var t_btn4 = document.querySelector('#t_btn4');
t_btn.addEventListener('click',function () {
	AMI.alert('��ܰ��ʾ','�Ƿ�ر�?','ȷ��',function () {
		
	});
});
t_btn1.addEventListener('click',function () {
	AMI.confirm('��ܰ��ʾ','�Ƿ�ر�?',['��','��'],function (e) {
		if (e.index==0) {
			alert('0');
		}
		if (e.index==1) {
			alert('1');
		}
	});
});
t_btn2.addEventListener('click',function () {
	AMI.prompt('��ܰ��ʾ','�Ƿ�ر�?','ȷ��',function (e) {
		alert(e.value);
	});
});
t_btn3.addEventListener('click',function () {
	AMI.toast('�Ƿ�ɹ�');
});
t_btn4.addEventListener('click',function () {
	AMI.showloading('����������...');
	setTimeout(function () {
		AMI.hiddenloading();
	},2000);
});
	<script type="text/javascript">
		// 默认隐藏 右上部分 显示名称 和登录按钮
		document.getElementById("header__login").style.display = 'none'
		document.getElementById("header__login2").style.display = 'none'
		let username = localStorage.getItem("userName")
		if (username != "" && username != undefined) {
			document.getElementById("userName").innerHTML = username
			document.getElementById("header__login").style.display = 'block'
		} else {

			document.getElementById("header__login2").style.display = 'block'
		}


		let elements = document.getElementsByClassName('recommend')

		for (var i = 0; i < elements.length; i++) {
			elements[i].addEventListener("click", function() {
				window.location.href = 'details.html'
			});
		}
		

		
		const divObj=document.getElementsByClassName('time')[0];
		    setInterval(()=>{
		        const nowTime=getNowTime();
		        divObj.innerText=nowTime;
		    })
		    function getNowTime(){
		        const date=new Date();
		        const year=date.getFullYear();
		        const month=date.getMonth();
		        const day=date.getDate();
		        const hour=date.getHours();
		        const minite=date.getMinutes();
		        const seconds=date.getSeconds();
		        return `${year}-${month}-${day} ${hour}:${minite}:${seconds<10?'0'+seconds:seconds}`
		    }




		function closes() {
			document.getElementById("social").style.display = "none"
			document.getElementById("f1").style.display = "block"

		}

		function kaiqi() {
			document.getElementById("social").style.display = "block"
			document.getElementById("f1").style.display = "none"

		}

	</script>

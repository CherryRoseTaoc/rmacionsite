 <!DOCTYPE html>
	<html>
		<head>
			<title>validateForm</title>

			<style>

				body {
					background-image: url(b.jpg);
				}

				#login {
					 	background-color:rgba(50,50,50,.6);
					width:600px;
					height:auto;
					float:center;
					 

					 
				}

				 

				#log {
					width:120px;
					height:50px; 
					padding-left: 5px;
					border:none;
					background-color: green;
					font-size: 20px;
					color:white;
					font-weight: bolder;
				}

				#log:hover {
					 border:none;
					color:white;
					background-color: rgba(10,255,10,.5);
					cursor:pointer;
				}

				input[type=text],[type=password] {
					background-color:rgba(50,50,50,.5);
					width:220px;
					height:25px;  
					border-color:red;
					padding:10px;
					color:lightblue;
					font-size: 16px;
					margin:20px;
					border-radius: 10px;

				}

				input:focus {
					background-color: black;
					color:white;
					box-shadow: 0 0 25px red;

				}

				 
 				span, p {
 					color:white;
 					font-size: 50px;
 				}

 				button {
 					width:90px;
 					height:40px;
 					margin:15px;
 					background-color:black;
 					border:none;
 					color:white;
 					border-radius: 20px;
 					box-shadow: 0 0 20px green;
 				}

 				button:hover {
 					background-color:rgba(0,0,0, .5);
 					box-shadow: 0 0 20px lightgreen;
 				}

 			 #info {
 			 	color:white;

 			 }

 			 #print {
 			 	font-size: 15px;
 			 	font-weight: bolder;
 			 }

 			 #information {
 			 	background-color:rgba(100,10,10,.5);
 			 	width: 100%;
 			 	height: 100px;
 			 	text-shadow: 0 0 30px lightgrey;
 			 }
			 

			</style>

			<script>

			function printfunction() {
				window.print();
			}

				function validateForm() {
					var fname = document.getElementById("fname").value;
					var lname = document.getElementById("lname").value;
					var uname= document.getElementById("uname").value;
					var name = document.getElementById("name").value;
					var password = document.getElementById("password").value;
					var confirmpassword = document.getElementById("confirmpassword").value;

					if (  fname == null || fname == "") {
						alert("INPUT YOUR FIRSTNAME.....");
						} 

						if (lname == null || lname == ""){
							alert("INPUT YOUR LASTNAME...");
							return false;
							 }

							if (uname == null || uname == "") {
								alert("INPUT YOUR USERNAME...");
								return false;
								} 

								if (name == null || name == "") {
									alert("INPUT YOUR E-MAIL ADDRESS...");
									return false;
									} 

									 

									if (password == null || password == "") {
										alert("INPUT YOUR PASSWORD...");
										 return false;
										 }

										if (password != confirmpassword) {
											alert("MISMATCH PASSWORD... hahaha....");
											 return false;
										}
						else {
						alert(" GOOD DAY " + uname.toUpperCase() + "," + "\nSUCCESSFULLY LOGGED IN WITH YOUR ACCOUNT\nFIRSTNAME: " + fname.toUpperCase() + "\nLASTNAME: " + lname.toUpperCase() + "\nE-MAIL ADDRESS: " +name+ "\nENJOY WITH MY CALCULATOR....");
						return true;
					}

				}



				 
			</script>
		 

		</head>

		<body>
		 
			 
			<center><br><br>
				<div id = "login">
					<form action = "calc.html" onsubmit="return validateForm()">  
					<div id = "information"><br>
						<h1 id = "info">---------- INFORMATION ---------- <p id = "time"></p></h1>
					</div>
								
							 <input type = "text" id = "fname" placeholder= "Enter your Firstname..." >
							 <span id = "comment"></span>
							 <input type = "text" id = "lname" placeholder= "Enter your Lastname" ><br><br>
							<input type = "text" id = "uname" placeholder= "Enter Username..." > 
							 <input type = "text" id = "name" placeholder= "Enter your E-mail Address..." >
							 <input type = "password" id = "password" placeholder= "Enter your Password..." ><br>
							 <input type = "password" id = "confirmpassword" placeholder = "Confirm your Password..."><br>
							 <button id = "log" onclick "validateForm()">CREATE</button><br>
							 
							<button onclick = "printfunction()" id = "print">PRINT</button>
				    </form>  
 				 </div>

				 
			</center>
		</body>
	</html>

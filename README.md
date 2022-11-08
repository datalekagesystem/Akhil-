
IMPLEMETATION & RESULTS


INDEX .PHP

<!DOCTYPE html>
<html>
<head>
	<title>Data Leakage</title>
	<?php require_once("include.php");?>
	<link rel="stylesheet" href="main.css">
	<style media="screen">
		.front-background{
			background-image: url("assets/data-leakage-detection.jpg");
			height: 100vh;
			width: 100vw;
		}
	</style>
</head>
<body>
<?php
require_once("index_menubar.php");
?>
<div class="container-fluid">
		<div class="row">
            <div class="col-sm-12 front-background">
							<h1 class="text-center text-white p-4">Data Leakage Detection System</h1>
						</div>
		</div>
	</div>
</body>
</html>


MAIN.CSS


.white:link,.white:visited{
	color:white;
}
.front-background{
	background-image: url("../assets/data-leakage-detection.jpg") !important;
	width: 100vw;
	height: 100vh;
}


NONACTIVEMENUBAR.PHP

<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <a class="navbar-brand" href="../index.php">Data Leakage</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item active">
        <a class="nav-link" href="../index.php">Home</a>
      </li>
    </ul>

    <ul class="navbar-nav">
      <li class="nav-item">
        <a class="nav-link" href="register.php">Register</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="login.php">Login</a>
      </li>
    </ul>
  </div>
</nav>

USERMENUBAR.PHP

<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <a class="navbar-brand" href="../index.php">Data Leakage</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <?php
           if($_SESSION['usertype']=="user"){
            echo "
<li class='nav-item active'>
        <a class='nav-link' href='user_dashboard.php'>Home</a>
      </li>
            ";
           }
      ?>

    </ul>

    <ul class="navbar-nav">
      <li class="nav-item">
        <a class="nav-link" href="../main/logout.php">Logout</a>
      </li>
    </ul>
  </div>
</nav>


USER_SIDE_MENUBAR.PHP


<div class="list-group my-3">
	<a href="../main/edit_profile.php" class="list-group-item"><i class="fas fa-user-edit"></i> Edit Details</a>
	<a href="send_files.php" class="list-group-item"><i class="fas fa-share-square"></i> Send Files</a>
	<a href="key_request.php" class="list-group-item"><i class="fas fa-key"></i> Key Request</a>
	<a href="users_list.php" class="list-group-item"><i class="fas fa-users"></i> Sent Files(by me)</a>
	<a href="distributor_files.php" class="list-group-item"><i class="fas fa-file"></i> Files (Send by another)</a>
</div>


INDEX_MENUBAR.PHP


<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <a class="navbar-brand" href="index.php">Data Leakage</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item active">
        <a class="nav-link" href="index.php">Home</a>
      </li>
    </ul>

    <ul class="navbar-nav">
      <li class="nav-item">
        <a class="nav-link" href="main/register.php">Register</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="main/login.php">Login</a>
      </li>
    </ul>
  </div>
</nav>

INCLUDE.PHP

<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-giJF6kkoqNQ00vy+HMDP7azOuL0xtbfIcaT9wjKHr8RbDVddVHyTfAAsrekwKmP1" crossorigin="anonymous">

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/js/bootstrap.bundle.min.js" integrity="sha384-ygbV9kiqUc6oa4msXn9868pTtWMgiQaeYH7/t7LECLbyPA2x65Kgf80OJFdroafW" crossorigin="anonymous"></script>


<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.6.3/css/all.css" integrity="sha384-UHRtZLI+pbxtHCWp1t77Bi1L4ZtiqrqD80Kn4Z8NTSRyMA2Fd33n5dQ8lWUE00s/" crossorigin="anonymous">


<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
<link rel="stylesheet" type="text/css" href="../main.css?<?=microtime()?>">



DISTRIBUTOR_SIDE_MENUBAR.PHP

<br>
<div class="list-group">
	<a href="../main/edit_profile.php" class="list-group-item"><i class="fas fa-user-edit"></i> Edit Details</a>
  <a href="send_files.php" class="list-group-item"><i class="fas fa-share-square"></i> Send Files</a>
  <a href="key_request.php" class="list-group-item"><i class="fas fa-key"></i> Key Request</a>
  <a href="users_list.php" class="list-group-item"><i class="fas fa-users"></i> Sent Files (by me)</a>  
  <a href="distributor_files.php" class="list-group-item"><i class="fas fa-file"></i> Files(Send by another)</a>  
</div>


DISTRIBUTOR_MENUBAR.PHP
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="../index.php">Data Leakage</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <?php 
           if($_SESSION['usertype']=="distributor"){
            echo "
<li class='nav-item active'>
        <a class='nav-link' href='distributor_dashboard.php'>Home</a>
      </li>
            ";
           }
      ?>
                        
    </ul>
    
    <ul class="navbar-nav">      
      <li class="nav-item">
        <a class="nav-link" href="../main/logout.php">Logout</a>
      </li>                                    
    </ul>
  </div>
</nav>


ADMIN_SIDEBAR.PHP


<br>
<div class="list-group">
	<a href="../main/edit_profile.php" class="list-group-item"><i class="fas fa-user-edit"></i> Edit Details</a>
	<a href="send_files.php" class="list-group-item"><i class="fas fa-share-square"></i> Send Files</a>
	<a href="key_request.php" class="list-group-item"><i class="fas fa-key"></i> Key Request</a>
	<a href="users_list.php" class="list-group-item">Sent Files(by me)</a>
  <a href="user_request.php" class="list-group-item">User Registeration Request</a>
  <a href="leakers.php" class="list-group-item">Leaker</a>
  <a href="distributor_files.php" class="list-group-item"><i class="fas fa-file"></i> Files(Send By Another)</a>
</div>


ADMIN_MENUBAR.PHP
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="../index.php">Data Leakage</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <?php 
           if($_SESSION['usertype']=="admin"){
            echo "
<li class='nav-item active'>
        <a class='nav-link' href='admin_dashboard.php'>Home</a>
      </li>
            ";
           }
      ?>
                        
    </ul>
    
    <ul class="navbar-nav">      
      <li class="nav-item">
        <a class="nav-link" href="../main/logout.php">Logout</a>
      </li>                                    
    </ul>
  </div>
</nav>


USERS_LIST.PHP

<?php
session_start();
if($_SESSION['usertype']=="user"){

}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>User Dashboard- Users List(Sent Files)</title>
	<?php
require_once("../include.php");
	 ?>
</head>
<body>
	<?php
require_once("../user_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
			<div class="col-sm-3">

				<?php
require_once("../user_side_menubar.php");
				 ?>
			</div>
			<div class="col-sm-9">
				<?php
                   require_once("../function/distributor_model.php");
                   users_send_list();
				?>
			</div>
	 </div>
	</div>

</body>
</html>


USER_DASHBOARD.PHP

<?php
session_start();
if($_SESSION['usertype']=="user"){

}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>User Dashboard</title>
	<?php
require_once("../include.php");
	 ?>
</head>
<body>

	<?php
require_once("../user_menubar.php");
	 ?>

	 <div class="container-fluid">
        <div class="col-sm-3">
        	<?php
        		require_once("../user_side_menubar.php");
        	?>
        </div>
        <div class="col-sm-9"></div>
	 </div>

</body>
</html>


SEND_FILES.PHP

<?php
session_start();
if($_SESSION['usertype']=="user"){

}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>User Dashboard- Send Files</title>
	<?php
require_once("../include.php");
	 ?>
</head>
<body>
	<?php
require_once("../user_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
			<div class="col-sm-3">

				<?php


require_once("../user_side_menubar.php");



				 ?>
			</div>
			<div class="col-sm-9 shadow-sm p-5 mt-5 bg-white">
				<br>
				<center><h2>Send Files to Selected user</h2></center>
<?php
require_once("../function/distributor_model.php");
     if(isset($_POST['send_file'])){
     	$userid=$_POST['userid'];
     	$senderid=$_SESSION['userid'];
     	$subject=$_POST['subject'];

     	$filename=$_FILES['file']['name'];
     	$file_tmpname=$_FILES['file']['tmp_name'];
     	$filesize=$_FILES['file']['size']/(1024*1024);
     	$url="../files/$filename";
$data="";

if(!empty($subject) && !empty($filename) && !empty($userid))
{
     	if($filesize>10){
$data.="
<div class='alert alert-warning'>
<strong>Failed:</strong>
File size must be less than 10 mb.
</div>
";
     	}
     	else{
     		$secretkey=mt_rand(1000,9999);
    send_files($subject,$filename,$filesize,$senderid,$userid,$secretkey,$url,$file_tmpname);
     	}
}
else{
	$data.="
<div class='alert alert-warning'>
<strong>Failed:</strong>
Fill up data
</div>
	";
}
echo $data;
     }
 ?>


				<form action="send_files.php" method="post" enctype="multipart/form-data">
						<div class="form-group">
								<label for="user">Select User</label>
<?php get_user();?>
						</div>


						<div class="form-group">
								<label for="subject">Subject</label>
								<input type="text" name="subject" class="form-control">
						</div>

						<div class="form-group">
							<label for="file">File</label>
							<input type="file" name="file" class="form-control">
						</div>

						<div class="form-group">
							<center><input type="submit" name="send_file" value="Send" class="my-2 btn btn-primary"></center>
						</div>
				</form>


			</div>
	 </div>
	</div>

</body>
</html>



LEAKAGE_FILES.PHP FOR USER



<?php 
session_start();
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>User Dashboard- Leakage Files</title>
	<?php 
require_once("../include.php");
	 ?>
</head>
<body>

	<?php 
require_once("../user_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
        <div class="col-sm-3">
        	<?php 
        		require_once("../user_side_menubar.php");
        	?>
        </div>
        <div class="col-sm-6">
        	
             <?php 
             require_once("../function/user_model.php");
             leakage_file();
             ?>

        </div>
        <div class="col-sm-3"></div>
	 </div>
	</div>

</body>
</html>


KEY_REQUEST.PHP FOR USER


<?php
session_start();
if($_SESSION['usertype']=="user"){

}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>User Dashboard- Key Request</title>
	<?php
require_once("../include.php");
	 ?>
</head>
<body>
	<?php
require_once("../user_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
			<div class="col-sm-3">

				<?php
require_once("../user_side_menubar.php");
				 ?>
			</div>
			<div class="col-sm-9">
				<?php
require_once("../function/distributor_model.php");

 if(isset($_POST['share_key'])){
 	$fileid=$_POST['fileid'];
 	     share_key($fileid);
 }

 if(isset($_POST['decline'])){
     $fileid=$_POST["fileid"];
     $requestby=$_POST["requestby"];
     decline($fileid,$requestby);
 }
key_request();

				 ?>

			</div>
	 </div>
	</div>

</body>
</html>



DISTRIBUTORS FILES

<?php
session_start();
if($_SESSION['usertype']=="user"){

}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>User Dashboard- Distributor Files (Send By)</title>
	<?php
require_once("../include.php");
	 ?>
</head>
<body>

	<?php
require_once("../user_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
        <div class="col-sm-3">
        	<?php
        		require_once("../user_side_menubar.php");
        	?>
        </div>
        <div class="col-sm-9">
        	<br>
    	<center><h3>User Dashboard/Distributor Files (Send By)</h3></center>
	<?php
	require_once("../function/user_model.php");

if(isset($_POST['send_request'])){
       $requestby=$_POST['requestby'];
       $requestto=$_POST['requestto'];
       $fileid=$_POST['fileid'];
       $askkey=$_POST['askkey'];
       $request_label=$_POST['request_label'];
       $date_time=date("Y-m-d H:i:s");
       send_request($requestby,$requestto,$fileid,$askkey,$request_label,$date_time);
}

if(isset($_POST['share'])){
	$fileid=$_POST['fileid'];
	$userid=$_POST['userid'];
	$secretkey=$_POST['secretkey'];
	$subject=$_POST['subject'];
	$date_time=date("Y-m-d H:i:s");
	share_file($userid,$subject,$fileid,$secretkey,$date_time);
}


if(isset($_POST['share_others'])){
    $userid=$_POST["userid"];
    $fileid=$_POST["fileid"];
    if(!empty($userid)){
    share_with_others($userid,$fileid);
    }
    else{
        echo "<div class='alert alert-danger'>please select user</div>";
    }
}

	$userid=$_SESSION['userid'];
	get_distributor_send_files($userid);
?>
        </div>
	 </div>
	</div>

</body>
</html>


STARTER.SQL

INSERT INTO user(username,email,password,usertype,admin_active,date_time)VALUES
				("admin","admin@gmail.com","12345","admin","1","2019-01-02");

SETUP.SQL

/*

user:

userid
username
email
password
usertype  admin, user , distributor
admin_active
date_time

data_file:

fileid
subject
filename
filesize
senderid (sender)
userid  (receiver)
secretkey (key to download file)
date_time

request:

requestid
requestby (userid)
requestto (senderid which send files)
fileid (for which secret key ask)
askkey
request_label (1- request send, 2- request confirm)
date_time


leaker:


leakerid
userid (user which will leak a file)
subject
fileid 
secretkey
date_time

*/

CREATE TABLE IF NOT EXISTS user(
userid INT(10) AUTO_INCREMENT PRIMARY KEY,
username VARCHAR(255) NOT NULL,
email VARCHAR(255) NOT NULL,
password VARCHAR(255) NOT NULL,
usertype VARCHAR(255) DEFAULT 'user',
admin_active VARCHAR(255) DEFAULT '0',
date_time DATETIME NOT NULL
);

CREATE TABLE IF NOT EXISTS data_file(
fileid INT(10) AUTO_INCREMENT PRIMARY KEY,
subject VARCHAR(255) NOT NULL,
filename VARCHAR(255) NOT NULL,
filesize VARCHAR(255) NOT NULL,
senderid VARCHAR(255) NOT NULL,
userid  VARCHAR(255) NOT NULL,
secretkey VARCHAR(255) NOT NULL,
date_time DATETIME NOT NULL
);

CREATE TABLE IF NOT EXISTS request(
requestid INT(10) AUTO_INCREMENT PRIMARY KEY,
requestby VARCHAR(255) NOT NULL,
requestto VARCHAR(255) NOT NULL,
fileid VARCHAR(255) NOT NULL,
askkey VARCHAR(255) NOT NULL,
request_label VARCHAR(255) DEFAULT '0',
date_time DATETIME NOT NULL
);

CREATE TABLE IF NOT EXISTS leaker(
leakerid INT(10) AUTO_INCREMENT PRIMARY KEY,
userid VARCHAR(255) NOT NULL,
subject VARCHAR(255) NOT NULL,
fileid VARCHAR(255) NOT NULL,
secretkey VARCHAR(255) NOT NULL,
date_time DATETIME NOT NULL
);


REGISTER.PHP

<!DOCTYPE html>
<html>
<head>
	<title>Register</title>
	<?php require_once("../include.php");?>
</head>
<body class="front-background">
	<?php require_once("../nonactive_menubar.php");?>

<div class="container">
		<div class="row">
				<div class="col-sm-4"></div>
				<div class="col-sm-4 shadow p-5 mt-5 bg-white">

<?php
require_once("../function/model.php");
if(isset($_POST['register'])){
	$username=$_POST['username'];
	$email=$_POST['email'];
	$password=$_POST['password'];
	$cpassword=$_POST['cpassword'];
	$data="<br>";
	if(!empty($username) && !empty($email) && !empty($password) && !empty($cpassword)){
		if($password==$cpassword){
           register($username,$email,$password);
		}
		else{
			$data.="
				<div class='alert alert-danger'>
  <strong>Failed:</strong>
  Password and confirm password are not matched.
</div>
			";
		}
	}
	else{
$data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
  Please fill up data.
</div>
";
	}
	echo $data;
}

 ?>


					<form action="register.php" method="post">
							<div class="form-group">
									<label for="username">User Name</label>
									<input type="text" name="username" class="form-control">
							</div>

							<div class="form-group">
									<label for="email">Email Id</label>
									<input type="text" name="email" class="form-control">
							</div>

							<div class="form-group">
									<label for="password">Password</label>
									<input type="text" name="password" class="form-control">
							</div>

							<div class="form-group">
									<label for="cpassword">Confirm Password</label>
									<input type="text" name="cpassword" class="form-control">
							</div>

							<div class="form-group text-center">
									<input type="submit" name="register" value="Sign Up" class="btn btn-primary my-1">
							</div>
					</form>

				</div>
				<div class="col-sm-4"></div>
		</div>
</div>

</body>
</html>


PROCESS.PHP


<?php 
session_start();
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>User Dashboard</title>
	<?php 
require_once("../include.php");
	 ?>
</head>
<body>

	<?php 
require_once("../user_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
        <div class="col-sm-3">
        	
        </div>
        <div class="col-sm-6"><br>
	
	<?php 
	require_once("../function/user_model.php");
                 if(isset($_POST['download'])){
                 	$data="<br>";
$fileid=$_POST['fileid'];
$secretkey=$_POST['secretkey'];
  if(!empty($fileid) && !empty($secretkey)){
              $x=proceed_download($fileid,$secretkey);

  }
  else{
  	 $data.="<div class='alert alert-danger'>
  	 <strong>Failed:</strong>
  	 Fill up data
</div>
  	 ";
  }
  echo $data;
                 }
	 ?>

	 <form action="process.php?fileid=<?php echo $_GET['fileid'];?>" method="post">
	 	<div class="form-group">
				<label for="secretkey">Enter Secret key to download File</label>
				<input type='hidden' name='fileid' value="<?php if(isset($_GET['fileid'])){echo $_GET['fileid'];}?>">
				<input type="text" name="secretkey" value="" class="form-control">
	 	</div>

	 	<div class="form-group">
	 		<input type="submit" name="download" value='Download' class='btn btn-primary'>
	 	</div>
	 </form>

        </div>
        <div class="col-sm-3"></div>
	 </div>
	</div>

</body>
</html>


LOGOUT.PHP
<?php 
session_start();
session_destroy();
$url="../index.php";
header("Location:$url");
exit();
 ?>

LOGIN.PHP

<!DOCTYPE html>
<html>
<head>
	<title>Login</title>
	<?php require_once("../include.php");?>
</head>
<body class="front-background">
	<?php require_once("../nonactive_menubar.php");?>

<div class="container">
		<div class="row">
				<div class="col-sm-4"></div>
				<div class="col-sm-4 shadow-sm p-5 mt-5 bg-white">

<?php
require_once("../function/model.php");
if(isset($_POST['login'])){
  $email=$_POST['email'];
  $password=$_POST['password'];
  $data="<br>";

  if(!empty($email) && !empty($password)){
           login($email,$password);
}
else{
	$data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
  Please fill up data
</div>
	";
}

  echo $data;
}
?>


					<form action="login.php" method="post">


							<div class="form-group">
									<label for="email">Email Id</label>
									<input type="text" name="email" class="form-control">
							</div>

							<div class="form-group">
									<label for="password">Password</label>
									<input type="text" name="password" class="form-control">
							</div>


							<div class="form-group">
		<center>
			<input type="submit" name="login" value="Sign In" class="btn btn-primary my-1">
									</center>

									<a href="forget.php">Forget Password?</a>

							</div>
					</form>
					<br>

					<div class="card">
								<div class="card-body">
<i><b>Note:</b> Password may be changed, try to forget password using given email id below.</i><hr color="red">

						Admin:  <br>
						email: admin@gmail.com  <br>
						password: 12345 <hr color="red">

						Distributor: <br>
						email: distributor@gmail.com <br>
						password: 12345 <hr color="red">

						User: <br>
						<strong>user1</strong><br>
						email: user1@gmail.com <br>
						password: 12345 <br>

						<strong>user2</strong><br>
						email: user2@gmail.com <br>
						password: 12345
					</div></div>

				</div>
				<div class="col-sm-4"></div>
		</div>
</div>

</body>
</html>


FORGET.PHP
<!DOCTYPE html>
<html>
<head>
	<title>Forget Password</title>
	<?php require_once("../include.php");?>
</head>
<body>
	<?php require_once("../nonactive_menubar.php");?>

<div class="container">
		<div class="row">
				<div class="col-sm-4"></div>
				<div class="col-sm-4 shadow-sm p-5 mt-5 bg-white">

<?php
require_once("../function/model.php");
if(isset($_POST['forget'])){
  $email=$_POST['email'];
  $data="<br>";

  if(!empty($email)){
           forget_password($email);
}
else{
	$data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
  Please fill up data
</div>
	";
}

  echo $data;
}
?>

					<br>
					<form action="forget.php" method="post">


							<div class="form-group">
									<label for="email">Email Id</label>
									<input type="text" name="email" class="form-control">
							</div>


							<div class="form-group">
		<center>
			<input type="submit" name="forget" value="Recover Password" class="btn btn-primary my-2">
									</center>



							</div>
					</form>
					<br>

				</div>
				<div class="col-sm-4"></div>
		</div>
</div>

</body>
</html>
EDIT_PROFILE.PHP

<?php
 session_start();
?>
<!DOCTYPE html>
<html>
<head>
	<title>Edit Profile</title>
	<?php require_once("../include.php");?>
</head>
<body>
	<?php require_once("../nonactive_menubar.php");?>

<div class="container">
		<div class="row">
				<div class="col-sm-4"></div>
				<div class="col-sm-4 shadow-sm p-5 mt-5 bg-white">

<?php
require_once("../function/model.php");

if(isset($_POST['edit_profile'])){
		$userid=$_POST['userid'];
		$username=$_POST['username'];
		$password=$_POST['password'];
		$cpassword=$_POST['cpassword'];
		$data="<br>";
		if(!empty($username) && !empty($password) && !empty($cpassword)){
           if($password ==$cpassword){
                   save_changes($userid,$username,$password);
           }
           else{
$data.="<div class='alert alert-danger'>
<strong>Failed:</strong>
Password and confirm password are not same.
</div>
";
           }
		}
		else{
$data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
  Fill up data.
</div>
";
		}
		echo $data;
}

        get_profile($_SESSION['userid']);
        ?>




				</div>
				<div class="col-sm-4"></div>
		</div>
</div>

</body>
</html>


DOWNLOAD.PHP
<?php
$filename = $_GET["file"];
$contenttype = "application/force-download";
header("Content-Type: " . $contenttype);
header("Content-Disposition: attachment; filename=\"" .$filename. "\";");
readfile("../files/".$filename);
exit();
?>


USER_MODEL.PHP


<?php
require_once("../function/connect.php");
$conn=connect();

function get_distributor_send_files($userid){
	$data="<br>";
	global $conn;
	$sql="SELECT * FROM data_file WHERE userid='$userid' ORDER BY fileid DESC";
	$result=mysqli_query($conn,$sql);
	if($result){
				if(mysqli_num_rows($result)>0){
$n=0;
               while($rows=mysqli_fetch_array($result)){
               	$n++;
                      $fileid=$rows['fileid'];
                      $subject=$rows['subject'];
                      $filename=$rows['filename'];
                      $filesize=$rows['filesize'];
                      $senderid=$rows['senderid'];
                      $userid=$rows['userid'];
                      $secretkey=$rows['secretkey'];
                      $date_time=$rows['date_time'];


$secretdata=check_request($fileid,$userid,$senderid,$secretkey);
$sendername=getsendername($senderid);


$users_list=users_list($senderid);

$data.="
<div class='card my-3'>
  <div class='card-body'>
    <h4 class='card-title'>Sender: $sendername</h4>
    <p class='card-text'>Subject:$subject | File Name: $filename | File Size: $filesize</p>
    <a href='#' class='card-link text-decoration-none'>$secretdata</a>
    <a href='#' class='card-link text-decoration-none'>$date_time</a> <hr>
    <form action='distributor_files.php' method='post'>
    <input type='hidden' name='fileid' value='$fileid'>
                        <p>
                                <label for='users'>Select users</label>
                                $users_list
                        </p>
                <p>
                    <input type='submit' name='share_others' value='Share'>
                </p>
    </form>
  </div>
</div>
";
               }

$data.="<hr>";

				}
				else{
					$data.="
					<div class='alert alert-danger'>
						<strong>Failed:</strong>
						No file found
					</div>
					";
				}
	}
	else{
		$error=mysqli_error($conn);
		$data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
		";
	}
	echo $data;
}


function users_list($senderid){
    $data="";
    global $conn;
    $myid=$_SESSION['userid'];
    $sql="SELECT * FROM user WHERE userid!='$myid' AND userid!='$senderid'";
    $result=mysqli_query($conn,$sql);
    if($result){
        $data.="<select name='userid'><option></option>";
                while($rows=mysqli_fetch_array($result)){
                    $userid=$rows["userid"];
                    $username=$rows["username"];
                    $data.="<option value='$userid'>$username</option>";
                }
                $data.="</select>";
    }
    else{

    }

    return $data;
}


function share_others($fileid,$userid){
    $data="asdfasdf";

    $filedata=get_file_data($fileid);

    $subject=$filedata["subject"];
    $filename=$filedata["filename"];
    $filesize=$filedata["filesize"];
    $senderid=$filedata["senderid"];
    $userid=$_SESSION["userid"];
    $secretkey=$filedata["secretkey"];

    $data.="$secretkey";


    echo $data;
}

function get_file_data($fileid){
    $data="";
    global $conn;
    $sql="SELECT * FROM data_file WHERE fileid='$fileid'";
    $result=mysqli_query($conn,$sql);
    if($result){
         $rows=mysqli_fetch_array($result);
         $data=$rows;
    }
    else{

    }
    return $data;
}



function check_request($fileid,$userid,$senderid,$secretkey){
	$data="";
		global $conn;
$sql="SELECT * FROM request WHERE fileid='$fileid' AND requestby='$userid' AND requestto='$senderid'";
$result=mysqli_query($conn,$sql);
if($result){
         if(mysqli_num_rows($result)>0){
                      while($rows=mysqli_fetch_array($result)){
                      	$request_label=$rows['request_label'];
                        $askkey=$rows['askkey'];
                      	if($request_label=="0"){
                    $data.="
					<form action='distributor_files.php' method='post'>
					<input type='hidden' name='requestby' value='$userid'>
					<input type='hidden' name='requestto' value='$senderid'>
					<input type='hidden' name='fileid' value='$fileid'>
					<input type='hidden' name='askkey' value='$secretkey'>
					<input type='hidden' name='request_label' value='1'>
					<input type='submit' name='send_request' value='Send Request' class='btn btn-primary btn-sm'>
					</form>
					<hr/>
					<a href='../main/process.php?fileid=$fileid'>
                    <button class='btn btn-primary btn-sm'>Proceed to Download=></button></a>
                          ";
                      	}
                      	else if($request_label=="1"){
                    $data.="<button type='button' class='btn btn-warning btn-sm'>Pending</button>
                                <hr/>
                            <a href='../main/process.php?fileid=$fileid'>
                             <button class='btn btn-primary btn-sm'>Proceed to Download=></button></a>
                          ";
                      	}
                      	else if($request_label==="2"){
                          $data.="
                          <button type='button' class='btn btn-success btn-sm'>Key Received ($askkey)</button>
                                      <hr/>
                            <a href='../main/process.php?fileid=$fileid'>
                            <button class='btn btn-primary btn-sm'>Proceed to Download=></button></a>
                          ";
                      	}
                      	else if($request_label==="3"){
                          $data.="
                         <button class='btn btn-danger'> Cancelled</button>

                          ";
                      	}
                      }
         }
         else{
         	$data.="
					<form action='distributor_files.php' method='post'>
					<input type='hidden' name='requestby' value='$userid'>
					<input type='hidden' name='requestto' value='$senderid'>
					<input type='hidden' name='fileid' value='$fileid'>
					<input type='hidden' name='askkey' value='$secretkey'>
					<input type='hidden' name='request_label' value='1'>
					<input type='submit' name='send_request' value='Send Request' class='btn btn-primary btn-sm'>
					</form>
					<br>
                    <a href='../main/process.php?fileid=$fileid'>
                    <button class='btn btn-primary btn-sm'>Proceed to Download=></button></a>
         	";
         }
}
else{
	$error=mysqli_error($conn);
		$data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
		";
}


	return $data;
}





function getsendername($senderid){
	global $conn;
	$data="";
$sql="SELECT * FROM user WHERE userid='$senderid' LIMIT 1";
$result=mysqli_query($conn,$sql);
if($result){
   if(mysqli_num_rows($result)>0){
            while($rows=mysqli_fetch_array($result)){
            	$username=$rows['username'];
            	$data.="$username";
            }
   }
   else{
   	$data.="not found";
   }
}
else{
	$error=mysqli_error($conn);
		$data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
		";
	}
	return $data;
}


function send_request($requestby,$requestto,$fileid,$askkey,$request_label,$date_time){
       global $conn;
       $data="<br>";

       $sql="SELECT * FROM request WHERE fileid='$fileid' AND requestby='$requestby'";
       $result=mysqli_query($conn,$sql);
       if($result){
                 if(mysqli_num_rows($result)>0){
                      $data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
Request Already send.
</div>
  ";
                 }
                 else{
                        	$sql1="INSERT INTO request(requestby,requestto,fileid,askkey,request_label,date_time)VALUES(
'$requestby','$requestto','$fileid','$askkey','$request_label','$date_time'
       )";
       	$result1=mysqli_query($conn,$sql1);
       	if($result1){
  $data.="
<div class='alert alert-success'>
  <strong>Success:</strong>
Successfully secretkey request send.
</div>
  ";
       	}
       	else{
       		$error=mysqli_error($conn);
       		$data.="<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
       		";
       	}
                 }
       }
       else{
           	$error=mysqli_error($conn);
       		$data.="<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
       		";
       }




       echo $data;
}

function share_file($userid,$subject,$fileid,$secretkey,$date_time){
global $conn;
$data="<br>";
       	$sql1="INSERT INTO leaker(userid,subject,fileid,secretkey,date_time)VALUES(
		'$userid','$subject','$fileid','$secretkey','$date_time'
       )";
       	$result1=mysqli_query($conn,$sql1);
       	if($result1){
      $data.="
<div class='alert alert-success'>
  <strong>Success:</strong>
Successfully file shared.
</div>
  ";
       	}
       	else{
       		$error=mysqli_error($conn);
       		$data.="<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
       		";
       	}



echo $data;
}

function proceed_download($fileid,$secretkey){
global $conn;
$data="";
        $sql="SELECT * FROM data_file WHERE fileid='$fileid' AND secretkey='$secretkey' LIMIT 1";
        $result=mysqli_query($conn,$sql);
        if($result){

          if(mysqli_num_rows($result)>0){

                while($rows=mysqli_fetch_array($result)){
                  $filename=$rows['filename'];
                  $subject=$rows['subject'];
                  $userid=$_SESSION['userid'];
                  $date_time=date("Y-m-d H:i:s");
                  isleaker($userid,$subject,$fileid,$secretkey,$date_time);

                  $url="download.php?file=$filename";
                  header("Location:$url");
                  exit();


                }

          }
          else{
          $data.="<div class='alert alert-danger'>
  <strong>Failed:</strong>
  Invalid secret key.
</div>
          ";
          }

        }
        else{
          $error=mysqli_error($conn);
          $data.="<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
          ";
        }
echo  $data;
}


function isleaker($userid,$subject,$fileid,$secretkey,$date_time)
{
    global $conn;
    $data="";
    $sql="SELECT * FROM request WHERE fileid='$fileid' AND requestby='$userid'";
    $result=mysqli_query($conn,$sql);
    if($result){
         if(mysqli_num_rows($result)>0){

         }
         else{
             $sql2="SELECT * FROM leaker WHERE userid='$userid' AND fileid='$fileid' AND secretkey='$secretkey'";
             $result2=mysqli_query($conn,$sql2);
             if($result2){
                        if(mysqli_num_rows($result2)>0){

                        }
                        else{
                               $sql1="INSERT INTO leaker(userid,subject,fileid,secretkey,date_time)VALUES('$userid','$subject','$fileid','$secretkey','$date_time')";
             $result1=mysqli_query($conn,$sql1);
             if($result1){

             }
             else{
                  $error=mysqli_error($conn);
          $data.="<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
          ";
             }
                        }
             }
             else{
                   $error=mysqli_error($conn);
          $data.="<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
          ";
             }




         }
    }
    else{
         $error=mysqli_error($conn);
          $data.="<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
          ";
    }

echo $data;
}

function leakage_file(){
       $data="<br>";
       global $conn;
$sql="SELECT * FROM leaker ORDER BY leakerid DESC";
$result=mysqli_query($conn,$sql);
if($result){
     if(mysqli_num_rows($result)>0){

        $data.="<table class='table table-bordered'>
<thead>
   <tr>
        <th>Sr No</th>
        <th>File Details</th>
        <th>Download</th>
        <th>Shared By</th>
        <th>Date Time</th>
   </tr>
</thead>
        ";
$n=0;
        while($rows=mysqli_fetch_array($result)){
          $n++;
              $userid=$rows['userid'];
              $subject=$rows['subject'];
              $fileid=$rows['fileid'];
              $secretkey=$rows['secretkey'];
              $date_time=$rows['date_time'];
$user=getsendername($userid);
$file_detail=getfiledetail($fileid);
$download="<a href='../main/process.php?fileid=$fileid' class='white'>
<button type='button' class='btn btn-success'>
Download ($secretkey)
</a>";

          $data.="
              <tr>
                  <td>$n</td>
                  <td>$file_detail</td>
                  <td>$download</td>
                  <td>$user</td>
                  <td>$date_time</td>
              </tr>
          ";
        }

        $data.="</tbody></table>";

     }
     else{
          $data.="<div class='alert alert-danger'>
  <strong>Failed:</strong>
  Not found
</div>
          ";
     }
}
else{
  $error=mysqli_error($conn);
          $data.="<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
          ";
        }
       echo $data;
}


function getfiledetail($fileid){
global $conn;
  $data="";
$sql="SELECT * FROM data_file WHERE fileid='$fileid' LIMIT 1";
$result=mysqli_query($conn,$sql);
if($result){
   if(mysqli_num_rows($result)>0){
            while($rows=mysqli_fetch_array($result)){
               $subject=$rows['subject'];
               $filename=$rows['filename'];
               $f=$rows['filesize'];
               $filesize=round($rows['filesize'],2)."Mb";

               if($filesize==0){
                $filesize=round(($f*1024),3)."Kb";
               }
               $data.="
      <strong>Subject:</strong> $subject <br>
      <strong>File Name:</strong> $filename <br>
      <strong>File Size:</strong> $filesize
               ";
            }
   }
   else{
    $data.="not found";
   }
}
else{
  $error=mysqli_error($conn);
    $data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
    ";
  }
  return $data;
}


function share_with_others($userid,$fileid)
{
    $data="";
    global $conn;
    $filedata=filedata($fileid);

    $subject=$filedata["subject"];
    $filename=$filedata['filename'];
    $filesize=$filedata['filesize'];
    $senderid=$_SESSION['userid'];
    $user_id=$userid;
    $secretkey=$filedata["secretkey"];
    $date_time=date("Y-m-d H:i:s");
    $sql1="SELECT * FROM data_file WHERE userid='$user_id' AND senderid='$senderid'";
    $result1=mysqli_query($conn,$sql1);
    if($result1){
              if(mysqli_num_rows($result1)>0){
                  $data.="Already shared";
              }
              else{
                   $sql="INSERT INTO data_file(subject,filename,filesize,senderid,userid,secretkey,date_time)VALUES('$subject','$filename','$filesize','$senderid','$user_id','$secretkey','$date_time')";
    $result=mysqli_query($conn,$sql);
    if($result){
         echo "<div class='alert alert-primary'>Successfully shared</div>";
    }
    else{

    }
              }
    }
    else{

    }


    echo $data;
}


function filedata($fileid){
    $data="";
    global $conn;
    $sql="SELECT * FROM data_file WHERE fileid='$fileid' LIMIT 1";
    $result=mysqli_query($conn,$sql);
    if($result){
                if(mysqli_num_rows($result)>0){
                              $rows=mysqli_fetch_array($result);
                }
                $data=$rows;
    }
    else{

    }
    return $data;
}



 ?>



MODEL.PHP

<?php
require_once("connect.php");
$conn=connect();

function register($username,$email,$password){
	global $conn;
$data="<br>";

$sql="SELECT * FROM user WHERE email='$email'";
$result=mysqli_query($conn,$sql);
if($result){
       if(mysqli_num_rows($result)>0){
           $data.="
			<div class='alert alert-info'>
				<strong>Failed:</strong>
				This email id already exist.
			</div>
           ";
       }
       else{
               $date_time=date("Y-m-d");
       		$sql1="INSERT INTO user(username,email,password,date_time)VALUES('$username','$email','$password','$date_time')";
       		$result1=mysqli_query($conn,$sql1);
       		if($result1){
$data.="
<div class='alert alert-success'>
		<strong>Success:</strong>
		Successfully Registered.
</div>
";
       		}
       		else{
       				$data.="
<div class='alert alert-danger'>
		<strong>Failed:</strong>
		dberror
</div>
       				";
       		}

       }
}
else{
$data.="
<div class='alert alert-danger'>
		<strong>Failed:</strong>
		dberror
</div>
";
}
echo $data;
}

function login($email,$password){
	global $conn;
$data="<br>";

$sql="SELECT * FROM user WHERE email='$email' AND password='$password'";
$result=mysqli_query($conn,$sql);
if($result){
       if(mysqli_num_rows($result)>0){
                       while($rows=mysqli_fetch_array($result)){
                       	$userid=$rows['userid'];
                       	$username=$rows['username'];
                       	$usertype=$rows['usertype'];
                       	$admin_active=$rows['admin_active'];
if($admin_active=="0"){
	$data.="
<div class='alert alert-danger'>
		<strong>Failed:</strong>
		You registeration in review to admin. it will activated by admin very soon.
</div>
";
}
else if($admin_active=="1"){
	    session_start();
	    $_SESSION['usertype']=$usertype;
	    $_SESSION['userid']=$userid;
	    if($usertype=="user"){
	    		$url="../user/user_dashboard.php";
	    }
	    else if($usertype=="admin"){
$url="../admin/admin_dashboard.php";
	    }
	    else if($usertype=="distributor"){
	$url="../distributor/distributor_dashboard.php";
}
	    header("Location:$url");
	    exit();
}




                       }
       }
       else{
       	$data.="
<div class='alert alert-danger'>
		<strong>Failed:</strong>
		This email id not registered yet.
</div>
";
       }
}
else{
	$error=mysqli_error($conn);
$data.="
<div class='alert alert-danger'>
		<strong>Failed:</strong>
		dberror:$error
</div>
";
}
echo $data;
}

function forget_password($email){
	global $conn;
	$data="<br>";
$sql="SELECT * FROM user WHERE email='$email' LIMIT 1";
$result=mysqli_query($conn,$sql);
if($result){
   if(mysqli_num_rows($result)>0){

            while($rows=mysqli_fetch_array($result)){
            	$password=$rows['password'];
            	$data.="
<div class='alert alert-success'>
		<strong>Password Recovered Successfully:</strong>
		$password
</div>
            	";
            }
   }
   else{
$data.="
<div class='alert alert-info'>
		<strong>Failed:</strong>
		Invalid email id.
</div>
";
   }
}
else{
$error=mysqli_error($conn);
$data.="
<div class='alert alert-danger'>
		<strong>Failed:</strong>
		dberror:$error
</div>
";
}
echo $data;
}

function get_profile($userid){
	global $conn;
$data="<br>";

$sql="SELECT * FROM user WHERE userid='$userid' LIMIT 1";
$result=mysqli_query($conn,$sql);
if($result){
     if(mysqli_num_rows($result)>0){

        while($rows=mysqli_fetch_array($result)){
        	$userid=$rows['userid'];
        	$username=$rows['username'];
        	$password=$rows['password'];
        }

$data.="
<br>
 <center><h3>Edit Profile</h3></center>
<form action='edit_profile.php' method='post'>
  <div class='form-group'>
  <input type='hidden' name='userid' value='$userid'>
									<label for='username'>User Name</label>
		<input type='text' name='username' class='form-control' value='$username'>
							</div>

							<div class='form-group'>
									<label for='password'>Password</label>
				<input type='text' name='password' class='form-control' value='$password'>
							</div>

							<div class='form-group'>
									<label for='cpassword'>Confirm Password</label>
									<input type='text' name='cpassword' class='form-control'>
							</div>

							<div class='form-group'>
									<center><input type='submit' name='edit_profile' value='Save Changes' class='btn btn-primary my-3'></center>
							</div>
</form>
";



     }
     else{
$data.="
<div class='alert alert-danger'>
		<strong>Failed:</strong>
		No record found
</div>
";
     }
}
else{
 	$error=mysqli_error($conn);
$data.="
<div class='alert alert-danger'>
		<strong>Failed:</strong>
		dberror:$error
</div>
";
}
echo $data;
}


function save_changes($userid,$username,$password){
	 global $conn;
	 $data="<br>";
$sql="UPDATE user SET username='$username',password='$password' WHERE userid='$userid' LIMIT 1";
$result=mysqli_query($conn,$sql);
if($result){
       $data.="
<div class='alert alert-success'>
		<strong>Success:</strong>
		Successfully updated.
</div>
";
}
else{
	$error=mysqli_error($conn);
 $data.="
<div class='alert alert-danger'>
		<strong>Failed:</strong>
		dberror:$error
</div>
";
}
	 echo $data;
}


 ?>


DISTRIBUTOR_MODEL.PHP

<?php
require_once("../function/connect.php");
$conn=connect();


function send_files($subject,$filename,$filesize,$senderid,$userid,$secretkey,$url,$file_tmpname){

    $filename=md5(mt_rand(1,10000))."-".$filename;
    $url="../files/$filename";

$date_time=date("Y-m-d H:i:s");
global $conn;
$data="<br>";
$sql="INSERT INTO data_file(
subject,
filename,
filesize,
senderid,
userid,
secretkey,
date_time
)VALUES
(
  '$subject',
  '$filename',
  '$filesize',
  '$senderid',
  '$userid',
  '$secretkey',
  '$date_time'
)
";

$result=mysqli_query($conn,$sql);
if($result){

if(move_uploaded_file($file_tmpname,$url)){
$data.="
<div class='alert alert-success'>
 <strong>Success:</strong>
 File Successfully send.
</div>
";
}
else{
    $sql1="DELETE FROM send_files WHERE filename='$filename' AND userid='$userid' AND date_time='$date_time' LIMIT 1";
    $resutl1=mysqli_query($conn,$sql1);
    if($result1){
         $data.="
<div class='alert alert-success'>
 <strong>Failed:</strong>
 File upload failed:
</div>
";
    }
    else{
        	$error=mysqli_error($conn);
$data.="
<div class='alert alert-success'>
 <strong>Failed:</strong>
 dberror: $error
</div>
";
    }
}

}
else{
	$error=mysqli_error($conn);
$data.="
<div class='alert alert-success'>
 <strong>Failed:</strong>
 dberror: $error
</div>
";
}

echo $data;
}

function get_user(){
$data="";
global $conn;
$self=$_SESSION['userid'];
$sql="SELECT * FROM user WHERE admin_active='1' AND userid<>'$self' ORDER BY userid ASC";
$result=mysqli_query($conn,$sql);
if($result){
    if(mysqli_num_rows($result)>0){

           $data.="<select name='userid' class='form-control'>
					<option></option>
           ";

           	while($rows=mysqli_fetch_array($result)){
           		$userid=$rows['userid'];;
           		$username=$rows['username'];
           		$data.="<option value='$userid'>$username</option>";
           	}

           $data.="</select>";
    }
    else{
    $data.="
<div class='alert alert-danger'>
<strong>Failed:</strong>
not found
</div>
	";
    }
}
else{
	$error=mysqli_error($conn);
	$data.="
<div class='alert alert-danger'>
<strong>Failed:</strong>
dberror:$error
</div>
	";
}

echo $data;
}

function key_request(){
$data="<br>";
global $conn;
$self=$_SESSION['userid'];
$sql="SELECT * FROM request WHERE requestto='$self'";
$result=mysqli_query($conn,$sql);
if($result){
     if(mysqli_num_rows($result)>0){
           $data.="
<table class='table table-dark table-striped'>
<thead>
  <tr>
     <th>Sr No</th>
     <th>Request By</th>
     <th>File</th>
     <th>Confirm</th>
     <th>Date_time</th>
  </tr>
</thead>
<tbody>
           ";
$n=0;
        while($rows=mysqli_fetch_array($result)){
     $n++;
            $requestby=$rows['requestby'];
            $fileid=$rows['fileid'];
            $request_label=$rows['request_label'];
            $date_time=$rows['date_time'];

     $username=getusername($requestby);
     $file_detail=getfiledetail($fileid);

 if($request_label=="1"){
        $confirmdata="
         <form action='key_request.php' method='post'>
              <input type='hidden' name='fileid' value='$fileid'>
              <input type='submit' name='share_key' value='Share Key' class='btn btn-primary'>
         </form>
         <hr>
         <form action='key_request.php' method='post'>
              <input type='hidden' name='fileid' value='$fileid'>
              <input type='hidden' name='requestby' value='$requestby'>
              <input type='submit' name='decline' value='Decline' class='btn btn-primary'>
         </form>

        ";


 }
 else if($request_label=="2"){
  $confirmdata="Confirmed";
 }
 else if($request_label=="3"){
     $confirmdata="Canceled";
 }



          $data.="
<tr>
    <td>$n</td>
    <td>$username</td>
    <td>$file_detail</td>
    <td>$confirmdata</td>
    <td>$date_time</td>
 </tr>
          ";
        }


           $data.="</tbody></table>";
     }
     else{

  $data.="
<div class='alert alert-danger'>
<strong>Failed:</strong>
Not found any key request
</div>
  ";
     }
}
else{
 $error=mysqli_error($conn);
  $data.="
<div class='alert alert-danger'>
<strong>Failed:</strong>
dberror:$error
</div>
  ";
}
echo $data;
}


function getusername($userid){
    global $conn;
  $data="";
$sql="SELECT * FROM user WHERE userid='$userid' LIMIT 1";
$result=mysqli_query($conn,$sql);
if($result){
   if(mysqli_num_rows($result)>0){
            while($rows=mysqli_fetch_array($result)){
              $username=$rows['username'];
              $data.="$username";
            }
   }
   else{
    $data.="not found";
   }
}
else{
  $error=mysqli_error($conn);
    $data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
    ";
  }
  return $data;
}

function getfiledetail($fileid){
global $conn;
  $data="";
$sql="SELECT * FROM data_file WHERE fileid='$fileid' LIMIT 1";
$result=mysqli_query($conn,$sql);
if($result){
   if(mysqli_num_rows($result)>0){
            while($rows=mysqli_fetch_array($result)){
               $subject=$rows['subject'];
               $filename=$rows['filename'];
               $f=$rows['filesize'];
               $filesize=round($rows['filesize'],2)."Mb";

               if($filesize==0){
                $filesize=round(($f*1024),3)."Kb";
               }
               $data.="
      <strong>Subject:</strong> $subject <br>
      <strong>File Name:</strong> $filename <br>
      <strong>File Size:</strong> $filesize
               ";
            }
   }
   else{
    $data.="not found";
   }
}
else{
  $error=mysqli_error($conn);
    $data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
    ";
  }
  return $data;
}

function share_key($fileid){
  $data="<br>";
global $conn;

$sql="UPDATE request SET request_label='2' WHERE request_label='1' AND fileid='$fileid' LIMIT 1";
$result=mysqli_query($conn,$sql);
if($result){
    $data.="
<div class='alert alert-primary'>
  <strong>Success:</strong>
  Successfully share secretkey.
</div>
    ";
}
else{
       $error=mysqli_error($conn);
    $data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
    ";
}
  echo $data;
}


function users_send_list()
{
  global $conn;
  $data="<br>";
$self=$_SESSION['userid'];
$sql="SELECT * FROM data_file WHERE senderid='$self'";
$result=mysqli_query($conn,$sql);
if($result){
   if(mysqli_num_rows($result)>0){

$data.="<table class='table table-bordered'>
<thead>
 <tr>
    <th>Sr No</th>
    <th>Subject</th>
    <th>Filename</th>
    <th>filesize</th>
    <th>User</th>
    <th>Date Time</th>
 </tr>
</thead>
<tbody>
";
$n=0;
   while($rows=mysqli_fetch_array($result)){
$n++;
$subject=$rows['subject'];
$filename=$rows['filename'];
$filesize=$rows['filesize'];
$userid=$rows['userid'];
$date_time=$rows['date_time'];
$user=getusername($userid);
$data.="
<tr>
  <td>$n</td>
  <td>$subject</td>
  <td>$filename</td>
  <td>$filesize</td>
  <td>$user</td>
  <td>$date_time</td>
</tr>
";

   }


$data.="
</tbody>
</table>";

   }
   else{

    $data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
  No users found.
</div>
    ";
   }
}
else{
$error=mysqli_error($conn);
    $data.="
<div class='alert alert-danger'>
  <strong>Failed:</strong>
  dberror:$error
</div>
    ";
}
  echo $data;
}


function decline($fileid,$requestby)
{
    global $conn;
    $data="";

    $sql="UPDATE request SET request_label='3' WHERE fileid='$fileid' AND requestby='$requestby' LIMIT 1";
    $result=mysqli_query($conn,$sql);
    if($result){
        $data.="Decline successfully";
    }
    else{
        $data.="error:".mysqli_error($conn);
    }

    echo $data;
}

 ?>


CONNECT.PHP

<?php 
function connect(){
  $server="localhost";
  $user="dataleakage_user";
  $password="12345";
  $database="dataleakage";
  $conn=mysqli_connect($server,$user,$password,$database);
  if($conn){
  	return $conn;
  }
  else{
  	echo "connection error:";
  }
}
 ?>


ADMIN_MODEL.PHP
<?php 
require_once("connect.php");
$conn=connect();

function load_user_request(){
	$data="<br>";
global $conn;

$sql="SELECT * FROM user WHERE usertype='user' OR usertype='distributor' ORDER BY userid DESC";
$result=mysqli_query($conn,$sql);
if($result){
       if(mysqli_num_rows($result)>0){
       			$data.="
<table class='table table-bordered'>
<thead>
  <tr>
		<th>Sr No</th>
		<th>User Name</th>
		<th>Email Id</th>
		<th>Activate account</th>
		<th>Create Distributor</th>
  </tr>
</thead>
<tbody>
       			";
$i=0;
       				while($rows=mysqli_fetch_array($result)){
       					$i++;
       					$userid=$rows['userid'];
       					$username=$rows['username'];
       					$email=$rows['email'];
       					$admin_active=$rows['admin_active'];
       					$usertype=$rows['usertype'];

if($admin_active=="0"){
$admin="
<form action='user_request.php' method='post'>
		<input type='hidden' name='userid' value='$userid'>
		<input type='submit' name='activate' value='Activate' class='btn btn-success'>
</form>
";
}
else{
	$admin="
<form action='user_request.php' method='post'>
		<input type='hidden' name='userid' value='$userid'>
		<input type='submit' name='deactivate' value='Deactivate' class='btn btn-danger'>
</form>
	";
}


if($usertype=="user"){
$usertype="
<form action='user_request.php' method='post'>
		<input type='hidden' name='userid' value='$userid'>
<input type='submit' name='usertype_distributor' value='Make Distributor' class='btn btn-success'>
</form>
";
}
else{
	$usertype="
<form action='user_request.php' method='post'>
		<input type='hidden' name='userid' value='$userid'>
		<input type='submit' name='usertype_user' value='Make User' class='btn btn-danger'>
</form>
	";
}


$data.="
<tr>
<td>$i</td>
<td>$username</td>
<td>$email</td>
<td>$admin</td>
<td>$usertype</td>
</tr>
";


       				}

$data.="</tbody></table>";

       }
       else{
       	$data.="
<div class='alert alert-danger'>
<strong>Failed:</strong>No request found
</div>
       	";
       }
}
else{
	$data.="
<div class='alert alert-danger'>
<strong>Failed:</strong>dberror
</div>
	";
}

	echo $data;
}


function activate_user($userid,$action){
	$data="<br>";
	global $conn;
$sql="UPDATE user SET admin_active='1' WHERE admin_active='0' AND userid='$userid' LIMIT 1";
$result=mysqli_query($conn,$sql);
if($result){
   $data.="
<div class='alert alert-success'>
<strong>Success:</strong>Activate
</div>
	";
}
else{
	$data.="
<div class='alert alert-danger'>
<strong>Failed:</strong>dberror
</div>
	";
}
	echo $data;
}


function deactivate_user($userid,$action){
	$data="<br>";
	global $conn;
$sql="UPDATE user SET admin_active='0' WHERE admin_active='1' AND userid='$userid' LIMIT 1";
$result=mysqli_query($conn,$sql);
if($result){
   $data.="
<div class='alert alert-success'>
<strong>Success:</strong>Deactivate
</div>
	";
}
else{
	$data.="
<div class='alert alert-danger'>
<strong>Failed:</strong>dberror
</div>
	";
}
	echo $data;
}


function create_user($userid,$action){
	$data="<br>";
	global $conn;
$sql="UPDATE user SET usertype='user' WHERE userid='$userid' LIMIT 1";
$result=mysqli_query($conn,$sql);
if($result){
   $data.="
<div class='alert alert-success'>
<strong>Success:</strong> Updated to user
</div>
	";
}
else{
	$data.="
<div class='alert alert-danger'>
<strong>Failed:</strong>dberror
</div>
	";
}
	echo $data;
}


function create_distributor($userid,$action){
	$data="<br>";
	global $conn;
$sql="UPDATE user SET usertype='distributor' WHERE userid='$userid' LIMIT 1";
$result=mysqli_query($conn,$sql);
if($result){
   $data.="
<div class='alert alert-success'>
<strong>Success:</strong> Updated to distributor
</div>
	";
}
else{
	$data.="
<div class='alert alert-danger'>
<strong>Failed:</strong>dberror
</div>
	";
}
	echo $data;
}

 ?>



FOR DISTRIBUTOR


USERS_LIST.PHP
<?php 
session_start();
if($_SESSION['usertype']=="distributor"){
    
}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>Distributor Dashboard- Users List(Sent Files)</title>
	<?php 
require_once("../include.php");
	 ?>
</head>
<body>
	<?php 
require_once("../distributor_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
			<div class="col-sm-3">
				
				<?php 
require_once("../distributor_side_menubar.php");
				 ?>
			</div>
			<div class="col-sm-6">
				<?php 
                   require_once("../function/distributor_model.php");
                   users_send_list();
				?>
				
			</div>
			<div class="col-sm-3"></div>
	 </div>
	</div>

</body>
</html>


SEND_FILES.PHP

<?php
session_start();
if($_SESSION['usertype']=="distributor"){

}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>Distributor Dashboard- Send Files</title>
	<?php
require_once("../include.php");
	 ?>
</head>
<body>
	<?php
require_once("../distributor_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
			<div class="col-sm-3">

				<?php

 if($_SESSION['usertype']=="distributor"){
require_once("../distributor_side_menubar.php");
}


				 ?>
			</div>
			<div class="col-sm-6 bg-white shadow my-3 p-3">
				<br>
				<center><h2>Send Files to Selected user</h2></center>
<?php
require_once("../function/distributor_model.php");
     if(isset($_POST['send_file'])){
     	$userid=$_POST['userid'];
     	$senderid=$_SESSION['userid'];
     	$subject=$_POST['subject'];

     	$filename=$_FILES['file']['name'];
     	$file_tmpname=$_FILES['file']['tmp_name'];
     	$filesize=$_FILES['file']['size']/(1024*1024);
     	$url="../files/$filename";
$data="";

if(!empty($subject) && !empty($filename) && !empty($userid))
{
     	if($filesize>10){
$data.="
<div class='alert alert-warning'>
<strong>Failed:</strong>
File size must be less than 10 mb.
</div>
";
     	}
     	else{
     		$secretkey=mt_rand(1000,9999);
    send_files($subject,$filename,$filesize,$senderid,$userid,$secretkey,$url,$file_tmpname);
     	}
}
else{
	$data.="
<div class='alert alert-warning'>
<strong>Failed:</strong>
Fill up data
</div>
	";
}
echo $data;
     }
 ?>


				<form action="send_files.php" method="post" enctype="multipart/form-data">
						<div class="form-group">
								<label for="user">Select User</label>
<?php get_user();?>
						</div>


						<div class="form-group">
								<label for="subject">Subject</label>
								<input type="text" name="subject" class="form-control">
						</div>

						<div class="form-group">
							<label for="file">File</label>
							<input type="file" name="file" class="form-control">
						</div>

						<div class="form-group">
							<center><input type="submit" name="send_file" value="Send" class="my-1 btn btn-primary"></center>
						</div>
				</form>


			</div>
			<div class="col-sm-3"></div>
	 </div>
	</div>

</body>
</html>

LEAKERS.PHP
<?php 
session_start();
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>Distributor Dashboard-Leakers</title>
	<?php 
require_once("../include.php");
	 ?>
</head>
<body>
	<?php 
require_once("../distributor_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
			<div class="col-sm-3">
				
				<?php 
require_once("../distributor_side_menubar.php");
				 ?>
			</div>
			<div class="col-sm-6">
				<?php 
             require_once("../function/user_model.php");
             leakage_file();
             ?>
				
			</div>
			<div class="col-sm-3"></div>
	 </div>
	</div>

</body>
</html>


KEY_REQUEST.PHP


<?php 
session_start();
if($_SESSION['usertype']=="distributor"){
    
}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>Distributor Dashboard- Key Request</title>
	<?php 
require_once("../include.php");
	 ?>
</head>
<body>
	<?php 
require_once("../distributor_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
			<div class="col-sm-3">
				
				<?php 
require_once("../distributor_side_menubar.php");
				 ?>
			</div>
			<div class="col-sm-6">
				<?php 
require_once("../function/distributor_model.php");

 if(isset($_POST['share_key'])){
 	$fileid=$_POST['fileid'];
 	     share_key($fileid);
 }
if(isset($_POST['decline'])){
     $fileid=$_POST["fileid"];
     $requestby=$_POST["requestby"];
     decline($fileid,$requestby);
 }
key_request();

				 ?>
				
			</div>
			<div class="col-sm-3"></div>
	 </div>
	</div>

</body>
</html>

DISTRIBUTOR_FILES.PHP

<?php 
session_start();
if($_SESSION['usertype']=="distributor"){
    
}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>Distributor Dashboard- Files (Send By)</title>
	<?php 
require_once("../include.php");
	 ?>
</head>
<body>

	<?php 
require_once("../distributor_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
        <div class="col-sm-3">
        	<?php 
        		require_once("../distributor_side_menubar.php");
        	?>
        </div>
        <div class="col-sm-6">
        	<br>
    	<center><h3>Distributor/Files (Send By)</h3></center>    	
	<?php
	require_once("../function/user_model.php");

if(isset($_POST['send_request'])){
       $requestby=$_POST['requestby'];
       $requestto=$_POST['requestto'];
       $fileid=$_POST['fileid'];
       $askkey=$_POST['askkey'];
       $request_label=$_POST['request_label'];
       $date_time=date("Y-m-d H:i:s");
       send_request($requestby,$requestto,$fileid,$askkey,$request_label,$date_time);
}

if(isset($_POST['share'])){
	$fileid=$_POST['fileid'];
	$userid=$_POST['userid'];
	$secretkey=$_POST['secretkey'];
	$subject=$_POST['subject'];
	$date_time=date("Y-m-d H:i:s");
	share_file($userid,$subject,$fileid,$secretkey,$date_time);
}


if(isset($_POST['share_others'])){
    $userid=$_POST["userid"];
    $fileid=$_POST["fileid"];
    if(!empty($userid)){
    share_with_others($userid,$fileid);
    }
    else{
        echo "<div class='alert alert-danger'>please select user</div>";
    }
}


	$userid=$_SESSION['userid'];
	get_distributor_send_files($userid);
?>
        </div>
        <div class="col-sm-3"></div>
	 </div>
	</div>

</body>
</html>


DISTRIBUTOR_DASHBOARD.PHP


<?php 
session_start();
if($_SESSION['usertype']=="distributor"){
    
}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>Distributor Dashboard</title>
	<?php 
require_once("../include.php");
	 ?>
</head>
<body>
	<?php 
require_once("../distributor_menubar.php");
	 ?>

	 <div class="container-fluid">
			<div class="col-sm-3">
				
				<?php 
require_once("../distributor_side_menubar.php");
				 ?>
			</div>
			<div class="col-sm-6">
				
				
			</div>
			<div class="col-sm-3"></div>
	 </div>

</body>
</html>



FOR ADMIN

USERS_LIST.PHP
<?php 
session_start();
if($_SESSION['usertype']=="admin"){
    
}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>Admin Dashboard- Users List(Sent Files)</title>
	<?php 
require_once("../include.php");
	 ?>
</head>
<body>
	<?php 
require_once("../admin_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
			<div class="col-sm-3">
				
				<?php 
require_once("../admin_side_menubar.php");
				 ?>
			</div>
			<div class="col-sm-6">
				<?php 
                   require_once("../function/distributor_model.php");
                   users_send_list();
				?>
				
			</div>
			<div class="col-sm-3"></div>
	 </div>
	</div>

</body>
</html>


USER_REQUEST.PHP

<?php 
session_start();
if($_SESSION['usertype']=="admin"){
    
}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>Admin Dashboard- User Request</title>
	<?php require_once("../include.php");?>
</head>
<body>
	<?php require_once("../admin_menubar.php");?>

	<div class="container-fluid">
			<div class="row">
					<div class="col-sm-3">
						<?php 
							require_once("../admin_side_menubar.php");
						?>
					</div>
					<div class="col-sm-6">
						  <?php 
										require_once("../function/admin_model.php");

  if(isset($_POST['activate'])){
  $userid=$_POST['userid'];
  $action="activate";
     activate_user($userid,$action);
}
else if(isset($_POST['deactivate'])){
	  $userid=$_POST['userid'];
	  $action="deactivate";
	  deactivate_user($userid,$action);
}


  if(isset($_POST['usertype_user'])){
  $userid=$_POST['userid'];
  $action="user";
     create_user($userid,$action);
}
else if(isset($_POST['usertype_distributor'])){
	  $userid=$_POST['userid'];
	  $action="distributor";
	  create_distributor($userid,$action);
}

										load_user_request();
						  ?>

					</div>
					<div class="col-sm-3"></div>
			</div>
	</div>

</body>
</html>


SEND_FILES.PHP

<?php
session_start();
if($_SESSION['usertype']=="admin"){

}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>Distributor Dashboard- Send Files</title>
	<?php
require_once("../include.php");
	 ?>
</head>
<body>
	<?php
require_once("../distributor_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
			<div class="col-sm-3">

				<?php


require_once("../admin_side_menubar.php");



				 ?>
			</div>
			<div class="col-sm-6 shadow p-5 bg-white my-3">
				<br>
				<center><h2>Send Files to Selected user</h2></center>
<?php
require_once("../function/distributor_model.php");
     if(isset($_POST['send_file'])){
     	$userid=$_POST['userid'];
     	$senderid=$_SESSION['userid'];
     	$subject=$_POST['subject'];

     	$filename=$_FILES['file']['name'];
     	$file_tmpname=$_FILES['file']['tmp_name'];
     	$filesize=$_FILES['file']['size']/(1024*1024);
     	$url="../files/$filename";
$data="";

if(!empty($subject) && !empty($filename) && !empty($userid))
{
     	if($filesize>10){
$data.="
<div class='alert alert-warning'>
<strong>Failed:</strong>
File size must be less than 10 mb.
</div>
";
     	}
     	else{
     		$secretkey=mt_rand(1000,9999);
    send_files($subject,$filename,$filesize,$senderid,$userid,$secretkey,$url,$file_tmpname);
     	}
}
else{
	$data.="
<div class='alert alert-warning'>
<strong>Failed:</strong>
Fill up data
</div>
	";
}
echo $data;
     }
 ?>


				<form action="send_files.php" method="post" enctype="multipart/form-data">
						<div class="form-group">
								<label for="user">Select User</label>
<?php get_user();?>
						</div>


						<div class="form-group">
								<label for="subject">Subject</label>
								<input type="text" name="subject" class="form-control">
						</div>

						<div class="form-group">
							<label for="file">File</label>
							<input type="file" name="file" class="form-control">
						</div>

						<div class="form-group">
							<center><input type="submit" name="send_file" value="Send" class="btn btn-primary"></center>
						</div>
				</form>


			</div>
			<div class="col-sm-3"></div>
	 </div>
	</div>

</body>
</html>

LEAKERS.PHP

<?php 
session_start();
if($_SESSION['usertype']=="admin"){
    
}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>Admin Dashboard-Leakers</title>
	<?php 
require_once("../include.php");
	 ?>
</head>
<body>
	<?php 
require_once("../admin_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
			<div class="col-sm-3">
				
				<?php 
require_once("../admin_side_menubar.php");
				 ?>
			</div>
			<div class="col-sm-6">
				<?php 
             require_once("../function/user_model.php");
             leakage_file();
             ?>
				
			</div>
			<div class="col-sm-3"></div>
	 </div>
	</div>

</body>
</html>


KEY_REQUEST.PHP

<?php 
session_start();
if($_SESSION['usertype']=="admin"){
    
}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>Admin Dashboard- Key Request</title>
	<?php 
require_once("../include.php");
	 ?>
</head>
<body>
	<?php 
require_once("../admin_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
			<div class="col-sm-3">
				
				<?php 
require_once("../admin_side_menubar.php");
				 ?>
			</div>
			<div class="col-sm-6">
				<?php 
require_once("../function/distributor_model.php");

 if(isset($_POST['share_key'])){
 	$fileid=$_POST['fileid'];
 	     share_key($fileid);
 }
 
 if(isset($_POST['decline'])){
     $fileid=$_POST["fileid"];
     $requestby=$_POST["requestby"];
     decline($fileid,$requestby);
 }
 

key_request();

				 ?>
				
			</div>
			<div class="col-sm-3"></div>
	 </div>
	</div>

</body>
</html>


DISTRIBUTOR_FILES.PHP

<?php 
session_start();
if($_SESSION['usertype']=="admin"){
    
}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>Admin Dashboard- Distributor Files (Send By)</title>
	<?php 
require_once("../include.php");
	 ?>
</head>
<body>

	<?php 
require_once("../admin_menubar.php");
	 ?>

	 <div class="container-fluid">
	 	<div class="row">
        <div class="col-sm-3">
        	<?php 
        		require_once("../admin_side_menubar.php");
        	?>
        </div>
        <div class="col-sm-6">
        	<br>
    	<center><h3>Admin Dashboard/ Files (Send By)</h3></center>    	
	<?php
	require_once("../function/user_model.php");

if(isset($_POST['send_request'])){
       $requestby=$_POST['requestby'];
       $requestto=$_POST['requestto'];
       $fileid=$_POST['fileid'];
       $askkey=$_POST['askkey'];
       $request_label=$_POST['request_label'];
       $date_time=date("Y-m-d H:i:s");
       send_request($requestby,$requestto,$fileid,$askkey,$request_label,$date_time);
}

if(isset($_POST['share'])){
	$fileid=$_POST['fileid'];
	$userid=$_POST['userid'];
	$secretkey=$_POST['secretkey'];
	$subject=$_POST['subject'];
	$date_time=date("Y-m-d H:i:s");
	share_file($userid,$subject,$fileid,$secretkey,$date_time);
}

if(isset($_POST['share_others'])){
    $userid=$_POST["userid"];
    $fileid=$_POST["fileid"];
    if(!empty($userid)){
    share_with_others($userid,$fileid);
    }
    else{
        echo "<div class='alert alert-danger'>please select user</div>";
    }
}

	$userid=$_SESSION['userid'];
	get_distributor_send_files($userid);
?>
        </div>
        <div class="col-sm-3"></div>
	 </div>
	</div>

</body>
</html>


ADMIN_DASHBOARD.PHP

<?php 
session_start();
if($_SESSION['usertype']=="admin"){
    
}
else{
    $url="../index.php";
    header("Location:$url");
    exit();
}
 ?>
<!DOCTYPE html>
<html>
<head>
	<title>Admin Dashboard</title>
	<?php require_once("../include.php");?>
</head>
<body>
	<?php require_once("../admin_menubar.php");?>

	<div class="container-fluid">
			<div class="row">
					<div class="col-sm-3">
						<?php 
							require_once("../admin_side_menubar.php");
						?>
					</div>
					<div class="col-sm-6">
						

					</div>
					<div class="col-sm-3"></div>
			</div>
	</div>

</body>
</html>

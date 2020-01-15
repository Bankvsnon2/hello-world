<!DOCTYPE html>
<html>
<head>
	<title>ThaiCreate.Com Tutorial</title>
</head>
<body>
<table align="center" width="762">
<tr>
<td>
<?php
error_reporting(~E_NOTICE);
if($_GET["Action"] == "Save")
{
// Statement
}
$skg = $_POST['name_txt'] ;
$rpg = $_POST['chk1'] ;
$rpg2 = $_POST['chk2'] ;
$rpg3 = $_POST['chk3'] ;
$rpg4 = $_POST['chk4'] ;
$rpg5 = $_POST['chk5'] ;
$rpg6 = $_POST['chk6'] ;
$rpg7 = $_POST['chk7'] ;
$rpg8 = $_POST['chk8'] ;
$rpg9 = $_POST['chk9'] ;
$rpg10 = $_POST['chk10'] ;
$rpg11 = $_POST['chk11'] ;
$rpg12 = $_POST['chk12'] ;
$rpg13 = $_POST['chk13'] ;
$rpg14 = $_POST['chk14'] ;
$rpg15 = $_POST['chk15'] ;
$rpg16 = $_POST['chk16'] ;
$rpg17 = $_POST['chk17'] ;
$rpg18 = $_POST['chk18'] ;
$rpg19 = $_POST['chk19'] ;
$rpg20 = $_POST['chk20'] ;
$rpg21 = $_POST['chk21'] ;
$rpg22 = $_POST['chk22'] ;
$rpg23 = $_POST['chk23'] ;
$rpg24 = $_POST['chk24'] ;
$rpg25 = $_POST['chk25'] ;
$rpg26 = $_POST['chk26'] ;
$rpg27 = $_POST['chk27'] ;
$rpg28 = $_POST['chk28'] ;
$rpg29 = $_POST['chk29'] ;
$rpg30 = $_POST['chk30'] ;
$rpg31 = $_POST['chk31'] ;
$rpg32 = $_POST['chk32'] ;
$rpg33 = $_POST['chk33'] ;
$rpg34 = $_POST['chk34'] ;
$rpg35 = $_POST['chk35'] ;
$rpg36 = $_POST['chk36'] ;
$rpg37 = $_POST['chk37'] ;
$rpg38 = $_POST['chk38'] ;
$rpg39 = $_POST['chk39'] ;
$rpg40 = $_POST['chk40'] ;
$rpg41 = $_POST['chk41'] ;
$rpg42 = $_POST['chk42'] ;
$rpg43 = $_POST['chk43'] ;
$rpg44 = $_POST['chk44'] ;
$rpg45 = $_POST['chk45'] ;
$rpg46 = $_POST['chk46'] ;
$rpg47 = $_POST['chk47'] ;
$rpg48 = $_POST['chk48'] ;
define('LINE_API',"https://notify-api.line.me/api/notify");
 
$token = "6xDJbyjjvnUf8wf2GspXDE6Tj2Kuvy3YkbIC8iepIue"; //ใส่Token ที่copy เอาไว้
$str = 'ชื่อผู้วิเคราะห์โรค : '  .$skg. ', อาการที่ท่านเลือก : '.$rpg.$rpg2.$rpg3.$rpg4.$rpg5.$rpg6.$rpg7.$rpg8.$rpg9.$rpg10.$rpg11.$rpg12.$rpg13.$rpg14.$rpg15.$rpg16.$rpg17.$rpg18.$rpg19.$rpg20.$rpg21.$rpg22.$rpg23.$rpg24.$rpg25.$rpg26.$rpg27.$rpg28.$rpg29.$rpg30.$rpg31.$rpg32.$rpg33.$rpg34.$rpg35.$rpg36.$rpg37.$rpg38.$rpg39.$rpg40.$rpg41.$rpg42.$rpg43.$rpg44.$rpg45.$rpg46.$rpg47.$rpg48; //ข้อความที่ต้องการส่ง สูงสุด 1000 ตัวอักษร
 
$res = notify_message($str,$token);
//print_r($res);
function notify_message($message,$token){
 $queryData = array('message' => $message);
 $queryData = http_build_query($queryData,'','&');
 $headerOptions = array( 
         'http'=>array(
            'method'=>'POST',
            'header'=> "Content-Type: application/x-www-form-urlencoded\r\n"
                      ."Authorization: Bearer ".$token."\r\n"
                      ."Content-Length: ".strlen($queryData)."\r\n",
            'content' => $queryData
         ),
 );
 $context = stream_context_create($headerOptions);
 $result = file_get_contents(LINE_API,FALSE,$context);
 $res = json_decode($result);
 return $res;
}
if($_POST){
	$msg = "" ;
	$err = "" ;
	$skg = $_POST['name_txt'] ;
	$vip = "";
	

		if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35'] and $_POST['chk36'] and $_POST['chk37'] and $_POST['chk38'] and $_POST['chk39'] and $_POST['chk40'] and $_POST['chk41'] and $_POST['chk42'] and $_POST['chk43'] and $_POST['chk44'] and $_POST['chk45'] and $_POST['chk46'] and $_POST['chk47'] and $_POST['chk48']){
			$msg .= " ไม่สามารถระบุโรคได้  <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
			}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35'] and $_POST['chk36'] and $_POST['chk37'] and $_POST['chk38'] and $_POST['chk39'] and $_POST['chk40'] and $_POST['chk41'] and $_POST['chk42'] and $_POST['chk43'] and $_POST['chk44'] and $_POST['chk45'] and $_POST['chk46'] and $_POST['chk47'] ){
			$msg .= " ไม่สามารถระบุโรคได้  <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35'] and $_POST['chk36'] and $_POST['chk37'] and $_POST['chk38'] and $_POST['chk39'] and $_POST['chk40'] and $_POST['chk41'] and $_POST['chk42'] and $_POST['chk43'] and $_POST['chk44'] and $_POST['chk45'] and $_POST['chk46']  ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35'] and $_POST['chk36'] and $_POST['chk37'] and $_POST['chk38'] and $_POST['chk39'] and $_POST['chk40'] and $_POST['chk41'] and $_POST['chk42'] and $_POST['chk43'] and $_POST['chk44'] and $_POST['chk45']  ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35'] and $_POST['chk36'] and $_POST['chk37'] and $_POST['chk38'] and $_POST['chk39'] and $_POST['chk40'] and $_POST['chk41'] and $_POST['chk42'] and $_POST['chk43'] and $_POST['chk44']  ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35'] and $_POST['chk36'] and $_POST['chk37'] and $_POST['chk38'] and $_POST['chk39'] and $_POST['chk40'] and $_POST['chk41'] and $_POST['chk42'] and $_POST['chk43']  ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35'] and $_POST['chk36'] and $_POST['chk37'] and $_POST['chk38'] and $_POST['chk39'] and $_POST['chk40'] and $_POST['chk41'] and $_POST['chk42']  ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35'] and $_POST['chk36'] and $_POST['chk37'] and $_POST['chk38'] and $_POST['chk39'] and $_POST['chk40'] and $_POST['chk41']  ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35'] and $_POST['chk36'] and $_POST['chk37'] and $_POST['chk38'] and $_POST['chk39'] and $_POST['chk40']   ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35'] and $_POST['chk36'] and $_POST['chk37'] and $_POST['chk38'] and $_POST['chk39']   ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35'] and $_POST['chk36'] and $_POST['chk37'] and $_POST['chk38']  ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35'] and $_POST['chk36'] and $_POST['chk37']   ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35'] and $_POST['chk36']    ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34'] and $_POST['chk35']    ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33'] and $_POST['chk34']     ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32'] and $_POST['chk33']     ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31'] and $_POST['chk32']     ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30'] and $_POST['chk31']      ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29'] and $_POST['chk30']      ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28'] and $_POST['chk29']      ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27'] and $_POST['chk28']     ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26'] and $_POST['chk27']     ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25'] and $_POST['chk26']      ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24'] and $_POST['chk25']      ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23'] and $_POST['chk24']       ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22'] and $_POST['chk23']        ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21'] and $_POST['chk22']        ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20'] and $_POST['chk21']        ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19'] and $_POST['chk20']         ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18'] and $_POST['chk19']          ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17'] and $_POST['chk18']           ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16'] and $_POST['chk17']            ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16'] and $_POST['chk16']             ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15'] and $_POST['chk16']              ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14'] and $_POST['chk15']              ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk14']               ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12'] and $_POST['chk13']               ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11'] and $_POST['chk12']                ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10'] and $_POST['chk11']                 ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk4'] and $_POST['chk6'] and $_POST['chk12'] and $_POST['chk13'] and $_POST['chk18'] and $_POST['chk10'] and $_POST['chk41'] and $_POST['chk31'] and $_POST['chk17'] and $_POST['chk36'] and $_POST['chk38'] ){
			$msg .= " คออักเสบ <br>";
			$vip .= "1.มีไข้สูง 2.เหนื่อย 3.อ่อนเพลีย 4.เบื่ออาหาร 5.ครั่นเนื้อครั่นตัว 6.หนาวสั่น 7.รู้สึกแห้งผากในลำคอหรือเจ็บคอมาก 8.กลืนอาหารหรือน้ำลำบาก 9.ต่อมที่คอบวม 10.เสียงแหบหรือกล่องเสียงอักเสบ 11.คอแดงหรือมีหนองที่ต่อมทอนซิล";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9'] and $_POST['chk10']                 ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8'] and $_POST['chk9']                 ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7'] and $_POST['chk8']                  ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6'] and $_POST['chk7']                  ){
			$msg .= " ไม่สามารถระบุโรคได้ <br>";
			$vip .= "ไม่สามารถระบุอาการได้ ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5'] and $_POST['chk6']                   ){
			$msg .= " 1.เป็นไข้หวัด 2.เยื่อบุตาอักเสบหรือตาแดง 3.คออักเสบ<br>";
			$vip .= "1.ไอ 2.คันตา 3.ตาแดง 4.มีไข้สูง 5.เจ็บคอ 6.เหนื่อย";
		}
		else if($_POST['chk1'] and $_POST['chk5'] and $_POST['chk11'] and $_POST['chk27'] and $_POST['chk22'] and $_POST['chk23']                   ){
			$msg .= " เป็นไข้หวัด <br>";
			$vip .= "1.ไอ 2.เจ็บคอ 3.น้ำมูกไหล 4.ปวดเมื่อยเนื้อตัวและข้อ 5.ต่อมในคอเจ็บบวม 6.ปวดศรีษะปานกลาง";
		}
		else if($_POST['chk3'] and $_POST['chk14'] and $_POST['chk2'] and $_POST['chk39'] and $_POST['chk28'] and $_POST['chk40']                   ){
			$msg .= " เยื่อบุตาอักเสบหรือตาแดง<br>";
			$vip .= "1.ตาแดง 2.หนังตาบวม 3.คันตา 4.มีสะเก็ดเกาะตาหรือขี้ตาเป็นหนอง 5.รู้สึกเหมือนมีขี้ผงเข้าตา 6.มีน้ำตาไหลออกจากตามากผิดปกติ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4'] and $_POST['chk5']                    ){
			$msg .= " 1.เป็นไข้หวัด 2.เยื่อบุตาอักเสบหรือตาแดง 3.คออักเสบ<br>";
			$vip .= "1.ไอ 2.คันตา 3.ตาแดง 4.มีไข้สูง 5.เจ็บคอ";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3'] and $_POST['chk4']                    ){
			$msg .= " 1.เป็นไข้หวัด  2.เยื่อบุตาอักเสบหรือตาแดง 3.คออักเสบ<br>";
			$vip .= "1.ไอ 2.คันตา 3.ตาแดง 4.มีไข้สูง";
		}
		else if($_POST['chk1'] and $_POST['chk2'] and $_POST['chk3']                     ){
			$msg .= " 1.เป็นไข้หวัด 2.เยื่อบุตาอักเสบหรือตาแดง<br>";
			$vip .= "1.ไอ 2.คันตา 3.ตาแดง";
		}
		else if($_POST['chk9'] and $_POST['chk8'] and $_POST['chk15']                     ){
			$msg .= " อาหารเป็นพิษ ท้องเดิน/ท้องเสีย<br>";
			$vip .= "1.ถ่ายเป็นน้ำหรือถ่ายเหลว 2.ปวดท้อง 3.อาเจียน";
		}
		else if($_POST['chk15'] and $_POST['chk21'] and $_POST['chk26']                     ){
			$msg .= " ท้องผูก<br>";
			$vip .= "1.อุจจาระแข็ง 2.มีแก๊สในกระเพราะ 3.เป็นริดสีดวงทวารหนัก";
		}
		else if($_POST['chk1'] and $_POST['chk2']                      ){
			$msg .= " 1.เป็นไข้หวัด 2.เยื่อบุตาอักเสบหรือตาแดง<br>";
			$vip .= "1.ไอ 2.คันตา";
		}
				else if ($chk == "20"){
			$msg .= " ลมพิษ<br>";
			$vip .= "ขึ้นผื่นเป็นวงกลม";
		}
					else if($chk == "1 and 2"){
			$msg .= " ไข้หวัด,เยื่อบุตาอักเสบหรือตาแดง <br>";
			$vip .= "ไอ,คันตา";
		}
					else if ($chk == "1 and 3"){
			$msg .= " ไข้หวัด,เยื่อบุตาอักเสบหรือตาแดง<br>";
			$vip .= "ไอ,ตาแดง";
		}
					else if ($chk == "1 and 4"){
			$msg .= " ไข้หวัด,คออักเสบ<br>";
			$vip .= "ไอ,มีไข้สูง";
		}
					else if ($chk == "1 and 5"){
			$msg .= " ไข้หวัด<br>";
			$vip .= "ไอ,เจ็บคอ";
		}
					else if ($chk == "1 and 6"){
			$msg .= " ไข้หวัด,คออักเสบ<br>";
			$vip .= "ไอ,เหนื่อย";
		}
					else if ($chk == "1 and 7"){
			$msg .= " ไข้หวัด,กรดไหลย้อน<br>";
			$vip .= "ไอ,เรอบ่อย";
		}
					else if ($chk == "1 and 8"){
			$msg .= " ไข้หวัด,อาหารเป็นพิษ<br>";
			$vip .= "ไอ,อาเจียน";
		}
					else if ($chk == "1 and 9"){
			$msg .= " ไข้หวัด,ท้องเดิน/ท้องเสีย<br>";
			$vip .= "ไอ,ปวดท้อง";
		}
					else if($chk == "1 and 10"){
			$msg .= " ไข้หวัด,คออักเสบ <br>";
			$vip .= "ไอ,หนาวสั่น";
		}
					else if ($chk == "1 and 11"){
			$msg .= " ไข้หวัด<br>";
			$vip .= "ไอ,น้ำมูกไหล";
		}
					else if ($chk == "1 and 12"){
			$msg .= " ไข้หวัด,คออักเสบ<br>";
			$vip .= "ไอ,อ่อนเพลีย";
		}
					else if ($chk == "1 and 13"){
			$msg .= " ไข้หวัด,คออักเสบ<br>";
			$vip .= "ไอ,เบื่ออาหาร";
		}
					else if ($chk == "1 and 14"){
			$msg .= " ไข้หวัด,เยื่อบุตาอักเสบหรือตาแดง<br>";
			$vip .= "ไอ,หนังตาบวม";
		}
					else if ($chk == "1 and 15"){
			$msg .= " ไข้หวัด,ท้องผูก<br>";
			$vip .= "ไอ,อุจจาระแข็ง";
		}
					else if ($chk == "1 and 16"){
			$msg .= " ไข้หวัด,ผิวหนังอักเสบเนื่องจากการแพ้แสงแดด<br>";
			$vip .= "ไอ,ผิวหนังผุพอง";
		}
					else if ($chk == "1 and 17"){
			$msg .= " ไข้หวัด,คออักเสบ<br>";
			$vip .= "ไอ,ต่อมที่คอบวม";
		}
					else if($chk == "1 and 18"){
			$msg .= " ไข้หวัด,คออักเสบ<br>";
			$vip .= "ไอ,ครั่นเนื้อครั่นตัว";
		}
					else if ($chk == "1 and 19"){
			$msg .= " ไข้หวัด,ลมพิษ<br>";
			$vip .= "ไอ,ขึ้นผื่นเป็นวงวงรี";
		}
					else if ($chk == "1 and 20"){
			$msg .= " ไข้หวัด,ลมพิษ<br>";
			$vip .= "ไอ,ขึ้นผื่นเป็นวงกลม";
		}
					else if ($chk == "1 and 21"){
			$msg .= " ไข้หวัด,ท้องผูก<br>";
			$vip .= "ไอ,มีแก๊สในกระเพราะ";
		}
					else if ($chk == "1 and 22"){
			$msg .= " ไข้หวัด,ไข้หวัด<br>";
			$vip .= "ไอ,ต่อมในคอเจ็บบวม";
		}
					else if ($chk == "1 and 23"){
			$msg .= " ไข้หวัด<br>";
			$vip .= "ไอ,ปวดศรีษะปานกลาง";
		}
					else if ($chk == "1 and 24"){
			$msg .= " ไข้หวัด,ลมพิษ<br>";
			$vip .= "ไอ,ขึ้นผื่นเป็นวงแดงนูน";
		}
					else if ($chk == "1 and 25"){
			$msg .= " ไข้หวัด,ลมพิษ<br>";
			$vip .= "ไอ,ขึ้นผื่นเป็นวง";
		}	
					else if ($chk == "1 and 26"){
			$msg .= " ไข้หวัด,ท้องผูก<br>";
			$vip .= "ไอ,เป็นริดสีดวงทวารหนัก";
		}	
					else if ($chk == "2 and 1"){
			$msg .= " เยื่อบุตาอักเสบหรือตาแดง,ไข้หวัด<br>";
			$vip .= "คันตา,ไอ";
		}	

					else if ($chk == "3 and 4"){
			$msg .= " เยื่อบุตาอักเสบหรือตาแดง,คออักเสบ<br>";
			$vip .= "ตาแดง,มีไข้สูง";
		}
					else if ($chk == "5 and 6"){
			$msg .= " ไข้หวัด,คออักเสบ<br>";
			$vip .= "เจ็บคอ,เหนื่อย";
		}
					else if ($chk == "7 and 8"){
			$msg .= " กรดไหลย้อน,อาหารเป็นพิษ<br>";
			$vip .= "เรอบ่อย,อาเจียน";
		}
					else if ($chk == "9 and 10"){
			$msg .= " ท้องเดิน/ท้องเสีย,คออักเสบ<br>";
			$vip .= "ปวดท้อง,หนาวสั่น";
		}
					else if ($chk == "11 and 12"){
			$msg .= " ไข้หวัด,คออักเสบ<br>";
			$vip .= "น้ำมูกไหล,อ่อนเพลีย";
		}
					else if ($chk == "13 and 14"){
			$msg .= " คออักเสบ,เยื่อบุตาอักเสบหรือตาแดง<br>";
			$vip .= "เบื่ออาหาร,หนังตาบวม";
		}
					else if ($chk == "15 and 16"){
			$msg .= " ท้องผูก,ผิวหนังอักเสบเนื่องจากการแพ้แสงแดด<br>";
			$vip .= "อุจจาระแข็ง,ผิวหนังผุพอง";
		}
					else if ($chk == "17 and 18"){
			$msg .= " คออักเสบ<br>";
			$vip .= "ต่อมที่คอบวม,ครั่นเนื้อครั่นตัว";
		}
					else if ($chk == "19 and 20"){
			$msg .= " ลมพิษ<br>";
			$vip .= "ขึ้นผื่นเป็นวงวงรี,ขึ้นผื่นเป็นวงกลม";
		}
					else if ($chk == "21 and 22"){
			$msg .= " ท้องผูก,ไข้หวัด<br>";
			$vip .= "มีแก๊สในกระเพราะ,ต่อมในคอเจ็บบวม";
		}
					else if ($chk == "23 and 24"){
			$msg .= " ไข้หวัด,ลมพิษ<br>";
			$vip .= "ปวดศรีษะปานกลาง,ขึ้นผื่นเป็นวงแดงนูน";
		}
					else if ($chk == "25 and 26"){
			$msg .= " ลมพิษ,ท้องผูก<br>";
			$vip .= "ขึ้นผื่นเป็นวง รู้สึกคัน,เป็นริดสีดวงทวารหนัก";
		}
					else if ($chk == "27 and 28"){
			$msg .= " ไข้หวัด,เยื่อบุตาอักเสบหรือตาแดง<br>";
			$vip .= "ปวดเมื่อยเนื้อตัวและข้อ,รู้สึกเหมือนมีขี้ผงเข้าตา";
		}
					else if ($chk == "29 and 30"){
			$msg .= " ท้องเดิน/ท้องเสีย,เคล็ดขัดยอก<br>";
			$vip .= "ถ่ายเป็นน้ำหรือถ่ายเหลว,ข้อหรือกล้ามเนื้อบวมแดง";
		}
					else if ($chk == "31 and 32"){
			$msg .= " คออักเสบ,ไข้หวัด<br>";
			$vip .= "กลืนอาหารหรือน้ำลำบาก,ปวดเมื่อยข้อหรือกล้ามเนื้อ";
		}
					else if ($chk == "33 and 34"){
			$msg .= " เคล็ดขัดยอก,กรดไหลย้อน<br>";
			$vip .= "ฟกช้ำรอบข้อหรือกล้ามเนื้อ,มีบวมพองหลังกินอาหาร";
		}
					else if ($chk == "35 and 36"){
			$msg .= " ผิวหนังอักเสบเนื่องจากการแพ้แสงแดด,คออักเสบ<br>";
			$vip .= "ผิวหนังแดง และไวต่อความรู้สึก,เสียงแหบหรือกล่องเสียงอักเสบ";
		}
					else if ($chk == "37 and 38"){
			$msg .= " เคล็ดขัดยอก,คออักเสบ<br>";
			$vip .= "ข้อหรือกล้ามเนื้อไวต่อการสัมผัส,คอแดงหรือมีหนองที่ต่อมทอนซิล";
		}
					else if ($chk == "39 and 40"){
			$msg .= " เยื่อบุตาอักเสบหรือตาแดง<br>";
			$vip .= "มีสะเก็ดเกาะตาหรือขี้ตาเป็นหนอง,มีน้ำตาไหลออกจากตามากผิดปกติ";
		}
					else if ($chk == "41 and 42"){
			$msg .= " คออักเสบ,ลมพิษ<br>";
			$vip .= "รู้สึกแห้งผากในลำคอหรือเจ็บคอมาก,ขึ้นผื่นเป็นวง รู้สึกร้อนผ่าวตามผิวกาย";
		}
					else if ($chk == "43 and 44"){
			$msg .= " กระเพาะ,กรดไหลย้อน<br>";
			$vip .= "ปวดท้อง เป็นๆ หายๆ มักปวดตรงใต้ลิ้นปี่,อาหารไหลย้อนขึ้นมา และมีรสเปรี้ยวในปาก";
		}
					else if ($chk == "45 and 46"){
			$msg .= " ผิวหนังอักเสบเนื่องจากการแพ้แสงแดด<br>";
			$vip .= "ผิวหนังตกสะเก็ด คัน และรู้สึกเหมือนโดนหนามแทง,เป็นลมแดด";
		}
					else if ($chk == "47 and 48"){
			$msg .= " กรดไหลย้อน,เส้นเอ็นอักเสบ<br>";
			$vip .= "แสบร้อนจุกเสียดบริเวณใต้ลิ้นปี่ (เวลาก้มตัว นอนลง และกินอาหาร),ปวดเจ็บตรงเส้นเอ็น นานเป็นสัปดาห์";
		}
		else{
			$vip .= "ไม่ได้เลือกอาการ";
			$msg .= " ไม่สามารถระบุโรคได้<br>";
		}
	if($err ==""){
		echo "<img src='M/m1.jpg' width='850'> <br><br><b>ผลการวิเคราะห์โรคของคุณ : </b>$skg <br><b>คุณมีอาการ : </b>$vip <br><b>คุณมีความเสี่ยงที่จะเป็นโรค :</b>$msg "; 
		exit("</body></html>");
	}
	else{
		echo '<div class="warning"><b>ข้อผิดพลาด</b>'.$err. '<div>';
	}

		}
?>
</td>
</tr>
</table>
</body>
</html>

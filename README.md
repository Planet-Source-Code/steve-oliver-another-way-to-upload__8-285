﻿<div align="center">

## Another way to Upload


</div>

### Description

Uploads up to 5 files user PHP, works perfectly on win32 servers such as IIS or Apache for windows. Demonstrates the use of copy(), functions, and switch operators.
 
### More Info
 
$destination should be set to where you want the files uploaded to.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Steve Oliver](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/steve-oliver.md)
**Level**          |Beginner
**User Rating**    |4.0 (44 globes from 11 users)
**Compatibility**  |PHP 4\.0
**Category**       |[Files](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files__8-2.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/steve-oliver-another-way-to-upload__8-285/archive/master.zip)





### Source Code

```
<?
function uploadProg($filename1,$filename1_name,$filename2,$filename2_name,$filename3,$filename3_name,$filename4,$filename4_name,$filename5,$filename5_name){
########Set the destination here##############
$destination="C:\\Uploads\\";
copy($filename1,$destination."/".$filename1_name);
copy($filename2,$destination."/".$filename2_name);
copy($filename3,$destination."/".$filename3_name);
copy($filename4,$destination."/".$filename4_name);
copy($filename5,$destination."/".$filename5_name);
echo "<h1>File(s) Uploaded...</h1>";
echo "<b>$filename1_name was uploaded succesfully.</b><br>";
echo "<b>$filename2_name was uploaded succesfully.</b><br>";
echo "<b>$filename3_name was uploaded succesfully.</b><br>";
echo "<b>$filename4_name was uploaded succesfully.</b><br>";
echo "<b>$filename5_name was uploaded succesfully.</b><br><br>";
echo "<a href=\"upload.php\">Click here to go back.</a>";
}
function main(){?>
<form method="post" action="upload.php" enctype="multipart/form-data">
Files to Upload:<br>
<input type="file" name="filename1" size="20" tabindex="1"><br>
<input type="file" name="filename2" size="20" tabindex="2"><br>
<input type="file" name="filename3" size="20" tabindex="3"><br>
<input type="file" name="filename4" size="20" tabindex="4"><br>
<input type="file" name="filename5" size="20" tabindex="5"><br>
<input type="hidden" name="action" value="uploadProg">
<input type="submit" value="Upload Files" tabindex="6">
</form><?}
switch ($action){
    default:
    main();
    break;
    case "uploadProg":
    if ($filename1=="none") {echo("<h1>No File Selected....</h1>"); break;}
    uploadProg($filename1,$filename1_name,$filename2,$filename2_name,$filename3,$filename3_name,$filename4,$filename4_name,$filename5,$filename5_name);
    break;
}
?>
```


# final-activity-3
<!DOCTYPE html>
<html>
<body>
    <title>PHP Form</title>
</head>
<body>

<h2>Simple Form PHP</h2>


<form method="get" action="">

Name:
<input type="text" name="first name" placeholder="spencer">

<br><br>


</form>

<?php
if(isset($_GET['name'])) {

    $name = $_GET['name'];

    echo "Hello, " . $name;
}
?>

</body>
</html>
<!DOCTYPE html>
<html>
<body>

<form method="post" action="">

Username:
<input type="text" name="username" placeholder="spencerbarredo">

<br><br>

Password:
<input type="password" name="password" placeholder="barredo06">

<br><br>


</form>

<?php
if(isset($_POST['username'])) {

    $username = $_POST['username'];

    echo "Welcome, " . $username;
}
?>

</body>
</html>
<!DOCTYPE html>
<html>
<body>

<form method="post" action="">

<br><br>

Email:
<input type="text" name="email" placeholder="spencerbarredo06@gmail.com" required>

<br><br>

</body>
</html>
<!DOCTYPE html>
<html>
<body>

<form method="post" action="">

Hobbies:<br>

<input type="checkbox" name="hobbies[]" value="Reading"> watching<br>

<input type="checkbox" name="hobbies[]" value="Sports"> playing online<br>

<input type="checkbox" name="hobbies[]" value="Music"> Music<br><br>
</form>

<?php
if(isset($_POST['hobbies'])) {

    $hobbies = $_POST['hobbies'];

    echo "Selected Hobbies:<br>";

    foreach($hobbies as $hobby) {
        echo $hobby . "<br>";
    }
}
?>

</body>
</html>
<!DOCTYPE html>
<html>
<body>

<form method="post" action="">

Gender:<br><br>

<input type="radio" name="gender" value="Male"checked> Male<br>

<input type="radio" name="gender" value="Female"> Female<br><br>


</form>

<?php
if(isset($_POST['gender'])) {

    $gender = $_POST['gender'];

    echo "Selected Gender: " . $gender;
}
?>

</body>
<!DOCTYPE html>
<html>
<head>
    <title>Lab 8 - Dropdown Menu</title>
</head>
<body>

<form method="post">
    <label>Select Course:</label>
    <select name="course" required >
        <option value="">-- Choose a course --</option>
        <option value="BSIT">BS Information Technology</option>
        <option value="BSCS">BS Computer Science</option>
        <option value="BSIS">BS Information Systems</option>
    </select>
        <option value="BSIT">BSIT</option>
    </select>

    </select> 
    <br><br>
</form>

<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $course = $_POST["course"];

    if (!empty($course)) {
        echo "<h3>You select: $course</h3>";
    } else {
        echo "<h3>Please select a course.</h3>";
    }
}
?>

</body>
</html>
</html>
<form method="post">
    <label>Enter Age:</label>
    <input type="number" name="age" placeholder="23" required>

  <input type="submit" value="Submit">
</form> 

<p>If you click the "Submit" button, the form-data will be sent to a page called "/action_page.php".</p>

</body>
</html>


# ass

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Registration Form</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light">

<div class="container mt-5">
    <div class="card shadow-lg">
        <div class="card-header bg-primary text-white">
            <h4 class="mb-0" >Payroll Calculator</h4>
        </div>
        <div class="card-body">
            <form action="computesala.php" method="POST">
                <!-- Full Name -->
                <div class="mb-1">
                    <label for="fullname" class="form-label">Employee Name</label>
                    <input type="text" name="fullname" id="fullname" class="form-control" placeholder="Enter your full name" required>
                </div>
                <!-- Days of Work -->
                <div class="mb-2">
                    <label for="fullname" class="form-label">Total Days of Work</label>
                    <input type="number" name="days" id="" class="form-control" placeholder="" required>
                </div>
                <div class="mb-3">
                    <label for="fullname" class="form-label">Daily Rate</label>
                    <input type="number" name="rate" id="" class="form-control" placeholder="" required>
                </div>        
                <div class="mb-2">
                    <label for="fullname" class="form-label">Cash Advance</label>
                    <input type="number" name="adv" id="" class="form-control" placeholder="" required>
                </div>
                <!-- Submit Button -->
                <div class="text-end">
                    <button type="submit" class="btn btn-success">Generate Payslip</button>
                </div>
            </form>
        </div>
    </div>
</div>

<!-- Bootstrap JS Bundle -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>

</body>
</html>







<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration Details</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body class="bg-light">

<div class="container mt-5">
    <div class="card shadow-lg">
        <div class="card-header bg-success text-white">
            <h4 class="mb-0">Registration Successful</h4>
        </div>
        <div class="card-body">
            <?php
                    $work = $_POST['num2'];
                    $rate = $_POST['num3'];
                    $adv = $_POST['num4'];




                if($_SERVER['REQUEST_METHOD'] == "POST"){
                    $fullname = htmlspecialchars($_POST['fullname']);
                    $dayswork = htmlspecialchars($_POST['dayswork']);
                    $adress = htmlspecialchars($_POST['address']);
                    $birthdate = htmlspecialchars($_POST['birthdate']);

                }
                else{
                    echo "<div class='alert alert-danger'> No data received.</div>";
                    exit();
                }
            ?>
            <p class="lead">Here are the details you submitted:</p>
           
            <ul class="list-group">
                <li class="list-group-item"><strong>Full Name:</strong> <?=$fullname; ?> </li>
                <li class="list-group-item"><strong>Email:</strong> <?=$email;?>  </li>
                <li class="list-group-item"><strong>Address:</strong> <?=$adress;?>  </li>
                <li class="list-group-item"><strong>Birthdate:</strong> <?=$birthdate; ?> </li>
                <li class="list-group-item"><strong>Course:</strong> <?=$course;?>  </li>
                <li class="list-group-item"><strong>Gender:</strong> <?=$gender;?>  </li>
            </ul>

            <div class="mt-4">
                <a href="index.php" class="btn btn-primary">Register Another Student</a>
            </div>
        </div>
    </div>
</div>

<!-- Bootstrap JS -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>

</body>
</html>

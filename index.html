<?php
include 'config.php';

// Initialize variables
$first_name = $last_name = $age = $gender = $email = $contact_number = "";
$edit_mode = false;
$edit_id = 0;

// Handle form submission
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    if (isset($_POST['create'])) {
        // CREATE operation
        $first_name = mysqli_real_escape_string($conn, $_POST['first_name']);
        $last_name = mysqli_real_escape_string($conn, $_POST['last_name']);
        $age = mysqli_real_escape_string($conn, $_POST['age']);
        $gender = mysqli_real_escape_string($conn, $_POST['gender']);
        $email = mysqli_real_escape_string($conn, $_POST['email']);
        $contact_number = mysqli_real_escape_string($conn, $_POST['contact_number']);
        
        $sql = "INSERT INTO users (first_name, last_name, age, gender, email, contact_number) 
                VALUES ('$first_name', '$last_name', '$age', '$gender', '$email', '$contact_number')";
        
        if (mysqli_query($conn, $sql)) {
            echo "<script>alert('Record created successfully');</script>";
        } else {
            echo "<script>alert('Error creating record: " . mysqli_error($conn) . "');</script>";
        }
        
        // Clear form
        $first_name = $last_name = $age = $gender = $email = $contact_number = "";
    }
    
    if (isset($_POST['update'])) {
        // UPDATE operation
        $edit_id = mysqli_real_escape_string($conn, $_POST['edit_id']);
        $first_name = mysqli_real_escape_string($conn, $_POST['first_name']);
        $last_name = mysqli_real_escape_string($conn, $_POST['last_name']);
        $age = mysqli_real_escape_string($conn, $_POST['age']);
        $gender = mysqli_real_escape_string($conn, $_POST['gender']);
        $email = mysqli_real_escape_string($conn, $_POST['email']);
        $contact_number = mysqli_real_escape_string($conn, $_POST['contact_number']);
        
        $sql = "UPDATE users SET 
                first_name='$first_name', 
                last_name='$last_name', 
                age='$age', 
                gender='$gender', 
                email='$email', 
                contact_number='$contact_number' 
                WHERE id=$edit_id";
        
        if (mysqli_query($conn, $sql)) {
            echo "<script>alert('Record updated successfully');</script>";
        } else {
            echo "<script>alert('Error updating record: " . mysqli_error($conn) . "');</script>";
        }
        
        // Reset edit mode
        $edit_mode = false;
        $edit_id = 0;
        $first_name = $last_name = $age = $gender = $email = $contact_number = "";
    }
}

// Handle edit action
if (isset($_GET['edit'])) {
    $edit_id = mysqli_real_escape_string($conn, $_GET['edit']);
    $sql = "SELECT * FROM users WHERE id=$edit_id";
    $result = mysqli_query($conn, $sql);
    
    if (mysqli_num_rows($result) == 1) {
        $row = mysqli_fetch_assoc($result);
        $first_name = $row['first_name'];
        $last_name = $row['last_name'];
        $age = $row['age'];
        $gender = $row['gender'];
        $email = $row['email'];
        $contact_number = $row['contact_number'];
        $edit_mode = true;
    }
}

// Handle delete action
if (isset($_GET['delete'])) {
    $delete_id = mysqli_real_escape_string($conn, $_GET['delete']);
    $sql = "DELETE FROM users WHERE id=$delete_id";
    
    if (mysqli_query($conn, $sql)) {
        echo "<script>alert('Record deleted successfully');</script>";
    } else {
        echo "<script>alert('Error deleting record: " . mysqli_error($conn) . "');</script>";
    }
}

// Fetch all records
$sql = "SELECT * FROM users ORDER BY id DESC";
$result = mysqli_query($conn, $sql);
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Information Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f5f5f5;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .form-section, .table-section {
            margin-bottom: 30px;
        }
        h2 {
            color: #333;
            border-bottom: 2px solid #333;
            padding-bottom: 10px;
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input[type="text"],
        input[type="number"],
        input[type="email"],
        select {
            width: 100%;
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
        }
        .radio-group {
            display: flex;
            gap: 15px;
        }
        .radio-group label {
            display: flex;
            align-items: center;
            font-weight: normal;
        }
        .radio-group input {
            margin-right: 5px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }
        button:hover {
            background-color: #45a049;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 12px;
            text-align: left;
        }
        th {
            background-color: #f2f2f2;
            font-weight: bold;
        }
        tr:nth-child(even) {
            background-color: #f9f9f9;
        }
        .action-buttons {
            display: flex;
            gap: 5px;
        }
        .edit-btn {
            background-color: #2196F3;
            color: white;
            padding: 5px 10px;
            text-decoration: none;
            border-radius: 3px;
            font-size: 14px;
        }
        .delete-btn {
            background-color: #f44336;
            color: white;
            padding: 5px 10px;
            text-decoration: none;
            border-radius: 3px;
            font-size: 14px;
        }
        .edit-btn:hover {
            background-color: #0b7dda;
        }
        .delete-btn:hover {
            background-color: #da190b;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Information Form Section -->
        <div class="form-section">
            <h2>Information Form</h2>
            <form method="POST" action="">
                <?php if ($edit_mode): ?>
                    <input type="hidden" name="edit_id" value="<?php echo $edit_id; ?>">
                <?php endif; ?>
                
                <div class="form-group">
                    <label for="first_name">First Name</label>
                    <input type="text" id="first_name" name="first_name" value="<?php echo $first_name; ?>" required>
                </div>
                
                <div class="form-group">
                    <label for="last_name">Last Name</label>
                    <input type="text" id="last_name" name="last_name" value="<?php echo $last_name; ?>" required>
                </div>
                
                <div class="form-group">
                    <label for="age">Age</label>
                    <input type="number" id="age" name="age" value="<?php echo $age; ?>" required min="1" max="150">
                </div>
                
                <div class="form-group">
                    <label>Gender</label>
                    <div class="radio-group">
                        <label>
                            <input type="radio" name="gender" value="Male" <?php echo ($gender == 'Male') ? 'checked' : ''; ?> required> Male
                        </label>
                        <label>
                            <input type="radio" name="gender" value="Female" <?php echo ($gender == 'Female') ? 'checked' : ''; ?>> Female
                        </label>
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" value="<?php echo $email; ?>" required>
                </div>
                
                <div class="form-group">
                    <label for="contact_number">Contact Number</label>
                    <input type="text" id="contact_number" name="contact_number" value="<?php echo $contact_number; ?>" required>
                </div>
                
                <?php if ($edit_mode): ?>
                    <button type="submit" name="update">Update</button>
                    <a href="index.php" style="margin-left: 10px;">Cancel</a>
                <?php else: ?>
                    <button type="submit" name="create">Create</button>
                <?php endif; ?>
            </form>
        </div>

        <!-- Information Table Section -->
        <div class="table-section">
            <h2>Information Table</h2>
            <?php if (mysqli_num_rows($result) > 0): ?>
                <table>
                    <thead>
                        <tr>
                            <th>First Name</th>
                            <th>Last Name</th>
                            <th>Age</th>
                            <th>Gender</th>
                            <th>Email</th>
                            <th>Contact Number</th>
                            <th>Actions</th>
                        </tr>
                    </thead>
                    <tbody>
                        <?php while($row = mysqli_fetch_assoc($result)): ?>
                        <tr>
                            <td><?php echo htmlspecialchars($row['first_name']); ?></td>
                            <td><?php echo htmlspecialchars($row['last_name']); ?></td>
                            <td><?php echo htmlspecialchars($row['age']); ?></td>
                            <td><?php echo htmlspecialchars($row['gender']); ?></td>
                            <td><?php echo htmlspecialchars($row['email']); ?></td>
                            <td><?php echo htmlspecialchars($row['contact_number']); ?></td>
                            <td class="action-buttons">
                                <a href="index.php?edit=<?php echo $row['id']; ?>" class="edit-btn">Edit</a>
                                <a href="index.php?delete=<?php echo $row['id']; ?>" class="delete-btn" 
                                   onclick="return confirm('Are you sure you want to delete this record?')">Delete</a>
                            </td>
                        </tr>
                        <?php endwhile; ?>
                    </tbody>
                </table>
            <?php else: ?>
                <p>No records found. Please add some records using the form above.</p>
            <?php endif; ?>
        </div>
    </div>
</body>
</html>

<?php
// Close connection
mysqli_close($conn);
?>

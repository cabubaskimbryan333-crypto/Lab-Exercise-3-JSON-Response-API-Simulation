<?php
// Step 1: Declare a JSON string
$jsonString = '{"name": "Maria", "age": 25, "email": "maria@example.com"}';

// Step 2: Decode JSON into PHP object and array
$obj = json_decode($jsonString);
$array = json_decode($jsonString, true);
?>

<!DOCTYPE html>
<html>
<head>
    <title>JSON Handling in PHP</title>
</head>
<body>

<h2>Decoded JSON</h2>
<p><strong>Object Name:</strong> <?php echo $obj->name; ?></p>
<p><strong>Array Email:</strong> <?php echo $array['email']; ?></p>

<hr>

<h2>User Profiles (JSON Output)</h2>

<?php
// Step 3: Create an array of user profiles
$users = [
    [
        "id" => 1,
        "name" => "Kim Bryan Cabubas",
        "age" => 23,
        "email" => "kimbryancabubas212@gmail.com",
        "status" => "active"
    ],
    [
        "id" => 2,
        "name" => "Julieana Dela Cruz",
        "age" => 18,
        "email" => "julieanDelaCruz@gmail.com",
        "status" => "active"
    ],
    [
        "id" => 3,
        "name" => "Elysa Nicole Valdez",
        "age" => 19,
        "email" => "elysaNicoleValdez@gmail.com",
        "status" => "active"
    ]
];

// Step 4: Encode and display JSON (pretty-printed inside <pre> for readability)
$jsonOutput = json_encode($users, JSON_PRETTY_PRINT);
?>

<pre><?php echo $jsonOutput; ?></pre>

</body>
</html>

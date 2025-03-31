# Html2
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Multimedia Webpage</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
    }
    h1, h2 {
      text-align: center;
    }
    .container {
      max-width: 900px;
      margin: 0 auto;
    }
    form {
      margin-bottom: 20px;
    }
    input, select, button {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
    }
    table {
      width: 100%;
      border-collapse: collapse;
    }
    table, th, td {
      border: 1px solid black;
    }
    th, td {
      padding: 10px;
      text-align: left;
    }
    .media-container {
      display: flex;
      justify-content: space-around;
      margin: 20px 0;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Welcome to the Multimedia Webpage</h1>
    
    <!-- Registration Form with Validation -->
    <h2>Registration Form</h2>
    <form id="registrationForm" action="#" method="post">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" required placeholder="Enter your name" />

      <label for="email">Email:</label>
      <input type="email" id="email" name="email" required placeholder="Enter your email" />

      <label for="password">Password:</label>
      <input type="password" id="password" name="password" required minlength="6" placeholder="Enter a password (min 6 characters)" />

      <label for="country">Country:</label>
      <select id="country" name="country" required>
        <option value="" disabled selected>Select your country</option>
        <option value="USA">USA</option>
        <option value="Canada">Canada</option>
        <option value="UK">UK</option>
      </select>

      <button type="submit">Register</button>
    </form>

    <!-- Multimedia Section (Audio and Video) -->
    <div class="media-container">
      <div>
        <h2>Audio Element</h2>
        <audio controls>
          <source src="https://download.samplelib.com/mp3/sample-9s.mp3" type="audio/mp3">
          Your browser does not support the audio element.
        </audio>
      </div>
      
      <div>
        <h2>Video Element</h2>
        <video controls width="300">
          <source src="video/sample-video.mp4" type="video/mp4">
          Your browser does not support the video element.
        </video>
      </div>
    </div>

    <!-- Embedded Image -->
    <h2>Embedded Image</h2>
    <img src="data:image/jpeg;base64,"
    <!-- Table Example -->
    <h2>Sample Table</h2>
    <table>
      <thead>
        <tr>
          <th>Name</th>
          <th>Age</th>
          <th>Location</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>John Doe</td>
          <td>25</td>
          <td>New York</td>
        </tr>
        <tr>
          <td>Jane Smith</td>
          <td>30</td>
          <td>London</td>
        </tr>
        <tr>
          <td>Sam Johnson</td>
          <td>22</td>
          <td>Toronto</td>
        </tr>
      </tbody>
    </table>

    <!-- List Example -->
    <h2>Sample List</h2>
    <ul>
      <li>Apple</li>
      <li>Banana</li>
      <li>Cherry</li>
    </ul>
  </div>

  <script>
    // Basic form validation
    document.getElementById("registrationForm").addEventListener("submit", function(event) {
      const name = document.getElementById("name").value;
      const email = document.getElementById("email").value;
      const password = document.getElementById("password").value;
      
      if (!name || !email || !password) {
        alert("Please fill in all fields.");
        event.preventDefault(); // Prevent form submission
      }
    });
  </script>
  
</body>
</html>

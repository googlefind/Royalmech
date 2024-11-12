
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Google Search Bar</title>
  <style>
    /* General Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    /* Body Styling */
    body {
      font-family: Arial, sans-serif;
      background-color: #f2f2f2;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      flex-direction: column;
    }

    /* Google Logo Styling */
    .google-logo img {
      width: 272px; /* Google logo size */
      margin-bottom: 20px;
    }

    /* Search Box Container */
    .google-search-container {
      text-align: center;
    }

    /* Search Box Styling */
    .search-box {
      width: 100%;
      max-width: 584px;
      background-color: white;
      border-radius: 24px;
      padding: 12px 20px;
      box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
      display: flex;
      justify-content: center;
      align-items: center;
    }

    /* Input Field Styling */
    .search-box input {
      width: 100%;
      padding: 14px;
      font-size: 16px;
      border: 1px solid #ccc;
      border-radius: 24px;
      outline: none;
      max-width: 500px;
    }

    /* Input Focus State */
    .search-box input:focus {
      border-color: #4285f4;
    }

    /* Search Buttons Container */
    .search-buttons {
      margin-top: 20px;
    }

    /* Button Styling */
    .search-buttons button {
      background-color: #f8f8f8;
      border: 1px solid #f8f8f8;
      padding: 10px 24px;
      font-size: 14px;
      border-radius: 4px;
      cursor: pointer;
      margin: 0 6px;
      transition: all 0.2s;
    }

    .search-buttons button:hover {
      background-color: #f1f1f1;
    }

    /* Button Focused Styling */
    .search-buttons button:focus {
      outline: none;
      box-shadow: 0px 0px 5px rgba(66, 133, 244, 0.6);
    }
  </style>
</head>
<body>

  <!-- Google Logo -->
  <div class="google-logo">
    <img src="https://www.google.com/images/branding/googlelogo/1x/googlelogo-color-272x92.png" alt="Google Logo">
  </div>

  <!-- Google Search Bar Interface -->
  <div class="google-search-container">
    <div class="search-box">
      <input type="text" id="searchInput" placeholder="Search Google or type a URL">
    </div>

    <!-- Search Buttons -->
    <div class="search-buttons">
      <button onclick="performSearch()">Google Search</button>
      <button onclick="performImFeelingLucky()">I'm Feeling Lucky</button>
    </div>
  </div>

  <script>
    // Perform the Google Search
    function performSearch() {
      const searchQuery = document.getElementById("searchInput").value;
      if (searchQuery.trim() !== "") {
        // Redirect to Google search results
        window.location.href = `https://www.google.com/search?q=${encodeURIComponent(searchQuery)}`;
      } else {
        alert("Please enter a search term.");
      }
    }

    // "I'm Feeling Lucky" Button
    function performImFeelingLucky() {
      const searchQuery = document.getElementById("searchInput").value;
      if (searchQuery.trim() !== "") {
        // Redirect to Google's "I'm Feeling Lucky" feature
        window.location.href = `https://www.google.com/search?btnI=I&aqs=chrome..69i57j0i22i30l9.1890j0j7&pglt=43&q=${encodeURIComponent(searchQuery)}`;
      } else {
        alert("Please enter a search term.");
      }
    }

    // Trigger search when "Enter" key is pressed
    document.getElementById("searchInput").addEventListener("keypress", function(event) {
      if (event.key === "Enter") {
        performSearch();
      }
    });
  </script>

</body>
</html>

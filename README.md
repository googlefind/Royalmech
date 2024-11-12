
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Google Search Bar Interface</title>
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
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: #f2f2f2;
    }

    /* Google Search Container */
    .google-search-container {
      text-align: center;
    }

    /* Search Box Styling */
    .search-box {
      width: 100%;
      max-width: 600px;
      margin-top: -50px;
      background-color: white;
      border-radius: 24px;
      padding: 12px 20px;
      box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
    }

    /* Input Field Styling */
    .search-box input {
      width: 100%;
      padding: 10px;
      font-size: 16px;
      border: 1px solid #ccc;
      border-radius: 24px;
      outline: none;
    }

    /* Input Focus State */
    .search-box input:focus {
      border-color: #4285f4;
    }

    /* Hide Button by Default */
    .search-box button {
      display: none;
    }
  </style>
</head>
<body>

  <!-- Google Search Bar Interface -->
  <div class="google-search-container">
    <div class="search-box">
      <input type="text" id="searchInput" placeholder="Search Google or type a URL">
      <button onclick="performSearch()">Search</button>
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

    // Trigger search when "Enter" key is pressed
    document.getElementById("searchInput").addEventListener("keypress", function(event) {
      if (event.key === "Enter") {
        performSearch();
      }
    });
  </script>

</body>
</html>

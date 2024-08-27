---
layout: base
title: Student Home 
description: Home Page
hide: true
---

<img src="https://github.com/iKAN2025.png" class="profile-pic mt-4" alt="Profile Picture" style="display: block; margin: 0 auto;">


<div style="text-align: center;">
  <h2>iKAN2025</h2>
</div>


Hi, I'm iKAN20225,   a student at Del Norte High School who is interested in computer science.  I am passionate about full stack development and machine learning.  I love solving real-world problems through technology and enjoy collaborating with teams to build innovative solutions.

## Key Interests
- **Technology and Innovation**: Leveraging technology to solve complex problems.
- **Machine Learning and AI**: Developing and implementing intelligent systems.
- **Full Stack Development**: Building comprehensive web applications from front-end to back-end.
- **Team Collaboration**: Working effectively within teams to achieve common goals.

# Magic Box 




<html lang="en">
<head>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Magic Box</h1>
    <div id="draggable-container">
        <!-- Draggable items will be added here by JavaScript -->
    </div>
        <div id="magic-box">
        <!-- Dropped items will transform here -->
    </div>
</body>
</html>
<script>
document.addEventListener('DOMContentLoaded', () => {
    // 1. Make a connection to the HTML container for draggable items and the magic box
    const draggableContainer = document.getElementById("draggable-container");
    const magicBox = document.getElementById("magic-box");

    // 2. Define the draggable items data
    const items = [
        "Red",
        "Green",
        "Blue",
        "Yellow",
        "Purple"
    ];

    // 3. Create and add draggable items to the container using a for loop
    items.forEach((item, index) => {
        // Create a draggable item
        const draggableItem = document.createElement("div");
        draggableItem.className = "draggable-item";
        draggableItem.textContent = item;

        // Set draggable attribute
        draggableItem.draggable = true;

        // Handle drag start event
        draggableItem.addEventListener("dragstart", function(event) {
            event.dataTransfer.setData("text/plain", item);
        });

        // Append the draggable item to the container
        draggableContainer.appendChild(draggableItem);
    });

    // Handle drag over event to allow drop
    magicBox.addEventListener("dragover", function(event) {
        event.preventDefault(); // Necessary to allow drop
    });

    // Handle drop event to add transformed item to the magic box
    magicBox.addEventListener("drop", function(event) {
        event.preventDefault();

        // Get the dropped item data
        const droppedItem = event.dataTransfer.getData("text/plain");

        // Create a transformed item
        const transformedItem = document.createElement("div");
        transformedItem.className = "transformed-item";
        transformedItem.textContent = droppedItem;

        // Set a random background color
        const randomColor = `hsl(${Math.random() * 360}, 70%, 70%)`;
        transformedItem.style.backgroundColor = randomColor;

        // Set a random position within the magic box
        transformedItem.style.top = `${Math.random() * (magicBox.clientHeight - 50)}px`;
        transformedItem.style.left = `${Math.random() * (magicBox.clientWidth - 50)}px`;

        // Append the transformed item to the magic box
        magicBox.appendChild(transformedItem);
    });
});



</script>


# 
Certainly! Here’s the complete markdown document that integrates challenges faced, a 2-minute summary, Jupyter ideation process, and a coding style question, all in one:

markdown
Copy code
---
layout: base
title: Student Home
description: Home Page
hide: true
---

<img src="https://github.com/iKAN2025.png" class="profile-pic mt-4" alt="Profile Picture" style="display: block; margin: 0 auto;">

<div style="text-align: center;">
  <h2>iKAN2025</h2>
</div>

Hi, I'm iKAN2025, a student at Del Norte High School who is interested in computer science. I am passionate about full-stack development and machine learning. I love solving real-world problems through technology and enjoy collaborating with teams to build innovative solutions.

## Key Interests
- **Technology and Innovation**: Leveraging technology to solve complex problems.
- **Machine Learning and AI**: Developing and implementing intelligent systems.
- **Full Stack Development**: Building comprehensive web applications from front-end to back-end.
- **Team Collaboration**: Working effectively within teams to achieve common goals.

## Color Box 

[Documentation]({{site.baseurl}}/indexdocumententation)
[Ideation]({{site.baseurl}}/indexideation)

Items start out as colorless before they are dragged into the box. 


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="draggable-container">
        <!-- Draggable items will be added here by JavaScript -->
    </div>
    <div id="magic-box">
        <!-- Dropped items will transform here -->
    </div>

        <script>
        <script>
        document.addEventListener('DOMContentLoaded', () => {
            const draggableContainer = document.getElementById("draggable-container");
            const magicBox = document.getElementById("magic-box");

            // Define only 4 draggable items
            const items = [
                { name: "Red", color: "#FF6347" },  // Tomato color
                { name: "Green", color: "#3CB371" }, // Medium Sea Green
                { name: "Blue", color: "#1E90FF" },  // Dodger Blue
                { name: "Yellow", color: "#FFD700" } // Gold
            ];

            items.forEach((item) => {
                const draggableItem = document.createElement("div");
                draggableItem.className = "draggable-item";
                draggableItem.textContent = item.name;
                draggableItem.style.backgroundColor = item.color; // Set initial color
                draggableItem.draggable = true;

                draggableItem.addEventListener("dragstart", function(event) {
                    event.dataTransfer.setData("text/plain", item.color);
                });

                draggableContainer.appendChild(draggableItem);
            });

            magicBox.addEventListener("dragover", function(event) {
                event.preventDefault();
            });

            magicBox.addEventListener("drop", function(event) {
                event.preventDefault();
                const droppedColor = event.dataTransfer.getData("text/plain");
                const transformedItem = document.createElement("div");
                transformedItem.className = "transformed-item";
                transformedItem.style.backgroundColor = droppedColor; // Retain original color
                transformedItem.textContent = "Dropped";
                transformedItem.style.top = `${Math.random() * (magicBox.clientHeight - 50)}px`;
                transformedItem.style.left = `${Math.random() * (magicBox.clientWidth - 50)}px`;

                magicBox.appendChild(transformedItem);
            });
        });
    </script>
</body>
</html>
    </script>
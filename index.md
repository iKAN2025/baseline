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

## Magic Box 

![Documentation]({{site.baseurl}}/indexdocumententation)


<html lang="en">
<style>
    body {
    font-family: Arial, sans-serif;
    margin: 20px;
    padding: 0;
    text-align: center;
}

h1 {
    color: #333;
}

#draggable-container {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-bottom: 20px;
}

.draggable-item {
    width: 100px;
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: center;
    border: 2px solid #333;
    border-radius: 10px;
    background-color: #f0f0f0;
    cursor: pointer;
    user-select: none;
}

#magic-box {
    width: 400px;
    height: 400px;
    border: 2px dashed #333;
    border-radius: 20px;
    margin: 0 auto;
    position: relative;
    background-color: #e0e0e0;
    overflow: hidden;
    text-align: center;
}

.transformed-item {
    position: absolute;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background-color: #000;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 14px;
    font-weight: bold;
}

</style>

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
    const draggableContainer = document.getElementById("draggable-container");
    const magicBox = document.getElementById("magic-box");

    const items = [
        "Red",
        "Green",
        "Blue",
        "Yellow",
        "Purple"
    ];

    items.forEach((item) => {
        const draggableItem = document.createElement("div");
        draggableItem.className = "draggable-item";
        draggableItem.textContent = item;
        draggableItem.draggable = true;

        draggableItem.addEventListener("dragstart", function(event) {
            event.dataTransfer.setData("text/plain", item);
        });

        draggableContainer.appendChild(draggableItem);
    });

    magicBox.addEventListener("dragover", function(event) {
        event.preventDefault();
    });

    magicBox.addEventListener("drop", function(event) {
        event.preventDefault();
        const droppedItem = event.dataTransfer.getData("text/plain");
        const transformedItem = document.createElement("div");
        transformedItem.className = "transformed-item";
        transformedItem.textContent = droppedItem;
        transformedItem.style.backgroundColor = `hsl(${Math.random() * 360}, 70%, 70%)`;
        transformedItem.style.top = `${Math.random() * (magicBox.clientHeight - 50)}px`;
        transformedItem.style.left = `${Math.random() * (magicBox.clientWidth - 50)}px`;

        magicBox.appendChild(transformedItem);
    });
});
</script>
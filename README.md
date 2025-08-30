# firsttask
to-do-list
<!DOCTYPE html>
<html>
<head>
  <title>Simple To-Do</title>
  <style>
    body { font-family: sans-serif; text-align: center; margin-top: 50px; }
    input { padding: 5px; }
    button { padding: 5px 10px; }
    li { margin: 5px 0; }
  </style>
</head>
<body>
  <h2>To-Do List</h2>
  <input id="task" type="text" placeholder="New task">
  <button onclick="addTask()">Add</button>
  <ul id="list"></ul>

  <script>
    function addTask() {
      let task = document.getElementById("task").value;
      if (task === "") return;
      let li = document.createElement("li");
      li.textContent = task;
      li.onclick = () => li.remove(); // Click to remove
      document.getElementById("list").appendChild(li);
      document.getElementById("task").value = "";
    }
  </script>
</body>
</html>


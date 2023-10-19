<!DOCTYPE html>
<html lang="vi">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>App Quản Lý Công Việc</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #4CAF50;
            color: white;
            padding: 20px;
        }

        .task-input {
            margin-bottom: 10px;
        }

        button {
            background-color: #333;
            color: white;
            border: none;
            padding: 10px 15px;
            cursor: pointer;
        }

        .task-list {
            margin-top: 20px;
        }

        .task-item {
            border: 1px solid #333;
            padding: 10px;
            margin-bottom: 10px;
        }
    </style>
</head>

<body>
    <h2>App Quản Lý Công Việc</h2>

    <div class="task-input">
        <label for="task-title">Đầu Việc:</label>
        <input type="text" id="task-title" placeholder="Nhập đầu việc...">
    </div>

    <div class="task-input">
        <label for="task-priority">Hạng Việc:</label>
        <input type="text" id="task-priority" placeholder="Nhập hạng việc...">
    </div>

    <div class="task-input">
        <label for="task-method">Cách Thức Triển Khai:</label>
        <textarea id="task-method" rows="2" placeholder="Nhập cách thức triển khai..."></textarea>
    </div>

    <div class="task-input">
        <label for="task-progress">Đã Tiến Hành:</label>
        <textarea id="task-progress" rows="2" placeholder="Nhập các bước đã tiến hành..."></textarea>
    </div>

    <div class="task-input">
        <label for="task-note">Lưu Ý:</label>
        <textarea id="task-note" rows="2" placeholder="Nhập lưu ý cho công việc..."></textarea>
    </div>

    <div class="task-input">
        <label for="task-time">Thời Gian Hoàn Thành:</label>
        <input type="date" id="task-time">
    </div>

    <button onclick="addTask()">Thêm Việc</button>

    <div class="task-list" id="task-list"></div>

    <script>
        function addTask() {
            const taskTitle = document.getElementById("task-title").value;
            const taskPriority = document.getElementById("task-priority").value;
            const taskMethod = document.getElementById("task-method").value;
            const taskProgress = document.getElementById("task-progress").value;
            const taskNote = document.getElementById("task-note").value;
            const taskTime = document.getElementById("task-time").value;

            const taskItem = document.createElement("div");
            taskItem.className = "task-item";

            taskItem.innerHTML = `
                <h3>${taskTitle}</h3>
                <p><strong>Hạng việc:</strong> ${taskPriority}</p>
                <p><strong>Cách thức triển khai:</strong> ${taskMethod}</p>
                <p><strong>Đã tiến hành:</strong> ${taskProgress}</p>
                <p><strong>Lưu ý:</strong> ${taskNote}</p>
                <p><strong>Thời gian hoàn thành:</strong> ${taskTime}</p>
            `;

            document.getElementById("task-list").appendChild(taskItem);
        }
    </script>
</body>

</html>


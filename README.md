# automatic-timetable-system-
Time Table Scheduling System - College Mini Project
<!-- SUBJECTS -->

<div id="subjects" class="page">

    <div class="box">
        <h2>📚 Add Subject</h2>

        <input type="text" id="subjectName"
               placeholder="Subject Name">

        <input type="text" id="subjectCode"
               placeholder="Subject Code">

        <br>

        <button class="btn" onclick="addSubject()">
            Add Subject
        </button>
    </div>

    <h3>Subject List</h3>

    <table>
        <thead>
            <tr>
                <th>Subject Name</th>
                <th>Subject Code</th>
            </tr>
        </thead>

        <tbody id="subjectList"></tbody>
    </table>

</div>


<!-- CLASSES -->

<div id="classes" class="page">

    <div class="box">
        <h2>🏫 Add Class / Division</h2>

        <input type="text" id="className"
               placeholder="Example: SYBSc IT">

        <input type="text" id="division"
               placeholder="Example: A">

        <br>

        <button class="btn" onclick="addClass()">
            Add Class
        </button>
    </div>

    <h3>Class List</h3>

    <table>
        <thead>
            <tr>
                <th>Class</th>
                <th>Division</th>
            </tr>
        </thead>

        <tbody id="classList"></tbody>
    </table>

</div>


<!-- ROOMS -->

<div id="rooms" class="page">

    <div class="box">
        <h2>🚪 Add Room</h2>

        <input type="text" id="roomName"
               placeholder="Example: Room 101">

        <input type="number" id="capacity"
               placeholder="Capacity">

        <br>

        <button class="btn" onclick="addRoom()">
            Add Room
        </button>
    </div>

    <h3>Room List</h3>

    <table>
        <thead>
            <tr>
                <th>Room</th>
                <th>Capacity</th>
            </tr>
        </thead>

        <tbody id="roomList"></tbody>
    </table>

</div>


<!-- TIME SLOTS -->

<div id="slots" class="page">

    <div class="box">
        <h2>⏰ Add Time Slot</h2>

        <input type="text" id="timeSlot"
               placeholder="Example: 9:00 AM - 10:00 AM">

        <br>

        <button class="btn" onclick="addTimeSlot()">
            Add Time Slot
        </button>
    </div>

    <h3>Time Slot List</h3>

    <table>
        <thead>
            <tr>
                <th>Time Slot</th>
            </tr>
        </thead>

        <tbody id="slotList"></tbody>
    </table>

</div>
<script>addTeacher()function addSubject() {

    let name = document.getElementById("subjectName").value;
    let code = document.getElementById("subjectCode").value;

    if(name === "" || code === "") {
        alert("Please enter subject name and code.");
        return;
    }

    let table = document.getElementById("subjectList");

    let row = table.insertRow();

    row.insertCell(0).innerHTML = name;
    row.insertCell(1).innerHTML = code;

    document.getElementById("subjectName").value = "";
    document.getElementById("subjectCode").value = "";
}


function addClass() {

    let className = document.getElementById("className").value;
    let division = document.getElementById("division").value;

    if(className === "" || division === "") {
        alert("Please enter class and division.");
        return;
    }

    let table = document.getElementById("classList");

    let row = table.insertRow();

    row.insertCell(0).innerHTML = className;
    row.insertCell(1).innerHTML = division;

    document.getElementById("className").value = "";
    document.getElementById("division").value = "";
}


function addRoom() {

    let room = document.getElementById("roomName").value;
    let capacity = document.getElementById("capacity").value;

    if(room === "" || capacity === "") {
        alert("Please enter room and capacity.");
        return;
    }

    let table = document.getElementById("roomList");

    let row = table.insertRow();

    row.insertCell(0).innerHTML = room;
    row.insertCell(1).innerHTML = capacity;

    document.getElementById("roomName").value = "";
    document.getElementById("capacity").value = "";
}


function addTimeSlot() {

    let time = document.getElementById("timeSlot").value;

    if(time === "") {
        alert("Please enter a time slot.");
        return;
    }

    let table = document.getElementById("slotList");

    let row = table.insertRow();

    row.insertCell(0).innerHTML = time;

    document.getElementById("timeSlot").value = "";
}

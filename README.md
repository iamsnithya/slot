# Ex03 Time Table
## Date:

## AIM
To write a html webpage page to display your slot timetable.

## ALGORITHM
### STEP 1
Create a Django-admin Interface.

### STEP 2
Create a static folder and inert HTML code.

### STEP 3
Create a simple table using ```<table>``` tag in html.

### STEP 4
Add header row using ```<th>``` tag.

### STEP 5
Add your timetable using ```<td>``` tag.

### STEP 6
Execute the program using runserver command.

## PROGRAM

    <!DOCTYPE html>
    <html lang="en">
    <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Semester Timetable</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f5f5f5;
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }
        
        .container {
            max-width: 800px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            padding: 20px;
            margin: 0 auto;
        }
        
        .college-header {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
            border-bottom: 2px solid #ddd;
            padding-bottom: 15px;
        }
        
        .college-logo {
            width: 600px;
            height: 70px;
            margin-right: 15px;
        }
        
        .college-name {
            flex: 1;
        }
        
        .college-name h1 {
            color: #1a4789;
            margin: 0;
            font-size: 24px;
            font-weight: bold;
        }
        
        .college-name p {
            color: #555;
            margin: 5px 0 0;
            font-size: 14px;
        }
        
        .college-code {
            background-color: #1a4789;
            color: white;
            padding: 8px 15px;
            border-radius: 5px;
            font-weight: bold;
            font-size: 20px;
        }
        
        .autonomous-tag {
            background-color: #e63946;
            color: white;
            padding: 3px 10px;
            border-radius: 3px;
            font-size: 14px;
            font-weight: bold;
            margin-left: 10px;
        }
        
        .student-info {
            background-color: #f9f9f9;
            padding: 12px;
            text-align: center;
            margin-bottom: 20px;
            border-radius: 5px;
            font-weight: bold;
            font-size: 18px;
        }
        
        .timetable {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 25px;
        }
        
        .timetable th, .timetable td {
            border: 2px solid #1a4789;
            padding: 10px;
            text-align: center;
        }
        
        .timetable th {
            background-color: #ffd100;
            color: #000;
            font-weight: bold;
        }
        
        .timetable td {
            background-color: #99e6ff;
        }
        
        .timetable .lunch {
            background-color: #ffd100;
            font-weight: bold;
            letter-spacing: 2px;
        }
        
        .free-slot {
            background-color: #99e6ff;
        }
        
        .subjects {
            width: 100%;
            border-collapse: collapse;
        }
        
        .subjects th, .subjects td {
            border: 1px solid #ddd;
            padding: 10px;
            text-align: left;
        }
        
        .subjects th {
            background-color: #f2f2f2;
            font-weight: bold;
        }
        
        .subjects tr:nth-child(even) {
            background-color: #f9f9f9;
        }
        
        .subjects tr:hover {
            background-color: #f1f1f1;
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 10px;
            }
            
            .college-header {
                flex-direction: column;
                text-align: center;
            }
            
            .college-logo {
                margin-right: 0;
                margin-bottom: 10px;
            }
            
            .college-code {
                margin-top: 10px;
            }
            
            .timetable th, .timetable td, .subjects th, .subjects td {
                padding: 5px;
                font-size: 14px;
            }
        }
    </style>
    </head>
    <body>
    <div class="container">
        <div class="college-header">
            <img src="https://ik.imagekit.io/0tydz7atd/Screenshot%202025-05-02%20110849.png?updatedAt=1746164347546" alt="College Logo" class="college-logo">
            
        </div>
        
        <div class="student-info">
            SLOT TIME TABLE 
        </div>
        
        <table class="timetable">
            <thead>
                <tr>
                    <th>Day/Time</th>
                    <th>Monday</th>
                    <th>Tuesday</th>
                    <th>Wednesday</th>
                    <th>Thursday</th>
                    <th>Friday</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <th>8-10</th>
                    <td>MAT</td>
                    <td colspan="3" class="free-slot">FREE SLOT</td>
                    <td>PHY</td>
                </tr>
                <tr>
                    <th>10-12</th>
                    <td>CS</td>
                    <td>FREE SLOT</td>
                    <td>UD</td>
                    <td>MAT</td>
                    <td>PHY</td>
                </tr>
                <tr>
                    <th>12-1</th>
                    <td colspan="5" class="lunch">L U N C H</td>
                </tr>
                <tr>
                    <th>1-3</th>
                    <td colspan="2" class="free-slot">FREE SLOT</td>
                    <td>MAT</td>
                    <td>FWAD</td>
                    <td>CS</td>
                </tr>
                <tr>
                    <th>3-5</th>
                    <td>FREE SLOT</td>
                    <td>MAT</td>
                    <td>CS</td>
                    <td>PHY</td>
                    <td>UD</td>
                </tr>
            </tbody>
        </table>
        
        <table class="subjects">
            <thead>
                <tr>
                    <th>S. No.</th>
                    <th>Subject Code</th>
                    <th>Subject Name</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>1.</td>
                    <td>19AI414</td>
                    <td>Fundamentals of Web Application Development (WDT)</td>
                </tr>
                <tr>
                    <td>2.</td>
                    <td>19CS406</td>
                    <td>Computer Networks (CN)</td>
                </tr>
                <tr>
                    <td>3.</td>
                    <td>20PH206</td>
                    <td>Physics for Computer Science (PHY)</td>
                </tr>
                <tr>
                    <td>4.</td>
                    <td>20MA201</td>
                    <td>Applied Mathematics and Statistics (MAT)</td>
                </tr>
                <tr>
                    <td>5.</td>
                    <td>19CS549</td>
                    <td>UI and UX Design (UD)</td>
                </tr>
            </tbody>
        </table>
    </div>
    </body>
    </html>


## OUTPUT
![Screenshot 2025-05-02 112030](https://github.com/user-attachments/assets/1fb0e797-dc38-4480-bd75-0a3e83c25f35)



## RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.

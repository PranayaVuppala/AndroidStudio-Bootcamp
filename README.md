# AndroidStudio-Bootcamp
# Android App Development Bootcamp & Appathon - 2024
### Sri Vishnu Engineering College For Women, Bhimavaram


#### Introduction to android eco-system & Platform Architecture [Slides](https://docs.google.com/presentation/d/1OYM4unFukbCV9q1NBmmm2ODbx1mU-Smjuo4Re6SNSTs/edit#slide=id.g116d7d9d49_3_13)

#### Access my free e-book that contains 40 chapters on Android App Development [ebook Link](https://android-app-development-documentation.readthedocs.io/en/latest/)

#### 24-Sep-2024
**Agenda**
- Introduction to Android
- Installation of Android Studio
- Installation of Android Virtual Device (Emulator)
- Connecting your physical device to android studio
- Creating the first app and running it
- Project Structure
- Brief about the app that we are going to develop tomorrow

**Installation of Android Studio**  
***Pre-requisite***
- i3/i5 based processors
- 8GB Recommended
- 20GB of Available space
- Good Internet

***Procedure***
- Go to this [link](https://developer.android.com/studio) and download android studio
- Follow the instructions of installation [here](https://developer.android.com/studio/install)
- Drop an email to [pavankreddy.t@gmail.com](pavankreddy.t@gmail.com)

**Installation of Android Virtual Device (Emulator)**

[Official Documentation - AVD (Android Virtual Device)](https://developer.android.com/studio/run/managing-avds)

[Official Documentation - Connecting Physical Device](https://developer.android.com/studio/run/device)

**Creating the first app and running it**  

**Project Structure**
[Official Documentation](https://developer.android.com/studio/projects)

**Brief about the app that we are going to develop tomorrow**

![Scorekeeper](/scorekeeper.png)

#### 25-09-2024
**Agenda**
- Design the Score keeper app
  - Views, ViewGroups & Layouts
  - XML Design
- Get the app into action
- Design for landscape
- Themes

**What is a view ?**
- All UI Components in android are called as Views
- View is the super class of all UI classes
- Examples: Buttons, EditText, TextViews, RecyclerView etc.,  
[officialDoc](https://developer.android.com/reference/android/view/View)   

**What is a ViewGroup ?**
- A ViewGroup is also a View that can accommodate other views inside it. 
- Ex: LinearLayout, constraintLayout, RecyclerView and etc.,  
[Official Doc](https://developer.android.com/reference/android/view/ViewGroup)  

**Layout**  
- Layout offers the basic structure of the design of your activity (A single screen)
- Ex: LinearLayout, ConstraintLayout, FrameLayout and etc.,  
[official Doc](https://developer.android.com/develop/ui/views/layout/declaring-layout)


![vvgl](/vvgl.png)

![vvgl2](/vvgl2.png)

- Desinging seperately for landscape 
- SaveInstanceState


### Day 1  (BootCamp)
[ListView](https://developer.android.com/reference/android/widget/ListView)

[Recyclerview](https://developer.android.com/develop/ui/views/layout/recyclerview)
[Slides](https://docs.google.com/presentation/d/1nFJqH0OSSZmjaycRzEGE6vvsm6jlxghQyoO15KKbkwc/edit#slide=id.p)

#### Assignment -  1 
Try Staggered Grid Layout Manager and display the data. [Favorite Actors]

[Github Public Apis](https://github.com/public-apis/public-apis)

#### Assignment 2
Try to get the books data and show it on recyclerview along with images. and after selecting one item, show the details of the item in another activity. 

|Videos|Length|Link
| ----- | :---: | :---: |
| Introduction to Chapter \- 2 | 4 | [https://youtu.be/aVmWnUVA7iU](https://youtu.be/aVmWnUVA7iU) |
| Explicit Intents | **16** | [https://youtu.be/te0n3Vn9aik](https://youtu.be/te0n3Vn9aik) |
| Passing Data | **12** | [https://youtu.be/MmcWLiWNTAI](https://youtu.be/MmcWLiWNTAI) |
| Android Activity Stack (TASKS) | **3** | [https://youtu.be/7JcqB6VRoto](https://youtu.be/7JcqB6VRoto) |
| Implicit Intents | **17** | [https://youtu.be/Q0bLt9HHONc](https://youtu.be/Q0bLt9HHONc) |
| Android Activity Lifecycle | **15** | [https://youtu.be/pZz8d-aw5OU](https://youtu.be/pZz8d-aw5OU) |
| Summary of Chapter 2 and Next Steps | **2** | [https://youtu.be/zZWI4F8rmXg](https://youtu.be/zZWI4F8rmXg) |
| Exploring UI Components \- Building Registration Form App Part \- 1 | **16** | [https://youtu.be/\_VePheWeatY](https://youtu.be/_VePheWeatY) |
| Exploring UI Components \- Building Registration Form App Part \- 2 | **8** | [https://youtu.be/GfXNN7bJ-h4](https://youtu.be/GfXNN7bJ-h4) |
| Android Input Controls | 20 | [https://youtu.be/m60-zC0k-I8](https://youtu.be/m60-zC0k-I8) |


#### Question
android:usesCleartextTraffic="true

what does it do ?


**Agenda**  
- Volley
- SharedPreferences
- SQLite
- Firebase Realtime Databases


Here's a step-by-step tutorial for Module 2 of your Jetpack Compose course, focusing on building a "Task Manager App." We'll break down the concepts and immediately apply them to our project. The goal is to create a task list where users can add, display, and manage tasks using Jetpack Compose.

### Module 2: Composables and Layouts (Building Project 1: Task Manager App)

#### 1. Understanding Composables
_Composables_ are the building blocks of Jetpack Compose. They are functions that define the UI in a declarative way. Every UI component, from a button to a list, is created using composable functions.

##### Step 1: Basic Composables
Let's create a simple UI with some of the basic composable elements like `Text`, `Button`, and `Image` to get started.

```kotlin
@Composable
fun Greeting() {
    Text(text = "Welcome to the Task Manager App!")
}

@Composable
fun SimpleButton() {
    Button(onClick = { /* Action to perform */ }) {
        Text(text = "Add Task")
    }
}
```

- `Text`: Displays text on the screen.
- `Button`: A clickable button that triggers actions when pressed.

##### Step 2: Creating a Task Item Composable
Next, we'll create a composable that represents a task in our task list. This composable will be reusable for each task.

```kotlin
@Composable
fun TaskItem(taskName: String) {
    Row(
        modifier = Modifier
            .padding(8.dp)
            .fillMaxWidth(),
        horizontalArrangement = Arrangement.SpaceBetween
    ) {
        Text(text = taskName)
        Button(onClick = { /* Mark task as complete */ }) {
            Text(text = "Complete")
        }
    }
}
```

- `Row`: Arranges items horizontally.
- `Modifier`: Used to add spacing, alignment, and styling to the composable.

#### 2. Layout and Design Principles

##### Step 1: Implementing Layouts with Column, Row, Box, and LazyColumn
Let's build the layout for displaying a list of tasks. We'll use `Column` to arrange items vertically and `LazyColumn` for efficient scrolling when the list grows.

```kotlin
@Composable
fun TaskList(tasks: List<String>) {
    LazyColumn {
        items(tasks) { task ->
            TaskItem(taskName = task)
        }
    }
}
```

- `LazyColumn`: A vertically scrolling list that only renders items currently visible on the screen, improving performance.
- `items`: A function used within `LazyColumn` to display each task in the list.

##### Step 2: Styling with Modifier
We'll use the `Modifier` parameter to add padding and other styling to our components.

```kotlin
@Composable
fun StyledTaskItem(taskName: String) {
    Row(
        modifier = Modifier
            .padding(16.dp)
            .fillMaxWidth()
            .background(Color.LightGray),
        horizontalArrangement = Arrangement.SpaceBetween
    ) {
        Text(text = taskName, style = TextStyle(fontWeight = FontWeight.Bold))
        Button(onClick = { /* Action to mark task complete */ }) {
            Text(text = "Complete")
        }
    }
}
```

- `background`: Sets the background color of the component.
- `padding`: Adds space around the content.

#### 3. Building Task Manager Features

##### Step 1: Adding Tasks to the List
To make the app interactive, let's create a UI component that allows users to add tasks to the list.

```kotlin
@Composable
fun AddTaskInput(onAddTask: (String) -> Unit) {
    var taskName by remember { mutableStateOf("") }

    Row(modifier = Modifier.padding(8.dp)) {
        TextField(
            value = taskName,
            onValueChange = { taskName = it },
            placeholder = { Text(text = "Enter task") },
            modifier = Modifier.weight(1f)
        )
        Button(onClick = { onAddTask(taskName); taskName = "" }) {
            Text(text = "Add")
        }
    }
}
```

- `TextField`: A composable for text input.
- `remember`: Used to remember the state of the task input field.
- `onAddTask`: A callback that gets triggered when a task is added.

##### Step 2: Displaying and Updating the Task List
Now let's combine everything to manage the list of tasks, add new ones, and mark tasks as complete.

```kotlin
@Composable
fun TaskManagerApp() {
    var tasks by remember { mutableStateOf(listOf<String>()) }

    Column(modifier = Modifier.padding(16.dp)) {
        AddTaskInput { newTask ->
            tasks = tasks + newTask
        }
        Spacer(modifier = Modifier.height(8.dp))
        TaskList(tasks = tasks)
    }
}
```

- `tasks`: Holds the list of tasks in the app's state.
- `AddTaskInput`: Adds new tasks to the list.
- `TaskList`: Displays all tasks.

### Bringing It All Together
Here's the complete composable to run the Task Manager app:

```kotlin
@Composable
fun TaskManagerApp() {
    var tasks by remember { mutableStateOf(listOf<String>()) }

    Column(modifier = Modifier.padding(16.dp)) {
        Text(text = "Task Manager", style = TextStyle(fontSize = 24.sp, fontWeight = FontWeight.Bold))
        AddTaskInput { newTask ->
            tasks = tasks + newTask
        }
        Spacer(modifier = Modifier.height(8.dp))
        LazyColumn {
            items(tasks) { task ->
                TaskItem(taskName = task)
            }
        }
    }
}
```

This setup allows users to:
- Add new tasks using an input field.
- Display tasks in a scrollable list.
- Mark tasks as complete dynamically.

### Next Steps
- Add animations to the task list for smoother transitions.
- Enhance the UI with colors, icons, and themes.
- Implement task persistence to save data when the app is closed.

This approach covers the foundational aspects of using composables and layouts in Jetpack Compose, all while building a fully functional Task Manager app.
 

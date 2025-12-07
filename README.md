# Anime Pomodoro

A modern, visually appealing, and fully interactive Pomodoro timer built using **HTML**, **CSS**, and **JavaScript**. This application includes real-time clock display, customizable backgrounds, a task manager, and a clean glassmorphism user interface.

---

## 🚀 Features

### ⏱️ Pomodoro Timer

* Three modes:

  * **Work (25 mins)**
  * **Short Break (5 mins)**
  * **Long Break (15 mins)**
* Start, pause, and reset controls
* Smooth animated UI with glass-style components
* Automatic alarm sound when session ends

### 🕒 Live Clock & Date

* Displays current time (HH:MM:SS)
* Shows full weekday and date
* Updates every second

### ✔️ Task Manager

* Add tasks with a single click or Enter key
* Mark tasks as completed
* Delete tasks instantly
* Attractive list design with scroll support when long

### 🖼️ Dynamic Background Selector

* Choose from 10 aesthetic background images
* Beautiful image preview buttons
* Smooth fade change effect

### 📱 Fully Responsive

* Works on desktops, tablets, and smartphones
* UI scales elegantly for different screen sizes

---

## 📂 Project Structure

```
project-folder/
│
├── index.html        # Main application
├── 1.jpg
├── 2.png
├── 3.jpg
├── ...               # Background images
└── 10.jpg
```

Make sure to place all background images in the same directory as `index.html` for correct loading.

---

## 🛠️ Technologies Used

* **HTML5** — Structure
* **CSS3** — Glassmorphistic design, layout, responsiveness
* **JavaScript (ES6)** — Timer logic, tasks, background switching, live clock

---

## 📘 How It Works

### 1. **Timer Logic**

* Uses `setInterval()` to count down every second
* Displays formatted time as MM:SS
* Pauses by clearing the interval
* Resets to the current mode's default time

### 2. **Modes**

Each mode button has a `data-mode` and `data-time` attribute:

```html
<button class="mode-btn" data-mode="work" data-time="25">Work</button>
```

Switching mode updates:

* Timer label
* Timer value
* Button styling

### 3. **Tasks**

Tasks are stored in an array:

```js
{ id: 123456789, text: "Task content", completed: false }
```

Rendering is done inside the `tasksList` container.

### 4. **Background Switching**

Each image button triggers:

```js
backgroundImage.style.backgroundImage = `url(${backgrounds[index]})`;
```

Also updates UI state for selected background.

---

## 🔊 Audio

The alarm uses a Google-hosted open sound:

```
https://actions.google.com/sounds/v1/alarms/alarm_clock.ogg
```

If audio autoplay fails, the user must press the timer once to allow sound permissions.

---

## 🧩 Customization

### Change Timer Durations

Modify these three buttons:

```html
<button data-time="25">Work</button>
<button data-time="5">Short Break</button>
<button data-time="15">Long Break</button>
```

### Add More Background Images

1. Add file to project folder (e.g., `11.jpg`)
2. Add to JS array:

```js
backgrounds.push("11.jpg");
```

### Modify Colors

All styling is located in the `<style>` section. Key color tokens:

* Background: `#1a1a2e`
* Glass card overlay: `rgba(255, 255, 255, 0.15)`
* Text shadows & transitions

---

## 📦 How to Run

No build tools required.
Just open **index.html** in a browser:

```
Right-click → Open with → Chrome/Edge/Firefox
```
OR

Click Here: https://anime-pomodoro.netlify.app/

---

## 📝 License

This project is free to use, modify, and integrate into personal or educational projects.

---

## ❤️ Credits

Designed and developed with a focus on aesthetics and productivity.
Feel free to improve or extend it!


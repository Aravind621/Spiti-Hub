# Spiti Hub

Spiti Hub is a frontend-centric web application designed for listing and renting homes. It allows users to register, log in, explore homes, and interact with forms—entirely on the client side, without the need for a backend server or database!

## Features

- **User Authentication**: Register and log in seamlessly.
- **Client-Side Storage**: All user credentials and data are stored locally in the browser using HTML5 `localStorage`.
- **Property Listings**: Explore available simulated houses for rent.
- **Form Submission Mockups**: Feedback, contact, and home listing forms simulate real submission workflows locally.

---

## 🚀 How to Run the App

Because this project has been converted from PHP to use pure frontend technologies (HTML, CSS, JavaScript), you **do not** need a local server (like XAMPP or WAMP) or a MySQL database to run it. 

### **Option 1: Direct Execution (Fastest)**

1. Navigate to your project folder (`spity-hub-main`).
2. Double-click the `home.html` file to open it in your preferred web browser (Google Chrome, Edge, Firefox, Safari).
3. The app is completely functional right out of the box! You can now start registering a new user.

### **Option 2: Using Visual Studio Code Live Server**

1. Open the `spity-hub-main` folder in **Visual Studio Code**.
2. Install the **Live Server** extension by *Ritwick Dey* (if you don't already have it).
3. Right-click on `home.html` and select **"Open with Live Server"**.
4. Your browser will automatically launch the app on a local development port (typically `http://127.0.0.1:5500/home.html`).

---

## 🔐 Data Storage: Where is it stored?

Instead of relying on a traditional SQL database, all application data logic is powered by **Browser LocalStorage**. LocalStorage provides a way for web pages to store key/value pairs locally inside the user's web browser, and the data is preserved seamlessly even after the browser window is closed or refreshed.

### **How it works:**
1. **Registration Flow**: When you submit your details inside `register.html`, the app intercepts your entry form and converts your information (Email, Username, Phone, Password) into a JavaScript Object format. It then saves this information directly to the browser storage under an array list called `"users"`.
2. **Login Flow**: When you open `login.html` and attempt to log in, the app pulls the `"users"` array from LocalStorage and cross-references your inputs against it to grant you access.

### **How to see your data:**
If you want to look at the exact data you've registered with:
1. Open the application in your browser (e.g., Google Chrome).
2. Right-click anywhere on the page and select **"Inspect"** or **"Inspect Element"** (or press your `F12` key / `Ctrl+Shift+I`).
3. In the Developer Tools window that pops up, look at the top bar and navigate to the **Application** tab (if you're using Firefox, it will be called the **Storage** tab).
4. On the left sidebar, click the dropdown arrow next to **Local Storage**.
5. Select the URL associated with this project (if you opened it directly, it will look like `file://`. If you used Live Server, it will look like `http://127.0.0.1:5500`).
6. You will see Keys like `"users"` and `"currentUser"`. Clicking on them will allow you to see exactly what user data the app has memorized!

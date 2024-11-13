# ant-devmode-mit-app-inventor

To set up hot-reloading with **Super Dev Mode** in MIT App Inventor, you can use **GWT (Google Web Toolkit)**'s `Super Dev Mode`, which makes it easy to see live code changes without restarting the server each time. Here’s a guide for setting it up in App Inventor’s environment.

---

### Step 1: Build and Run the GWT CodeServer

1. **Navigate to the MIT App Inventor Source Code Directory**:
   Make sure you're in the main directory of the MIT App Inventor source code.

2. **Run the GWT Dev Mode**:
   You’ll need to use Apache Ant (the build tool) to start the `devmode` target in MIT App Inventor. This will build the project in **Super Dev Mode**.
   ```bash
   ant devmode
   ```

3. **Start the App Inventor Server**:
   In another terminal window, start the main server if it’s not already running. This server runs on `localhost:8888` by default and will serve the App Inventor web interface.
   ```bash
   ant RunLocalBuildServer
   ```

---

### Step 2: Open the GWT CodeServer

1. **Open the CodeServer UI**:
   Open your browser and navigate to:
   ```
   http://localhost:9876/
   ```
   This is the GWT CodeServer interface.

2. **Drag the Bookmarklets**:
   You will see two links in the CodeServer UI:
   - **Dev Mode On**
   - **Dev Mode Off**

   Drag these bookmarklets to your browser’s bookmarks bar. They allow you to toggle Super Dev Mode on or off.

---

### Step 3: Enable Super Dev Mode in Your Project

1. **Open MIT App Inventor in Your Browser**:
   Go to `http://localhost:8888` to access your local version of App Inventor.

2. **Turn On Super Dev Mode**:
   - Open any page where you’d like to test hot-reloading.
   - Click the **Dev Mode On** bookmarklet from your bookmarks bar.
   - When you make changes to the Java code in the GWT project, save your changes.

3. **Compile and Refresh**:
   - Return to the CodeServer page (`http://localhost:9876`) and hit the “Compile” button to apply your code changes.
   - Refresh the App Inventor page, and you should see your changes without restarting the server.

---

### Additional Notes:

- **Java and GWT Changes**: Only Java code within GWT modules will reload. Changes to non-GWT Java files (like back-end services) may still require a server restart.
- **JavaScript or CSS Changes**: For front-end changes not in Java, you may need to manually refresh your browser.

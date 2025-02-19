debugging streamlit with VS Code see here:

https://abc-notes.data.tech.gov.sg/notes/topic-7-quick-prototyping-with-streamlit/4.-debugging-streamlit-apps-in-vs-code.html#:~:text=Go%20to%20the%20Run%20view.,press%20F5%20to%20start%20debugging.



# Setting Up Python Debugger in Visual Studio Code

Let's dive into the practical steps of setting up and using the Python Debugger in VS Code for our Streamlit app.

Here, we assume we all have installed and set up our Visual Studio code correctly for Streamlit app development. For details on setting up, see [3. Setting Up Streamlit Project with pip and venv](https://abc-notes.data.tech.gov.sg/notes/topic-7-quick-prototyping-with-streamlit/2.-setting-up-streamlit-project-with-pip-and-venv.html) from Topic 7.

Install the `Python Debugger` extension developed by Microsoft.

![](https://abc-notes.data.tech.gov.sg/notes/lib/media/img-20240909132900202.png)

---

Step 1: Configure the Debugger

To configure the debugger, we need to create a `launch.json` file in our project. This file contains the configuration settings for debugging.

1. Open your Streamlit project in VS Code.
2. Go to the Run view by clicking on the Run icon in the Activity Bar or by pressing `Ctrl+Shift+D`.
3. Click on "create a launch.json file" link.
4. Select "Python" from the list of environments.
5. A `launch.json` file will be created with a default configuration. Modify it to match the following configuration:

```json
{
    "configurations": [
        {
            "name": "Streamlit Debug",
            "type": "python",
            "request": "launch",
            "module": "streamlit",
            "args": [
                "run",
                "${file}"
            ]
        }
    ]
}
Copy
```

---

Step 3: Set Breakpoints

Breakpoints allow us to pause the execution of our code at specific lines, so we can inspect variables and the program state.

1. Open the Streamlit app file in VS Code.
2. Click in the gutter to the left of the line numbers where you want to set a breakpoint. A red dot will appear, indicating the breakpoint.

---

Step 4: Start Debugging

Now that we have configured the debugger and set breakpoints, we can start debugging.

1. Go to the Run view.
2. Select "Python: Streamlit" from the dropdown menu.
3. Click the green play button or press `F5` to start debugging.

VS Code will launch the Streamlit app and pause execution at the breakpoints we set. We can now inspect variables, step through the code, and evaluate expressions in the Debug Console.

---

Step 5: Inspect Variables and Step Through Code

While debugging, we can use the following controls:

* ✦  **Continue (`F5`)** : Resume execution until the next breakpoint.
* ✦  **Step Over (`F10`)** : Execute the next line of code, but don't step into functions.
* ✦  **Step Into (`F11`)** : Step into functions to see their execution.
* ✦  **Step Out (`Shift+F11`)** : Step out of the current function.
* ✦  **Restart (`Ctrl+Shift+F5`)** : Restart the debugging session.
* ✦  **Stop (`Shift+F5`)** : Stop the debugging session.

We can also hover over variables to see their current values or use the Variables pane to inspect them.

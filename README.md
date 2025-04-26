# Python Dev Container Starter

This is a minimal starter project for Python development using Docker containers and VSCode Dev Containers.

---

## How to Use

1. Install **Docker Desktop** and **VSCode**.
2. Install the **Dev Containers** extension in VSCode (Microsoft).
3. Clone this repository:
   ```bash
   gh repo clone sheepnir/my-python-container-project
   ```
4. Open the project folder in VSCode.
5. When prompted, click **"Reopen in Container"**.

---

## Development Workflow

### To start coding:
- Open the folder in VSCode.
- It will automatically build and start the container.
- Your code (inside `/app`) will be live inside the container.
- Modify any Python file — no need to rebuild unless you change Python packages.

### To install new Python packages:
1. Add the package name to `requirements.txt`.
2. Rebuild the container:
   - Open Command Palette (`Cmd + Shift + P`) → **Dev Containers: Rebuild Container**.
   - Or click the green corner button in VSCode and select **Rebuild Container**.

### To run the application:
1. Open a terminal in VSCode (inside the container).
2. Run:
   ```bash
   python main.py
   ```
3. The Flask app will start and listen on `0.0.0.0:5000`.

---

## Accessing the Application from Your Machine

Even though the app runs inside a container, it will be **automatically forwarded** to your Mac.

Open your browser and navigate to:

```
http://localhost:5000
```

You should see:
> Hello from inside the container!

---

## Gracefully Shutting Down and Switching Projects

When you are done working on this project and want to switch:

1. Simply **close the VSCode window**.
2. This automatically stops and removes the running container.
3. Open your next project folder and "Reopen in Container" if needed.

Alternatively, you can manually stop containers via Docker Desktop.

---

## Useful Commands

| Task | Command |
|:-----|:--------|
| Rebuild container after changing requirements | `Dev Containers: Rebuild Container` |
| Open a shell inside the container | Open Terminal in VSCode |
| Stop container | Close VSCode window or use Docker Desktop |

---

Your Mac remains clean, and each project stays fully isolated inside its container.

---

Happy Coding!
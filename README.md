# GitHub Actions – Python Demo Project

## Jenkins vs GitHub Actions

Both Jenkins and GitHub Actions are CI/CD automation tools used to automate tasks such as building, testing, and deploying applications.

## Advantages of GitHub Actions over Jenkins

- ☁️ **Hosting:** Jenkins needs a separate server, while GitHub Actions is hosted by GitHub.
- 🎨 **User Interface:** GitHub Actions has a simple and user-friendly interface.
- 💰 **Cost:** GitHub Actions is free for public repositories and offers free usage limits for private repositories. Jenkins is self-hosted, so server and maintenance costs may apply.
- 🔗 **GitHub Integration:** GitHub Actions is directly integrated with GitHub repositories and workflows.

---

## Advantages of Jenkins over GitHub Actions

- 🔧 **Flexibility:** Jenkins provides more flexibility for complex CI/CD pipelines.
- 🔌 **Integrations:** Jenkins has a large plugin ecosystem and can integrate with many tools and platforms.
- 🖥️ **Self-Hosted:** Jenkins can be installed and controlled on your own infrastructure.
- ⚙️ **Customization:** Jenkins offers extensive customization for complex automation requirements.

---

## Conclusion

**Jenkins** is a good choice for complex and highly customized CI/CD pipelines.

**GitHub Actions** is a simple and convenient choice when your code is hosted on GitHub and you want GitHub-integrated automation.

# Project Overview


In this project, I am creating a simple Python Flask application and using **GitHub Actions** to understand how CI/CD automation works. The main goal is to understand how a GitHub Actions workflow is automatically triggered when changes are pushed to the `main` branch.

### ⚡ What will happen?

Whenever I make a change in the Python application and **push/commit the changes to the `main` branch**, GitHub Actions will automatically be triggered.

After the workflow is triggered, GitHub Actions will:

1. 📥 Checkout the latest code from the repository.
2. 🖥️ Start a GitHub-hosted Ubuntu runner.
3. ⚙️ Execute the defined command.
4. 📝 Display the output in the GitHub Actions logs.

For this demo, the action we perform is simply:

```text
"Python app code was updated!"
```

## 🟢 Step 1: Create a GitHub Repository

Create a new repository on GitHub.

Repository name:
```text
github-actions-python-demo
```

## 🟢 Step 2: Create the Python Application

Add file → Create new file

Create a file named:
```text
python.py
```

Add the following code:
```text
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello, this is my Python App!"

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=5000)
```

Commit the changes.

### What does this application do?

This is a simple Flask web application. When the application runs on:

```text
http://localhost:5000
```
it displays:

```text
Hello, this is my Python App!
```

This application is only being used as a demo application for learning GitHub Actions.

## 🟢 Step 3: Create GitHub Actions Workflow

Inside the same GitHub repository, create:
```text
.github/workflows/action.yml
```

The repository structure will look like:

```text
github-actions-python-demo/
├──
├── app.py
│
└── .github/
    └── workflows/
        └── action.yml
```





















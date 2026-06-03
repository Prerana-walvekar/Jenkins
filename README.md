# CI Setup Using Jenkins, GitHub and Maven

## 📌 Step 1: Verify Required Tools

Check installed tools:

```bash
git --version
java -version
mvn -version
jenkins --version
```

Ensure Jenkins service is running:

```bash
sudo systemctl status jenkins
```

---

## 📌 Step 2: Clone Repository from GitHub

```bash
git clone <repository_url>
cd repository_name
```

---

## 📌 Step 3: Push Project to GitHub Repository

Initialize Git (if required):

```bash
git init
git add .
git commit -m "Initial project commit"
```

Connect to GitHub repository:

```bash
git remote add origin <github_repository_url>
```

Push the project:

```bash
git push -u origin main
```

---

## 📌 Step 4: Open Jenkins Dashboard

1. Open browser:
```
http://localhost:8080
```

2. Login to Jenkins.

---

## 📌 Step 5: Create Jenkins Freestyle Job

1. Click **New Item**
2. Enter Job Name
3. Select **Freestyle Project**
4. Click OK

---

## 📌 Step 6: Configure Git Repository in Jenkins

- Go to **Source Code Management**
- Select **Git**
- Enter repository URL:

```
https://github.com/username/repository_name.git
```

---

## 📌 Step 7: Configure Build Step

- Go to **Build Section**
- Click **Add Build Step**
- Select **Invoke top-level Maven targets**
- Enter goals:

```
clean install
```

---

## 📌 Step 8: Save and Build

- Click **Save**
- Click **Build Now**

---

## 📌 Step 9: Check Build Result

1. Go to **Build History**
2. Click latest build
3. Open **Console Output**

Expected:
```
BUILD SUCCESS
```

---

## 🎯 Result

CI pipeline successfully implemented using Jenkins, GitHub, and Maven on Ubuntu.

# Recipe Bot - Rasa

## Introduction
This is a **Rasa-powered chatbot** that helps you find recipes. Follow the steps below to set up and run the bot using **Docker**.

---

## Prerequisites
Before you begin, ensure you have the following installed:
- **Docker Desktop** ([Download here](https://www.docker.com/get-started))

---

## Installation & Setup
### **Step 1: Install Docker**
Download and install **Docker Desktop** if you haven’t already.

### **Step 2: Pull Rasa Image**
Run the following command to pull the latest Rasa image:
```sh
docker pull rasa/rasa:latest
```

### **Step 3: Initialize the Project**
Replace `[your file path]` with the actual path where you want to store the bot files.
```sh
docker run -it --rm -v [your file path]:/app rasa/rasa:latest init --no-prompt
```

### **Step 4: Train the Model**
Once the project is initialized, train the chatbot:
```sh
docker run -it --rm -v [your file path]:/app rasa/rasa:latest train
```

### **Step 5: Run the Chatbot**
After training completes, start the chatbot:
```sh
docker run -it --rm -v [your file path]:/app rasa/rasa:latest shell
```

---

## Usage
Now you can start chatting with the bot and ask for recipes!

Example:
```
You: Hi
Bot: Hey! How are you?

You: Can you give me a recipe for Paneer Butter Masala?
Bot: Here’s the recipe for Paneer Butter Masala...
```

---

## Notes
- Every time you make changes in domain , rules or nlu [these yml files], retrain the bot using **Step 4**.
- If you encounter issues, make sure Docker is running and the file paths are correct.

---

### Enjoy cooking with your personal **Recipe Bot**! 🍽️


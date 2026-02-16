# 🤝 Contributing to MovieMatch

First off, thank you for considering contributing to MovieMatch! 💖 We're thrilled you're interested in helping us build a better movie recommendation system. Your contributions are valuable and help make this open-source project great.

This document provides a set of guidelines for contributing to MovieMatch. These are mostly guidelines, not strict rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

---

## 📜 Code of Conduct

This project and everyone participating in it is governed by the [MovieMatch Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to ensure our community remains a safe and welcoming space.

---

## ❓ How Can I Contribute?

There are many ways to contribute, from writing code and improving documentation to reporting bugs and suggesting new features.

* **🐛 Reporting Bugs:** If you find a bug, please open an issue and provide as much detail as possible, including steps to reproduce it.
* **✨ Suggesting Enhancements:** Have an idea for a new feature or an improvement? Open an issue to share your thoughts.
* **📝 Writing Documentation:** Great documentation is key. If you see an area for improvement, feel free to make it.
* **💻 Submitting Pull Requests:** If you're ready to contribute code, that's fantastic! Please follow the workflow below.

---

## 🔰 Your First Contribution

Unsure where to begin? A great place to start is by looking for issues tagged with `good first issue` or `help wanted`. These are issues that have been identified as good entry points for new contributors. We're here to help you get started!

---

## ⚙️ Development Setup

To get the project running locally, you'll need to set up both the model generation environment and the Streamlit application.

### ✅ Prerequisites

* Python 3.8+
* Git

### 📋 Step-by-Step Instructions

1.  **Fork the Repository** 🍴
    Click the **Fork** button at the top right of the repository page. This creates a copy of the project in your own GitHub account.

2.  **Clone Your Fork** 💻
    Clone the repository to your local machine:
    ```bash
    git clone [https://github.com/YOUR_USERNAME/MovieMatch.git](https://github.com/YOUR_USERNAME/MovieMatch.git)
    cd MovieMatch
    ```

3.  **Create a Virtual Environment** 🌿
    It's highly recommended to work in a virtual environment:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

4.  **Install Dependencies** 📦
    Install all the required Python packages:
    ```bash
    pip install -r requirements.txt
    ```
    > **Note:** If a `requirements.txt` file doesn't exist, you may need to install the packages listed in the "Built With" section of the README manually.

5.  **Generate the Model Files** 🧠
    The Streamlit app depends on pre-generated model files (`.pkl`).
    * Place the dataset files (`tmdb_5000_movies.csv`, `tmdb_5000_credits.csv`) in the root folder of the project.
    * Run the `Movie Recommendation System.ipynb` Jupyter Notebook from start to finish. This will execute the data processing and similarity modeling pipeline and create the necessary `.pkl` files in your project directory.

6.  **Set Up the Streamlit App** 🔑
    * Create a folder named `.streamlit` in the project's root directory.
    * Inside `.streamlit`, create a file named `secrets.toml`.
    * Add your TMDB API key to this file. You can get a free key from [themoviedb.org](https://www.themoviedb.org/documentation/api).
    ```toml
    # .streamlit/secrets.toml
    TMDB_API_KEY = "your_actual_api_key_here"
    ```

7.  **Run the App** ▶️
    You're all set! Run the Streamlit app locally:
    ```bash
    streamlit run app.py
    ```
    The application should now be running in your web browser.

---

## 🚀 Pull Request Workflow

1.  **Create a New Branch**
    Create a new **branch** with a descriptive name for your feature or bug fix:
    ```bash
    # For a new feature
    git checkout -b feature/your-awesome-feature-name

    # For a bug fix
    git checkout -b fix/issue-description
    ```

2.  **Make Your Changes**
    Write your code, add your tests, and make sure everything works as expected. Follow the existing code style.

3.  **Commit Your Changes**
    Write a clear and concise **commit message**:
    ```bash
    git commit -m "feat: Add genre filtering to recommendations"
    ```
    > Use prefixes like `feat:`, `fix:`, `docs:`, `style:`, `refactor:`, or `test:`.

4.  **Push to Your Fork**
    Push your changes to your forked repository:
    ```bash
    git push origin feature/your-awesome-feature-name
    ```

5.  **Open a Pull Request**
    * Go to the original MovieMatch repository on GitHub.
    * You should see a prompt to create a **Pull Request** from your new branch.
    * Provide a clear title and a detailed description of your changes. Link to any relevant issues by writing `Closes #123`.
    * Submit the Pull Request and wait for a review.

Thank you for your contribution! 🎉

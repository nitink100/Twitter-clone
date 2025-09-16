# Ruby on Rails Social Media Platform 🐦

A social media platform, that emulates core Twitter functionalities by integrating with the official Twitter API v2. The application provides users with a personalized feed, real-time search, and automated content refreshing.

---

## ✨ Key Features

* **Twitter API Integration:** Seamlessly fetches and displays data from Twitter's v2 API using the RestClient gem.
* **Secure OAuth 2.0 Authentication:** Robust and secure user authorization allowing users to connect their Twitter accounts.
* **Personalized Feeds:** Logged-in users see a homepage populated with relevant tweets, stored and managed in a local database.
* **Automated Content Refresh:** A background job powered by **Sidekiq** and **Redis** automatically refreshes tweets for users, ensuring feeds are always up-to-date.
* **Real-time Search:** An intuitive search feature allowing users to effortlessly explore trending topics and hashtags.

---

## 🛠️ Tech Stack

* **Backend:** Ruby on Rails
* **Database:** SQLite3
* **Background Processing:** Sidekiq, Redis
* **API Interaction:** RestClient, OAuth 2.0
* **Development Environment:** WSL (Windows Subsystem for Linux)
* **Version Control:** Git & GitHub

---

## 🚀 Getting Started

Follow these instructions to set up and run the project locally.

### Prerequisites

Make sure you have the following installed on your system:
* Ruby (check `.ruby-version` file for exact version)
* Bundler
* Node.js & Yarn
* Redis Server

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/nitink100/Twitter-clone.git
    cd Twitter-clone
    ```

2.  **Install dependencies:**
    ```bash
    bundle install
    yarn install
    ```

3.  **Set up environment variables:**
    You'll need to get your own API keys from the [Twitter Developer Portal](https://developer.twitter.com/).

    Create a `.env` file in the root of the project and add the following keys:
    ```
    TWITTER_API_KEY="your_twitter_api_key"
    TWITTER_API_SECRET_KEY="your_twitter_api_secret_key"
    TWITTER_BEARER_TOKEN="your_twitter_bearer_token"
    ```

4.  **Set up the database:**
    ```bash
    rails db:create
    rails db:migrate
    ```

---

## 🏃 How to Run the Application

You'll need to run three separate processes in three different terminal tabs.

1.  **Start the Redis server:**
    ```bash
    redis-server
    ```

2.  **Start the Sidekiq workers:**
    ```bash
    bundle exec sidekiq
    ```

3.  **Start the Rails server:**
    ```bash
    rails s
    ```

Open your browser and navigate to `http://localhost:3000` to see the application in action!

---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

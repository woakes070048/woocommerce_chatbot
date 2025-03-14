# 🛒 WooCommerce ChatBot Assistant

An intelligent chatbot assistant for WooCommerce stores that helps customers with order status inquiries, product searches, and frequently asked questions.

## ✨ Features

- 📦 **Order Status Tracking**: Check order status using email address or order ID
- 🔍 **Product Search**: Find products in your WooCommerce catalog
- ❓ **FAQ Assistance**: Answer common customer questions using a customizable FAQ database
- 🧠 **Intelligent Routing**: Automatically routes queries to the appropriate service
- 🌐 **Web Integration**: Easy to integrate with any website via REST API

## 🛠️ Technology Stack

- **Backend**: Flask (Python)
- **AI Model**: Google Gemini AI
- **Database**: MySQL (WooCommerce database)
- **Agent Framework**: Agno
- **Frontend**: HTML/JavaScript (Sample included)

## 📋 Prerequisites

- Python 3.12.0 or higher
- WooCommerce store with MySQL database
- Google Gemini API key
- MySQL database credentials

## 🚀 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/kadavilrahul/woocommerce_chatbot.git
   ```
   ```bash
   cd woocommerce-chatbot
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   ```
   ```bash
   source venv/bin/activate  # On Windows, use: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file with your credentials (based on sample.env.txt):
   ```
   DB_NAME=your_db
   DB_USER=your_user
   DB_PASSWORD=your_password
   DB_HOST=your_server_ip_address
   WC_URL=https://your_website.com
   GEMINI_API_KEY=your_api_key
   DB_PORT=3306
   ```

5. Prepare your FAQ data in a CSV file named `faq.csv` in the project root directory. Use tab-separated format:
   ```
   question	answer
   How do I reset my password?	Click the "Forgot Password" link on the login page and follow the instructions.
   ```

## 🏃‍♀️ Running the Application

1. Start the backend service:
   ```bash
   python app.py
   ```

2. Open the client interface in your web browser:
   ```
   Client/index1.html
   ```

## 📚 API Usage

The chatbot exposes a simple REST API:

```
GET /message?input=your_question_here
```

Example response:
```json
{
  "result": "Here are the products that match your search..."
}
```

## 📁 Project Structure

- `app.py`: Flask application entry point
- `woocommerce_bot.py`: Core bot functionality and agent definitions
- `faq.csv`: Customizable FAQ database
- `requirements.txt`: Python dependencies
- `Client/`: Frontend implementation

## 🔧 Customization

### FAQ Database
Edit the `faq.csv` file to customize the frequently asked questions and answers. The format should be tab-separated with "question" and "answer" columns.

### Agent Behavior
You can modify the agent instructions in `woocommerce_bot.py` to customize how the bot interacts with users.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

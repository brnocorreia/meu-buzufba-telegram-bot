# Meu BuzuFBA - Telegram Web App

A modern Telegram Web App that allows users to post updates about urban bus routes at the Federal University of Bahia (UFBA).

## Features

- Post real-time updates about bus routes
- Report bus status (on time, delayed, very delayed, not running)
- Share current location of buses
- Add comments with additional information
- Seamless integration with Telegram

## Setup and Deployment

### Prerequisites

- A Telegram Bot (created via [@BotFather](https://t.me/BotFather))
- A web server or hosting service (GitHub Pages in this case)
- Backend API for storing updates (optional but recommended)

### Local Development

1. Clone this repository:

   ```
   git clone https://github.com/yourusername/meu-buzufba-telegram-bot.git
   cd meu-buzufba-telegram-bot
   ```

2. Open `index.html` in your browser to test the interface.

3. For API integration, update the endpoint URL in the JavaScript code:
   ```javascript
   // Replace with your actual API endpoint
   const response = await fetch("https://your-api-endpoint.com/bus-updates", {
     // ...
   });
   ```

### Deploying to GitHub Pages

1. Push your code to a GitHub repository.

2. Go to your repository settings, navigate to "Pages" and select the branch you want to deploy (usually `main` or `master`).

3. GitHub will provide you with a URL where your app is deployed (e.g., `https://yourusername.github.io/meu-buzufba-telegram-bot/`).

### Connecting to Telegram Bot

1. Talk to [@BotFather](https://t.me/BotFather) on Telegram and use the `/mybots` command.

2. Select your bot and then choose "Bot Settings" > "Menu Button" > "Configure Menu Button".

3. Set the Web App URL to your GitHub Pages URL.

4. Alternatively, you can create a command that opens the Web App:

   ```
   /setcommands
   ```

   Then add:

   ```
   atualizar - Enviar atualização sobre o ônibus
   ```

5. To configure the command to open the Web App, use:
   ```
   /setmenubutton
   ```
   And provide your GitHub Pages URL.

## Backend Integration

For a complete solution, you'll need a backend API to store and retrieve bus updates. You can create a simple API using:

- Node.js with Express
- Python with Flask or FastAPI
- Firebase Functions
- Any other backend technology

The API should have at least one endpoint to receive POST requests with the update data.

## Customization

You can customize the app by:

- Updating the bus routes in the select dropdown
- Changing the color scheme (the app automatically adapts to Telegram's theme)
- Adding more fields to the form
- Implementing real-time updates using WebSockets

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

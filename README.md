# Simple Prompt-Response Chatbot

A beautiful, responsive web-based chatbot built with Flask that responds to user prompts using a predefined dataset. The chatbot features a modern UI with smooth animations and is ready to deploy on Vercel.

## Features

- 🤖 **Smart Responses**: Pre-configured responses for common prompts and questions
- 🎨 **Modern UI**: Beautiful, responsive design with smooth animations
- 📱 **Mobile Friendly**: Works perfectly on desktop and mobile devices
- ⚡ **Fast & Lightweight**: Built with Flask for quick responses
- 🚀 **Easy Deployment**: Ready to deploy on Vercel with included configuration
- 💬 **Interactive Chat**: Real-time chat interface with typing indicators

## Project Structure

```
simple-prompt-response-chatbot/
├── api/
│   └── index.py          # Flask application (Vercel serverless function)
├── templates/
│   └── index.html        # Chatbot web interface
├── dataset.jsonl         # Response dataset (JSONL format)
├── requirements.txt      # Python dependencies
├── vercel.json          # Vercel deployment configuration
└── README.md            # This file
```

## Dataset Format

The chatbot uses a JSONL (JSON Lines) format for the response dataset. Each line contains:

```json
{"prompts": ["hi", "hello", "hey"], "response": "Hi there! I am a chatbot 🤖"}
```

- `prompts`: Array of trigger phrases (case-insensitive)
- `response`: The bot's response to any of the trigger phrases

## Local Development

### Prerequisites

- Python 3.7+
- pip

### Setup

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd simple-prompt-response-chatbot
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   python api/index.py
   ```

4. **Open your browser**
   Navigate to `http://localhost:5000`

## Deployment on Vercel

This project is configured for easy deployment on Vercel:

1. **Connect your GitHub repository to Vercel**
2. **Deploy automatically** - Vercel will detect the configuration and deploy

### Manual Deployment

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel
```

## Customization

### Adding New Responses

Edit `dataset.jsonl` to add new prompt-response pairs:

```json
{"prompts": ["your new prompt", "another variation"], "response": "Your custom response here! 🎉"}
```

### Styling

The chatbot UI is styled with CSS in `templates/index.html`. Key customization points:

- **Colors**: Modify CSS variables in the `:root` section
- **Layout**: Adjust `.chat-container` dimensions
- **Animations**: Customize keyframes and transitions

### Branding

Update the chatbot title and branding in `templates/index.html`:

```html
<div class="chat-title">Your Bot Name</div>
<div class="chat-sub">Your tagline here</div>
```

## API Endpoints

- `GET /` - Serves the chatbot interface
- `POST /chat` - Handles chat messages
  - Request: `{"message": "user input"}`
  - Response: `{"response": "bot response"}`

## Technologies Used

- **Backend**: Flask (Python)
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Deployment**: Vercel
- **Data Format**: JSONL

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

If you have any questions or need help, please open an issue on GitHub.

---

**Made with ❤️ for the community**

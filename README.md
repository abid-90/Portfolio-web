# Portfolio Website

A responsive portfolio website built with HTML, CSS, and JavaScript, featuring a fully functional contact form with email integration.

## Features

- Responsive design with mobile-first approach
- Animated background and smooth interactions
- Functional contact form with email notifications
- Project showcase
- Skills and certifications display
- Fully optimized for Vercel deployment

## Prerequisites

- Node.js 16+ installed
- A Gmail account with App Password generated
- Vercel account (free tier available at [vercel.com](https://vercel.com))

## Local Development

### Setup

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd Portfolio
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create `.env` file (copy from `.env.example`):
   ```bash
   cp .env.example .env
   ```

4. Add your Gmail credentials to `.env`:
   ```
   GMAIL_USER=your-email@gmail.com
   GMAIL_APP_PASSWORD=your-app-password-here
   ```

5. Run development server:
   ```bash
   npm run dev
   ```

### Generating Gmail App Password

1. Go to https://myaccount.google.com/security
2. Enable "2-Step Verification" (if not already enabled)
3. Go to "App passwords"
4. Select "Mail" and "Windows Computer"
5. Generate and copy the 16-character password
6. Use this as your `GMAIL_APP_PASSWORD`

## Deployment on Vercel

### Quick Deploy

1. Push your code to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Click "New Project" and import your GitHub repository
4. Add environment variables:
   - `GMAIL_USER`: Your Gmail address
   - `GMAIL_APP_PASSWORD`: Your Gmail app password
5. Click "Deploy"

### Using Vercel CLI

1. Install Vercel CLI globally:
   ```bash
   npm install -g vercel
   ```

2. Deploy your project:
   ```bash
   vercel
   ```

3. Follow the prompts to:
   - Link your project (first deploy)
   - Set environment variables in Vercel dashboard

4. Set environment variables in Vercel dashboard:
   - Go to Project Settings → Environment Variables
   - Add `GMAIL_USER` and `GMAIL_APP_PASSWORD`

## Project Structure

```
portfolio/
├── index.html          # Main HTML file
├── server.js           # Express server (for local dev)
├── package.json        # Dependencies
├── vercel.json         # Vercel configuration
├── api/
│   └── send-email.js   # Vercel serverless function for email
├── .env.example        # Environment variables template
├── .gitignore          # Git ignore rules
└── README.md           # This file
```

## Contact Form

The contact form uses Vercel serverless functions to send emails through Gmail. When a user submits the form:

1. Form data is validated on the client side
2. Data is sent to `/api/send-email` endpoint
3. Server validates data and sends email via Gmail
4. User receives confirmation message

## Troubleshooting

### Email not sending?

1. Verify Gmail credentials in `.env` or Vercel environment variables
2. Check that "Less secure app access" is disabled (use App Password instead)
3. Ensure 2-Step Verification is enabled on Gmail account
4. Check Vercel deployment logs for errors

### CORS errors?

The API endpoint handles CORS automatically. No additional configuration needed.

### Form not submitting?

1. Open browser console (F12) to see error messages
2. Check network tab to verify API call is being made
3. Ensure email field has valid format

## Environment Variables

Required environment variables for email functionality:

- `GMAIL_USER`: Your Gmail address (e.g., your.email@gmail.com)
- `GMAIL_APP_PASSWORD`: 16-character Gmail app password

**Never commit `.env` file to Git. Use `.env.example` as template.**

## Technologies Used

- HTML5
- CSS3 (with animations and gradients)
- JavaScript (vanilla, no frameworks)
- Node.js with Express (local development)
- Nodemailer (email service)
- Vercel (hosting and serverless functions)

## License

All rights reserved © 2025 Abid Syed

## Support

For issues or questions, contact: sd.abid3695@gmail.com
The contact form sends emails directly to your Gmail account using Nodemailer. Make sure to:
1. Enable 2-factor authentication on your Gmail account
2. Generate an app password for the application
3. Set the app password as the `EMAIL_PASS` environment variable

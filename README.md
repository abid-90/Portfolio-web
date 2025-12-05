# Portfolio Website

A responsive portfolio website built with HTML, CSS, and JavaScript, featuring a functional contact form.

## Features

- Responsive design
- Animated background
- Contact form with email functionality
- Project showcase
- Skills and certifications display

## Deployment on Vercel

### Prerequisites

1. Create a Vercel account at [vercel.com](https://vercel.com)
2. Install Vercel CLI: `npm install -g vercel`

### Environment Variables

Set up the following environment variables in your Vercel dashboard:

- `EMAIL_USER`: Your Gmail address (sd.abid3695@gmail.com)
- `EMAIL_PASS`: Your Gmail app password (generate from Google Account settings)

### Deployment Steps

1. Clone or download this repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Deploy to Vercel:
   ```bash
   vercel
   ```
4. Follow the prompts to link your project and deploy

### Local Development

To run locally:
```bash
npm run dev
```

This will start the development server with hot reloading.

## Contact Form

The contact form sends emails directly to your Gmail account using Nodemailer. Make sure to:
1. Enable 2-factor authentication on your Gmail account
2. Generate an app password for the application
3. Set the app password as the `EMAIL_PASS` environment variable

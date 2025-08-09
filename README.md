# MarkdownConverter - Convert Markdown to PDF & Word

A web-based tool that converts Markdown files to PDF and Word documents. Perfect for users who receive Markdown content from AI models like Claude and need to convert it to more accessible formats.

## Features

- **Real-time Markdown Preview**: See your content as you upload
- **PDF Conversion**: Convert to styled PDF documents
- **Word Document Export**: Export to Microsoft Word format
- **Mobile-Friendly**: Responsive design that works on all devices
- **Secure**: Files are automatically cleaned up after processing
- **No Registration Required**: Start converting immediately

## Supported Markdown Features

- Headers (`# ## ###`)
- **Bold** and *Italic* text
- [Links](url) and ![Images](url)
- Lists (ordered and unordered)
- Tables
- Code blocks and inline code
- Blockquotes
- And more!

## Deployment to Vercel

### Prerequisites

1. **GitHub Account**: You'll need a GitHub account
2. **Vercel Account**: Sign up at [vercel.com](https://vercel.com)
3. **Domain**: Your domain `convertmdtopdf.online` from GoDaddy

### Step 1: Create GitHub Repository

1. Create a new repository on GitHub
2. Push this code to the repository:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/markdown-converter.git
git push -u origin main
```

### Step 2: Deploy to Vercel

1. Go to [vercel.com](https://vercel.com) and sign in
2. Click "New Project"
3. Import your GitHub repository
4. Configure the following settings:
   - **Framework Preset**: Other
   - **Root Directory**: `./`
   - **Build Command**: Leave empty
   - **Output Directory**: Leave empty
   - **Install Command**: `pip install -r requirements.txt`

### Step 3: Environment Variables

Add these environment variables in your Vercel project settings:

```
SENDGRID_API_KEY=your_sendgrid_api_key
SESSION_SECRET=your_session_secret_key
DATABASE_URL=your_postgresql_database_url
```

### Step 4: Custom Domain Setup

1. In your Vercel project, go to "Settings" → "Domains"
2. Add your domain: `convertmdtopdf.online`
3. Vercel will provide DNS records to add to GoDaddy
4. In GoDaddy DNS settings, add the CNAME record pointing to Vercel

## Local Development

### Prerequisites

- Python 3.11+
- pip

### Installation

1. Clone the repository:
```bash
git clone https://github.com/YOUR_USERNAME/markdown-converter.git
cd markdown-converter
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Set environment variables:
```bash
export SENDGRID_API_KEY=your_key
export SESSION_SECRET=your_secret
export DATABASE_URL=sqlite:///app.db
```

4. Run the application:
```bash
python app.py
```

5. Open http://localhost:5000 in your browser

## Project Structure

```
MarkdownConverter/
├── app.py                 # Main Flask application
├── app_vercel.py         # Vercel-compatible version
├── models.py             # Database models
├── email_service.py      # Email functionality
├── requirements.txt      # Python dependencies
├── vercel.json          # Vercel configuration
├── static/              # Static files (CSS, JS)
├── templates/           # HTML templates
└── README.md           # This file
```

## SEO Optimization

The website is optimized for search engines targeting users who need to convert Markdown to PDF:

- **Primary Keywords**: "markdown to pdf", "convert markdown", "markdown converter"
- **Secondary Keywords**: "claude markdown", "ai markdown", "markdown to word"
- **Meta Tags**: Optimized title, description, and keywords
- **Structured Data**: Schema markup for better search visibility
- **Mobile-First**: Responsive design for mobile users

## Monetization

The website includes advertising spaces for monetization:

- **Banner Ads**: Top banner (728x90)
- **Sidebar Ads**: Medium rectangle (300x250)
- **Contact Form**: For advertiser inquiries

## Security Features

- File type validation
- File size limits (16MB max)
- Rate limiting on contact forms
- Automatic file cleanup
- XSS protection
- CSRF protection

## Performance Optimizations

- Minified CSS and JavaScript
- Optimized images
- CDN for external resources
- Efficient database queries
- Caching strategies

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For support or questions, contact: simon@alpharock.net

---

**Note**: This is a serverless deployment optimized for Vercel. For production use with high traffic, consider using a traditional server deployment with proper file storage and PDF generation services. 
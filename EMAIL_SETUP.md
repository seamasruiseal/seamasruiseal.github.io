# EmailJS Setup Guide

## Step 1: Create EmailJS Account
1. Go to https://www.emailjs.com/
2. Sign up for a free account
3. Verify your email

## Step 2: Add Email Service
1. In EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Choose "Gmail" (or your preferred email provider)
4. Connect your email account (seamas.ruiseal@tufts.edu)
5. Note down the Service ID (e.g., "service_abc123")

## Step 3: Create Email Template
1. Go to "Email Templates"
2. Click "Create New Template"
3. Use this template:

**Subject:** New Contact Form Message from {{name}}

**Body:**
```
Name: {{name}}
Email: {{email}}
Message: {{message}}
```

4. Note down the Template ID (e.g., "template_xyz789")

## Step 4: Get Public Key
1. Go to "Account" → "API Keys"
2. Copy your Public Key

## Step 5: Update contact.html
Replace these placeholders in contact.html:
- `YOUR_SERVICE_ID` → Your actual Service ID
- `YOUR_TEMPLATE_ID` → Your actual Template ID  
- `YOUR_PUBLIC_KEY` → Your actual Public Key

## Alternative: Formspree (Even Simpler)
If EmailJS seems complex, you can use Formspree:
1. Go to https://formspree.io/
2. Create account and get your form endpoint
3. Replace the form action with: `action="https://formspree.io/f/YOUR_FORM_ID"`
4. Remove the EmailJS code and use regular form submission

## Alternative: Netlify Forms
If you host on Netlify:
1. Add `netlify` attribute to your form
2. Messages will be available in your Netlify dashboard
3. You can also set up email notifications 
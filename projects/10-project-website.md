# Project 1: Build and Deploy a Responsive Website to AWS

## 🎯 Project Overview

Build a modern, responsive website and deploy it to AWS using S3 and CloudFront. This project demonstrates Q CLI's ability to assist with both web development and AWS deployment tasks.

### What You'll Build & Deploy
- 📱 **Responsive Website** - Modern HTML, CSS, JavaScript
- 🪣 **S3 Static Hosting** - Secure bucket with proper configuration
- 🌐 **CloudFront Distribution** - Global CDN with Origin Access Control (OAC)
- 🔒 **Security Best Practices** - Private bucket with OAC access

## 🚀 Part 1: Create the Website

### Step 1: Project Setup
```bash
# Create project directory
mkdir q-cli-website
cd q-cli-website

# Start Q CLI session
q chat
```

### Step 2: Generate Website Files
Use this prompt with Q CLI:

```
Create a responsive website with these files:

1. index.html - Modern HTML5 structure with:
   - Navigation menu
   - Hero section with call-to-action
   - Image gallery section (6 placeholder images)
   - Contact section with form
   - Footer

2. styles.css - Responsive CSS with:
   - Mobile-first design
   - CSS Grid for gallery
   - Smooth animations
   - Professional color scheme

3. script.js - Interactive features:
   - Image lightbox functionality
   - Smooth scrolling navigation
   - Form validation
   - Mobile menu toggle

Please create all files with complete, production-ready code.
```

### Step 3: Add Images
Ask Q CLI to help with placeholder images:

```
Create a simple script to generate 6 placeholder images for the gallery, or suggest free image sources I can use for this project.
```

## 🪣 Part 2: Deploy to AWS S3

### Step 4: Create S3 Bucket
Use Q CLI to create a secure S3 bucket:

```
Help me create an S3 bucket for static website hosting with these requirements:
- Bucket name: my-website-[random-string]
- Region: us-east-1
- Block all public access (private bucket)
- Enable versioning
- Add appropriate tags
- Configure for static website hosting

Provide the AWS CLI commands to set this up.
```

### Step 5: Upload Website Files
Ask Q CLI for the upload process:

```
Show me how to upload my website files (index.html, styles.css, script.js, and images folder) to the S3 bucket using AWS CLI. Include proper content-type settings for each file type.
```

### Step 6: Set Bucket Policy for OAC
Request bucket policy configuration:

```
Create an S3 bucket policy that allows access only through CloudFront Origin Access Control (OAC). The bucket should deny all public access and only allow CloudFront to serve the content.
```

## 🌐 Part 3: Setup CloudFront Distribution

### Step 7: Create CloudFront Distribution
Use this comprehensive prompt:

```
Help me create a CloudFront distribution for my S3 static website with these specifications:

1. Origin Configuration:
   - Use my S3 bucket as origin
   - Set up Origin Access Control (OAC) - not legacy OAI
   - Default root object: index.html

2. Distribution Settings:
   - Enable compression
   - Redirect HTTP to HTTPS
   - Use all edge locations
   - Set appropriate caching behaviors

3. Security:
   - Use OAC to access private S3 bucket
   - Add security headers
   - Enable WAF if recommended

4. Error Pages:
   - Custom 404 error page (redirect to index.html for SPA behavior)

Provide step-by-step AWS CLI commands and configuration.
```

### Step 8: Configure Origin Access Control
Ask Q CLI for OAC setup:

```
Walk me through creating and configuring Origin Access Control (OAC) for CloudFront to securely access my private S3 bucket. Include:
1. Creating the OAC
2. Attaching it to CloudFront distribution
3. Updating S3 bucket policy
4. Testing the configuration
```

## 🔧 Part 4: Configuration and Testing

### Step 9: DNS and Domain (Optional)
If you have a custom domain:

```
Help me configure a custom domain for my CloudFront distribution:
1. Set up Route 53 hosted zone
2. Create SSL certificate with ACM
3. Configure CloudFront to use custom domain
4. Update DNS records

Provide the complete AWS CLI workflow.
```

### Step 10: Performance Optimization
Ask Q CLI for optimization:

```
Help me optimize my CloudFront distribution for better performance:
1. Configure appropriate cache behaviors for different file types
2. Set up compression for text files
3. Add security headers
4. Configure TTL settings for static assets

Show me the CloudFront behavior configuration.
```

## 🧪 Part 5: Testing and Validation

### Step 11: Test Deployment
Use Q CLI to create testing commands:

```
Create a testing checklist and commands to verify:
1. S3 bucket is properly configured and private
2. CloudFront distribution is working
3. OAC is functioning correctly
4. Website loads properly through CloudFront
5. All static assets (CSS, JS, images) are served correctly
6. HTTPS redirection works
7. Compression is enabled

Include curl commands and AWS CLI commands for testing.
```

### Step 12: Security Validation
Ask Q CLI for security checks:

```
Help me validate the security of my deployment:
1. Confirm S3 bucket blocks all public access
2. Verify only CloudFront can access S3 content
3. Check SSL/TLS configuration
4. Validate security headers
5. Test for common misconfigurations

Provide commands to audit the security setup.
```

## 🎯 Complete Deployment Checklist

Use Q CLI to verify each step:

```
Create a final deployment checklist to confirm:
□ S3 bucket created with proper security settings
□ Website files uploaded with correct content-types
□ CloudFront distribution configured with OAC
□ S3 bucket policy allows only CloudFront access
□ HTTPS redirection enabled
□ Custom error pages configured
□ Compression enabled for text files
□ Security headers configured
□ DNS configured (if using custom domain)

Provide verification commands for each item.
```

## 🔧 Troubleshooting

### Common Issues
Use these prompts when you encounter problems:

```bash
# Access denied errors
"I'm getting access denied when accessing my website through CloudFront. Help me debug the OAC configuration."

# Caching issues
"My website updates aren't showing. Help me understand CloudFront caching and invalidation."

# SSL certificate problems
"I'm having issues with SSL certificate validation for my custom domain."

# Performance issues
"My website is loading slowly. Help me optimize CloudFront and S3 configuration."
```

## 📚 Learning Outcomes

By completing this project, you'll learn:
- Modern web development with Q CLI assistance
- AWS S3 static website hosting best practices
- CloudFront CDN configuration and optimization
- Origin Access Control (OAC) security implementation
- AWS CLI automation for deployment workflows
- Security best practices for static websites

## Next Steps

After completing this project, continue to [Project 2: Interactive Game](./11-project-game.md) to build and deploy a browser-based game with similar AWS infrastructure.

---

**Estimated Time:** 3-4 hours  
**Difficulty:** Intermediate  
**Skills:** Web Development, AWS S3, CloudFront, Security, DevOps

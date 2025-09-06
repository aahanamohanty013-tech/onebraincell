Chyrp Clone - CloneFest 2025 Submission
This project is a modern reimagining of the classic Chyrp blogging engine, rebuilt from the ground up for CloneFest 2025. It preserves the lightweight and flexible philosophy of the original while leveraging a modern, API-driven architecture with React and a Backend-as-a-Service (BaaS).

Tech Stack
Frontend: React 18 (served from a single front.html file)

Backend & Database: Supabase (PostgreSQL, Authentication, Storage, Instant APIs)

Styling: Tailwind CSS

This stack was chosen for its rapid development capabilities, scalability, and alignment with modern web development practices, directly addressing the "Startability" and "Stability" judging criteria.

Features Implemented
This submission successfully implements the vast majority of the original Chyrp's features.

Core:

Built with responsive and accessible HTML5.

Universal support for plain text and Markdown.

User management with a rights model (via Supabase Auth & RLS).

Feathers (Content Types):

Text: Blog entries with descriptions and full Markdown support.

Photo: Image uploads with captions.

Quote: Quotations with source and descriptive context.

Link: Link sharing with descriptions.

Video: Video file uploads.

Audio: Audio file uploads.

Modules (Enhancements):

Comments: A complete, real-time commenting system.

Likes: Visitors can like and unlike posts.

Post Views: View counts are tracked for each post.

Tags & Categories: Posts can be assigned a category and multiple tags.

Read More: Long text posts are truncated in the feed.

Rights: Support for attribution and copyright notices on posts.

Cascade: Infinite scrolling on the main post feed.

Lightbox: On-page image viewer for all images.

MAPTCHA: Math-based spam prevention for comments.

Highlighter: Automatic syntax highlighting for code snippets.

Easy Embed: Pasting a YouTube or Vimeo link automatically embeds the video.

MathJax: Cleanly displays mathematical notation written in LaTeX.

Setup & Installation Instructions
To run this project locally, follow these steps.

Prerequisites:

A free Supabase account.

A modern web browser.

Step 1: Set up the Supabase Backend

Go to app.supabase.com and create a new project.

Once the project is created, navigate to the SQL Editor.

Open the setup.sql file from this repository, copy its entire contents, and paste it into the Supabase SQL Editor.

Click "RUN". This will create all the necessary tables, relationships, and security policies.

Step 2: Configure the Frontend

In your Supabase project, go to Project Settings (the gear icon) → API.

You will find your Project URL and your anon public key.

Open the front.html file. At the top of the <script type="text/babel"> tag, you will find these two lines:

const SUPABASE_URL = '[https://your-project-id.supabase.co](https://your-project-id.supabase.co)';
const SUPABASE_ANON_KEY = 'your-anon-public-key-goes-here';

Replace the placeholder values with the URL and anon key you copied from your Supabase project.

Step 3: Run the Application
The application is a single HTML file and requires no build step. You can simply open the index.html file in your web browser. For the best experience and to avoid potential CORS issues, it's recommended to serve it with a simple local server (e.g., using the VS Code "Live Server" extension or python -m http.server).
step 4 : Deploy to AWS 
S3: Create a public S3 bucket, enable static hosting, and apply a public policy.

Upload: Upload your front.html and any assets to the bucket.

CloudFront: Create a CloudFront distribution, setting the origin to the S3 website endpoint.

Wait: Wait 15-20 minutes for the deployment to finish.

URL: Copy the "Distribution domain name" from CloudFront—this is your live link.
https://d1a0gc32tm55cd.cloudfront.net/ live deployed website link

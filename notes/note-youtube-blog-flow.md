# YouTube to Blog Post Flow Note

Full flow I built:

Step 1: Webhook receives YouTube URL
Someone sends: { "youtube_url": "https://youtube.com/watch?v=xxx" }

Step 2: HTTP Request gets transcript from Supadata
Transcript comes back as plain text in $json.content

Step 3: OpenAI writes blog post
System prompt trained to write like a real human.
Not robotic. Not templated. Genuine and engaging.

Step 4: Google Docs Create makes empty document
Title: Blog Post — 2026-06-06

Step 5: Google Docs Update adds content
Full blog post goes into the document.

Step 6: Gmail sends notification
Owner gets email that new blog post is ready.

Total time from URL to finished blog post: under 30 seconds.

One mistake I made:
I used Test URL in production.
Workflow stopped working after closing n8n.
Fix: Always use Production URL in any external tool.

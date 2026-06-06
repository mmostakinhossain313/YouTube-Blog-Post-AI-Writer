# Supadata API Note

I use Supadata to get YouTube video transcripts automatically.

Website: supadata.ai
Free account gives enough credits for testing.

API endpoint I use:
https://api.supadata.ai/v1/youtube/transcript

How I call it in n8n:
- Node: HTTP Request
- Method: GET
- URL: https://api.supadata.ai/v1/youtube/transcript
- Header: x-api-key = my API key
- Query Parameter: url = YouTube video URL

The transcript comes back as:
$json.content = full transcript text
$json.lang = language of the video

One mistake I made:
I put API key in query parameters instead of headers.
Got 401 unauthorized error.
Fix: Always put API key in Headers as x-api-key.

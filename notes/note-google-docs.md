# Google Docs Note

Google Docs node in n8n 2026 has two separate operations.

Operation 1: Create a document
- Creates empty document with just a title
- No content field available here
- Just gives back the document ID

Operation 2: Update a document
- Use this to add content to the document
- Document ID comes from Create operation: {{ $json.id }}
- Add content in Actions > Text field
- Expression: {{ $('Message a model').item.json.output[0].content[0].text }}

I must use both nodes together.
Create first. Then Update with content.

One mistake I made:
I thought Create would have a Content field.
Document was created but completely empty.
Fix: Added Update node after Create node.
That is how content gets into the document.

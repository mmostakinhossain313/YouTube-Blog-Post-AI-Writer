# Common Errors — YouTube Blog Post Writer

Error 1: 401 Unauthorized from Supadata
Reason: API key not in headers.
Fix: Add x-api-key header with API key value.

Error 2: Google Docs document created but empty
Reason: Create node has no content field.
Fix: Add Update node after Create. Put content in Text field.

Error 3: No Respond to Webhook node found
Reason: Webhook Respond set to Using Respond to Webhook Node.
Fix: Change Webhook Respond to Immediately.

Error 4: Expression showing undefined in Google Docs
Reason: Wrong node name in expression.
Fix: Use $('Message a model').item.json.output[0].content[0].text

Error 5: Workflow not running automatically
Reason: Using Test URL instead of Production URL.
Fix: Always Publish workflow and use Production URL.

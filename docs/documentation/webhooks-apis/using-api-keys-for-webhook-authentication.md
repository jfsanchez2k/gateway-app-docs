---
title: Using API keys for webhook authentication
deprecated: false
hidden: false
metadata:
  robots: index
---
## x-api-key Header

**Description:** This method uses an API key included in the header of your requests.

## Steps to Configure

1. **Provide an API Key**
   - Provide your API key to our API management team.

2. **Using API Key in Requests**
   - Add the API key in the `x-api-key` header of your API requests:
     - **Header:**
       - `x-api-key: YOUR_API_KEY`

### Example Request

```http
GET /endpoint HTTP/1.1
Host: api.yourdomain.com
x-api-key: YOUR_API_KEY
```

<br />

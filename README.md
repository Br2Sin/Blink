# Solana Blinks Example

This project allows users to donate SOL to a specific account via a web interface. It includes two main endpoints: `GET` and `POST`, which handle donation actions.

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
  - [GET](#get)
  - [POST](#post)
- [License](#license)

## Overview

This project provides a simple way for users to donate SOL to a predefined account using the Solana blockchain. It handles both the creation of donation actions and the processing of transactions.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/rkmonarch/blinks-example.git
   cd blinks-example
   ```

2. Install the dependencies:
   ```bash
   pnpm i
   ```

3. Start the development server:
   ```bash
   pnpm run dev
   ```
## Usage
To use this project, you can make GET and POST requests to the respective endpoints.

### API Endpoints
### GET
##### Description: Returns a JSON payload containing donation action details.
##### Endpoint: /api/donate
##### Method: GET

```tsx
{
  "icon": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS7dPPWr-BRKzBy_Fig0v_snt-_onQj9Pl5xA&s",
  "title": "Donate to the Rahul",
  "description": "Support rahul by donating SOL.",
  "label": "Donate",
  "links": {
    "actions": [
      {
        "label": "Donate 0.1 SOL",
        "href": "http://yourdomain.com/api/donate?amount=0.1"
      }
    ]
  }
}
```

### POST
##### Description: Processes a donation transaction on the Solana blockchain.
##### Endpoint: /api/donate
##### Method: POST
##### Request Body:

```
{
  "account": "SenderPublicKey"
}
```

#### Response:

```
{
  "fields": {
    "transaction": "SerializedTransaction",
    "message": "Transaction created"
  }
}
```

## License
This project is licensed under the MIT License. See the LICENSE file for details.

    

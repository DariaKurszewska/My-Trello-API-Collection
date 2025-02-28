# Trello API Request Collection in Postman

## Project Description

This repository contains a collection of predefined requests to interact with the Trello API, designed for educational purposes. The collection includes various requests for common Trello actions such as:

- Creating boards
- Creating lists
- Creating and managing cards
- Adding members to boards
- And more...

This collection is an excellent starting point for learning how to interact with the Trello API, and it can also be used for testing Trello's functionality through Postman.

### ⚠️ Important

Please be aware of the following:

- **Adhere to Atlassian’s terms and conditions:** This collection must not be used in violation of Atlassian's terms of use. Please review the [Atlassian Developer Terms](https://www.atlassian.com/legal/developer-terms) before using it.
- **Do not share sensitive credentials:** Never share your Trello API keys, authentication tokens, or any other sensitive credentials with anyone. Keep them secure and private. The collection does **not** contain any actual API keys or tokens.

## How to Configure the Collection

To use this collection in Postman, you need to set up a few environment variables for it to work properly.

### Required Environment Variables:

1. `base_url`   
   Set this variable to the following base URL for the Trello API:  
   `https://api.trello.com`

2. `key` 
   Your Trello API key. You can obtain it by visiting [Trello API Key](https://trello.com/app-key).

3. `token`  
   Your Trello authentication token, needed for user authorization. You can generate it on the same page as the API key.

**Important:**  
Without setting these values, the requests will not function properly. Make sure to configure these environment variables before using the collection.

### Instructions for Running the Collection:

1. **Set up Postman:**  
   First, ensure that you have Postman installed on your computer. You can download it from [Postman](https://www.postman.com/downloads/).

2. **Import the collection:**  
   After downloading and installing Postman, import this collection into Postman by clicking on "Import" in the top-left corner, then selecting the JSON file for the collection from this repository.

3. **Configure the environment variables:**  
   In Postman, create an environment and define the three environment variables (`base_url`, `key`, and `token`). You can do this by going to the "Environments" section in Postman, creating a new environment, and setting the appropriate values for each variable.

4. **Start using the collection:**  
   Once the collection and environment are set up, you can start running requests from the collection. Just select the environment you created, and the requests will be ready to execute.

## Example Request in Postman

Below is an example of how you can create a new board using the Trello API:

### Create Board Example

**Request URL:**  
```
{{base_url}}/1/boards/
```

**HTTP Method:**  
`POST`

**Headers:**  
```
Content-Type: application/json
```

**Query Parameters:**  
- `key` (required) - Your Trello API key.
- `token` (required) - Your Trello authentication token.

**Body (raw JSON):**
```json
{
  "name": "My New Board"
}
```

**Example cURL Command:**
```bash
curl -X POST "{{base_url}}/1/boards/" \
  -H "Content-Type: application/json" \
  -d '{"name": "My New Board", "key": "{{key}}", "token": "{{token}}"}'
```

This example demonstrates how to send a request to create a new board. You can use this template and adjust parameters as needed for other endpoints in the collection.

## License and Usage

This repository is publicly available for educational and personal use. The collection is intended for interacting with the Trello API using Postman for learning and testing purposes. 

You are free to use and modify the collection as you wish, but **you must adhere to the Trello API Terms of Use** and ensure that sensitive credentials such as API keys and authentication tokens are kept secure. 

Please note that this repository does not provide any warranty, and is shared **"as-is"**. I am not responsible for any issues or damages arising from its use.

## Issues and Support

If you encounter any issues or have questions regarding the collection, please follow these steps:

1. **Check the documentation:**  
   Make sure the issue is not already addressed in the README file or the official Trello API documentation.

2. **Open an issue:**  
   If you find a bug or have a suggestion for improvement, please open an issue in the Issues section.

3. **Provide details:**  
   When reporting a bug, please include the following information to help us resolve the issue quickly:
   - Steps to reproduce the problem.
   - The error message, if applicable.
   - The specific request (endpoint) from the Postman collection that is causing the issue.

We will try to address any issues as quickly as possible, but please note that this is an open-source project, and responses may take some time.

## Planned Updates

This collection is actively being developed, and new requests or improvements will be added as I continue to learn and work with the Trello API. Keep an eye out for future updates, such as additional Trello API functionality or enhanced request examples.

## Links

- [Official Trello API Documentation](https://developer.atlassian.com/cloud/trello/rest/)
- [Atlassian Developer Terms](https://www.atlassian.com/legal/developer-terms)
- [Trello API Key](https://trello.com/app-key)
- [Postman Downloads](https://www.postman.com/downloads/)


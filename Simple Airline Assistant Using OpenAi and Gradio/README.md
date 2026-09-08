# ✈️ Airline AI Assistant with OpenAI Tool Calling

A simple Airline AI Assistant built using the OpenAI API, function/tool calling, SQLite, and Gradio.

This project allows an AI assistant to interact with external functions to retrieve and update airline ticket prices. Instead of only generating text responses, the AI can decide when a tool needs to be called and provide the required arguments automatically.

## 🚀 Features

- 🤖 AI-powered airline assistant
- 🔧 OpenAI Function/Tool Calling
- 💰 Get ticket prices for different cities
- ✏️ Set or update ticket prices
- 🗄️ SQLite database integration
- 🔄 Supports multiple and sequential tool calls
- 💬 Simple chat interface using Gradio

## 🛠️ Technologies Used

- Python
- OpenAI API
- OpenAI Python Client Library
- Gradio
- SQLite
- JSON

## 🧠 How It Works

The AI assistant is provided with information about the available tools, including:

- Tool name
- Tool description
- Required parameters

For example, the AI can use a tool called:

`set_ticket_price`

The tool requires:

- `city`
- `price`

When a user asks the assistant to update a ticket price, the model can decide to call the appropriate function and automatically generate the required arguments.

The Python application then:

1. Receives the tool call from the AI
2. Extracts the arguments from the JSON response
3. Identifies which tool needs to be executed
4. Runs the corresponding Python function
5. Stores or updates the information in the SQLite database
6. Sends the tool result back to the AI
7. Returns a final response to the user

## 🔧 Example Tool

### Set Ticket Price

The AI can call the following tool to update a ticket price:

```text
set_ticket_price(city, price)

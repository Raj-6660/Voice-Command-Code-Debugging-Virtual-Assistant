# Voice Command Code Debugging Virtual Assistant

An AI-powered Telegram bot workflow built using n8n that enables users to send voice or text messages to an assistant for help with code debugging. The assistant processes the input using OpenAI's API and responds with either a text reply or a generated audio response.
- [Video Explanation of the Project](https://drive.google.com/file/d/1H_7-KmDFUaSv-cvGRXnkefz4HbjqVu7n/view?usp=sharing)

## 🚀 Features

Telegram Bot Integration: Triggered by text or voice messages sent via Telegram.

Voice & Text Input Handling: Dynamically routes input based on message type.

AI Agent: Processes user queries using OpenAI Chat Model with contextual memory.

Voice-to-Voice: Transcribes voice messages using OpenAI API and replies back in the form of audio.

Text-to-Text: Converts audio reponses into text chats and send them back via telegram.

## 🧠 Workflow Breakdown

1. Initial Setup

Telegram Trigger: Starts the workflow when a Telegram message is received.

Send Text Message: Sends an acknowledgment/confirmation message to the user.

Switch Node: Routes input to either text processing or audio handling flow.

2. Handling Audio File

Get File: Retrieves the audio file URL from the Telegram chat.

Transcribe Recording: Uses OpenAI API to transcribe the audio message into text.

3. AI Agent

OpenAI Chat Model: Processes the text (from voice or message) and generates a reply.

Simple Memory: Retains context to improve AI understanding and response.

4. Switch Node (Response Handling)

Text Reply: Sends the AI response as a text message via Telegram.

Audio Reply: Converts the response to speech and sends it as an audio file.

5. Generate Audio & Send It

Generate Audio: Converts AI text response into audio.

Send Audio File: Delivers the audio response back to the user on Telegram.

## 🛠 Tech Stack

n8n: Visual workflow automation tool

OpenAI API: For chat and transcription

Telegram Bot API: For messaging interface

## How to Use

Clone the repository
Import the workflow into your n8n instance
Set up your Telegram bot and get the token
Add your environment variables in .env
Deploy and test via Telegram


## 👨‍💻 Author

- Rajarshya Singh Mahal
- Built during the IIT Jammu Summer Internship Program
- Email: rajarshyasingh@gmail.com


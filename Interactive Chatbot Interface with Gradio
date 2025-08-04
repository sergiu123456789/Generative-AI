# 💬 Interactive Chatbot Interface with Gradio

An interactive, human-like chatbot application built using **Gradio**. This app includes real-time **streaming responses**, **text input**, and **user-configurable controls** like sliders — all in a clean, browser-based UI.

## 🔧 Tech Stack
- Python
- Gradio
- OpenAI / Hugging Face Transformers (optional backend)
- Async for real-time streaming

## 📌 Features
- 🔄 **Streaming replies**: Chatbot responses appear word-by-word, like a human typing
- 🧠 **Real-time interaction**: Uses async generators for smooth conversational flow
- 📝 **Text input box**: Accepts user messages
- 🎚️ **Slider controls**: Adjust chatbot behavior (e.g., temperature or max tokens)
- 🌐 **Web-based UI**: Runs in any browser via Gradio

## 🧪 How It Works

```python
import gradio as gr

full_response = ""  # Keep track of the full response if needed later

        # Loop through each chunk of the response as it arrives
        for chunk in stream:
            # Check if this chunk contains actual text content
            if chunk.choices[0].delta and chunk.choices[0].delta.content:
                # Extract the text from this chunk
                text_chunk = chunk.choices[0].delta.content
                # Add this chunk to our growing response
                full_response += text_chunk
                # 'yield' is special - it sends the current state of the response to Gradio
                # This makes the text appear to be typing in real-time
                yield full_response

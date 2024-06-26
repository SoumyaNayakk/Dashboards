### Local LLM Deployment and Interaction
## Steps to Install and Run Ollama on Windows

# 1)Download Ollama:
Visit the Ollama GitHub repository https://github.com/ollama/ollama to download the installer for Windows.

# 2)Install Ollama:
Download ollama for windows
 
# 3)Start Ollama Server:
Open Command Prompt and start the Ollama server using:
ollama run llama3
This will downlaod all the packages to run llama3 on windows

# 4)Check the Ollama Server:
ollama serve
Open a browser and visit this http://localhost:11434 and check.
Ensure the server is running correctly. It will typically listen on localhost with a specific port (e.g., 11434).
# 5) Using Curl to Interact with Ollama

To interact with the Ollama server using curl on Windows, open Command Prompt and use the following commands:https://curl.se/windows/

# 6)To generate a response use this command:
curl -X POST http://localhost:11434/api/generate -H "Content-Type: application/json" -d "{\"model\": \"llama3\", \"prompt\":\"What is a rainbow?\"}"
Let us analyze this response {"model":"llama3","created_at":"2024-06-19T20:19:39.7466054Z","response":" centuries","done":false} 
model: "llama3" - This specifies the name of the model that generated the response. In this case, it is "llama3".

created_at: "2024-06-19T20:19:39.7466054Z" - This timestamp indicates when the response was created. The format follows the ISO 8601 standard, providing a precise date and time in Coordinated Universal Time (UTC).

response: "centuries" - This is the content generated by the LLM in response to the input prompt. In this case, the model's response is the single word "centuries".

done: false - This boolean value indicates whether the response is complete or if there are more parts of the response still being processed. Since it is false, it suggests that the response might be partial, and more data could be coming.

# Explanation
- The model "llama3" processed a request and generated a response at the specified timestamp.
- The response contains the word "centuries", which is part of what the model generated.
- The done field being false implies that the model might not have finished generating the complete response yet.
# 7)Repeat steps 3 to 5 and download the model moondream
ollama run moondream
curl -X POST http://localhost:11434/api/generate -H "Content-Type: application/json" -d "{\"model\": \"moondream\", \"prompt\":\"What is a rainbow?\", \"stream\": false}"
stream : false means the response is obtained all together not a stream at a time

We can conclude that for a system with limited disc space and a decent processor, moondream is efficient in terms of speed compared to llama3
# 8)These are the commands to chat with the models
curl -X POST http://localhost:11434/api/chat -H "Content-Type: application/json" -d "{\"model\": \"moondream\", \"messages\": [{\"role\": \"user\", \"content\": \"why is the sky blue?\"}], \"stream\": false}"   




curl -X POST http://localhost:11434/api/chat -H "Content-Type: application/json" -d "{\"model\": \"llama3\", \"messages\": [{\"role\": \"user\", \"content\": \"why is the sky blue?\"}]}"

# Link to the video explanation
https://drive.google.com/file/d/1lKURE8OsVru6vOoCembDeNI3FXtyIwLN/view?usp=sharing


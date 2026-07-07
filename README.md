# 📧 AI Email Reply Writer

An AI-powered Email Reply Generator built using **Spring Boot** and **Google Gemini API**. This application generates professional email replies based on the original email content and the desired tone.

## 🚀 Features

- Generate AI-powered email replies
- Multiple writing tones
  - Professional
  - Friendly
  - Formal
  - Casual
  - Polite
- REST API built with Spring Boot
- Integration with Google Gemini API
- JSON-based request and response
- Clean and modular code structure

---

## 🛠️ Tech Stack

- Java 21
- Spring Boot
- Spring Web
- Spring WebFlux (WebClient)
- Maven
- Lombok
- Jackson
- Google Gemini API

---

## 📂 Project Structure

```
src
│
├── main
│   ├── java
│   │   └── com.email.email_reply_writer
│   │       ├── app
│   │       │   ├── EmailGeneratorService.java
│   │       │   ├── EmailReplyController.java
│   │       │   ├── EmailRequest.java
│   │       │   └── WebClientConfig.java
│   │       │
│   │       └── EmailReplyWriterApplication.java
│   │
│   └── resources
│       └── application.properties
│
└── pom.xml
```

---

## ⚙️ Prerequisites

Before running the project, make sure you have installed:

- Java 21
- Maven
- IntelliJ IDEA / VS Code
- Google Gemini API Key

---

## 🔑 Get Gemini API Key

1. Visit

https://aistudio.google.com/

2. Create an API Key.

3. Copy the API key.

---

## ⚙️ Configuration

### application.properties

```properties
spring.application.name=email-reply-writer

gemini.api.url=${GEMINI_URL}
gemini.api.key=${GEMINI_KEY}
```

---

### Environment Variables

Set the following environment variables:

```
GEMINI_URL=https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash:generateContent?key=
```

```
GEMINI_KEY=YOUR_API_KEY
```

---

## ▶️ Running the Project

Clone the repository

```bash
git clone https://github.com/yourusername/email-reply-writer.git
```

Move into the project

```bash
cd email-reply-writer
```

Run the application

```bash
mvn spring-boot:run
```

or simply run

```
EmailReplyWriterApplication.java
```

from your IDE.

The application starts on

```
http://localhost:8080
```

---

## 📮 API Endpoint

### Generate Email Reply

**POST**

```
http://localhost:8080/api/email/generate
```

### Request Body

```json
{
    "emailContent": "Hi, what's the status of the report?",
    "tone": "professional"
}
```

---

### Sample Response

```text
Dear Sir/Madam,

Thank you for your email.

The report is currently in progress and is on schedule. I will share it with you as soon as it is completed.

Please let me know if you need any additional information.

Best regards,
[Your Name]
```

---

## 🧠 How It Works

1. Client sends email content and desired tone.
2. Spring Boot receives the request.
3. A prompt is generated dynamically.
4. The application calls the Google Gemini API using WebClient.
5. Gemini generates a suitable email reply.
6. The response is parsed using Jackson.
7. The generated email is returned to the client.

---

## 📌 Prompt Example

```
You are an AI email assistant.

Write ONLY one professional email reply.

Rules:
- Do not generate multiple options.
- Do not include explanations.
- Do not generate a subject.
- Return only the email body.
```

---

## 🧪 Testing

You can test the API using:

- Postman
- Insomnia
- Thunder Client
- cURL

Example:

```bash
curl -X POST http://localhost:8080/api/email/generate \
-H "Content-Type: application/json" \
-d '{
    "emailContent":"Hi, what's the status of the report?",
    "tone":"professional"
}'
```

---

## 📸 Screenshots

You can add screenshots here.

Example:

```
screenshots/
    home.png
    postman.png
```

---

## 🔮 Future Improvements

- Gmail Integration
- Chrome Extension
- Email Templates
- Authentication
- Reply History
- Response Streaming
- Multi-language Support
- AI-powered Email Summarization
- Grammar Correction
- Sentiment Analysis

---

## 🤝 Contributing

Contributions are welcome.

1. Fork the repository
2. Create a new branch

```
git checkout -b feature-name
```

3. Commit your changes

```
git commit -m "Added new feature"
```

4. Push the branch

```
git push origin feature-name
```

5. Create a Pull Request

---

## 👨‍💻 Author

**Vishal Keshari**

- GitHub: https://github.com/yourusername
- LinkedIn: https://linkedin.com/in/yourprofile

---

## ⭐ Support

If you found this project helpful, please consider giving it a ⭐ on GitHub.

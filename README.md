1. In one run, the publisher program will send 5 messages to the message broker. Each message contains a UserCreatedEventMessage struct with two fields:
    - user_id: A String (e.g., "1", "2", "3", "4", "5")
    - user_name: A String (e.g., "129500004y-Amir", "129500004y-Budi", etc.)
    - So in total, it's sending 5 separate messages, each containing:
        - {user_id: "1", user_name: "129500004y-Amir"}
        - {user_id: "2", user_name: "129500004y-Budi"}
        - {user_id: "3", user_name: "129500004y-Cica"}
        - {user_id: "4", user_name: "129500004y-Dira"}
        - {user_id: "5", user_name: "129500004y-Emir"}

2. Let's break down the connection string amqp://guest:guest@localhost:5672:
- guest:guest:
    - The first guest is the username
    - The second guest is the password
    - These are the default credentials for RabbitMQ (a popular AMQP broker)
    - In a production environment, we would typically use more secure credentials
- localhost:5672:
    - localhost means the AMQP broker (like RabbitMQ) is running on the same machine as your application
    - 5672 is the default port number for AMQP
    - If we were connecting to a remote message broker, we would replace localhost with the actual server address

Running RabbitMQ:
<img width="1680" alt="image" src="https://github.com/user-attachments/assets/695e722d-84a3-4143-9abd-3ae7ef8e8371" />

Sending and Processing event locally:
<img width="886" alt="image" src="https://github.com/user-attachments/assets/7d34e4f3-5fd8-4da5-8971-95496db21db3" />

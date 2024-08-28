+++
title = 'GoChat!' 
date = 2024-04-26T01:29:35+05:30
draft = false   
tags = ["GO", "Command Line Interface"]
+++
--- 

<!-- 

next time se make a resume like this 

https://www.jriyyya.dev/Riya_Jain_IIIT_25.pdf 
-->


# A CLI Messaging App made with GoLang

This is a simple command-line interface (CLI) messaging application written in Go. It allows users to send messages between each other, broadcast messages to all users, and view message logs.


You can run this on replit as well, [here](https://replit.com/@pritpalsingh020/ViciousConsiderateTransversal).



## Key Components

### User Struct
The `User` struct represents a user with a unique ID and their message log.

```go
type User struct {
    ID  int
    Log []string
}
```

### Message Struct
The `Message` struct represents a message with sender ID, receiver ID, and content.

```go
type Message struct {
    SenderID   int
    ReceiverID int
    Content    string
}
```

### Sending a Message, Broadcasting a message to all the remaining users, and Checking user logs!
The `sendMessage` function allows users to send messages between two users. It validates user inputs for sender ID, receiver ID, and message content. If the message content is empty, it fetches a random fact from an API.

The `broadcastMessage` function allows users to broadcast a message to all users except the sender. It validates the sender ID and message content.

The `viewMessageLog` function allows users to view the message log of a specific user. It validates the user ID and prints the message log.

### Handling the invalid user input!

```go
func sendMessage(reader *bufio.Reader) {
    ...
	
	//error handling for invalid input for a user!

	if _, ok := users[receiverID]; !ok {
		fmt.Println("Receiver ID does not exist.")
		return
	}
    ...
}
```

### Fetching Random Facts
The `getRandomFact` function fetches a random fact from an API (`https://catfact.ninja/fact`). It handles errors during the API call and decoding of the response. Implementing this was the favourite part of the assignment.

```go
func getRandomFact() string {
    url := "https://catfact.ninja/fact"
	resp, err := http.Get(url)
	if err != nil {
		return "Failed to fetch random fact"
	}
	defer resp.Body.Close()

	var factResp map[string]string
	if err := json.NewDecoder(resp.Body).Decode(&factResp); err != nil {
		return "Failed to decode random fact response"
	}

	fact, ok := factResp["fact"]
	if !ok {
		return "Failed to get random fact"
	}

	return fact
}
```

## Error Handling
The application performs error handling and input validation in various parts:
- Validating user inputs for sender ID, receiver ID, and user ID.
- Handling errors during the conversion of user inputs to integers.
- Handling errors during HTTP requests to fetch random facts from the API.
- Handling errors during decoding of the JSON response from the API.
  

## Demo

### testing regular options
> testing out the option-1 (send message between two users!)

![image](https://github.com/pritpalcodes/MyMandap---Assignment/assets/90276050/9b8307fd-f07c-487b-96db-2625ddb3d46a)

> option 3, whereby our user 2 is checking its logs, and see the message sent by user 1 earlier!

![image](https://github.com/pritpalcodes/MyMandap---Assignment/assets/90276050/0d1d7ddc-3825-4b30-8afd-97bd43e91814)

> finally, option 2, broadcasting a message! (here uesr 3 broadcasts a message to all the remaining users)

![image](https://github.com/pritpalcodes/MyMandap---Assignment/assets/90276050/1757eb36-d965-4696-9414-168f7070e7dd)

> checking the broadcast so received!

![image](https://github.com/pritpalcodes/MyMandap---Assignment/assets/90276050/05703521-f325-49ef-8816-e9328be69216)

> If empty message -> generate a random fact!

![image](https://github.com/pritpalcodes/MyMandap---Assignment/assets/90276050/246ca102-9744-4601-b396-30fa6b201161)



### testing for error handling
> user does NOT exist -> return error message(keep the loop running)

![image](https://github.com/pritpalcodes/MyMandap---Assignment/assets/90276050/7317d503-dbe4-49f8-ae60-814f561dac47)

> what if the input is INVALID (say user ID is a string?)

![image](https://github.com/pritpalcodes/MyMandap---Assignment/assets/90276050/
586c98bf-28ed-4e92-88f7-76a4b8504ba1)

> #### At last we exit the program and see all the user logs, all at once! :)

![image](https://github.com/pritpalcodes/MyMandap---Assignment/assets/90276050/2f5da723-c31d-45d9-9794-9cb71dd4e3ff)


If you liked this assignment, you can also check out my other assignments on [my GitHub](https://github.com/pritpal-singh) or on my [website](https://pritpalsingh.in).

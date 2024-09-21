# Overview of Application
The conversion client and server application provides two conversion games:
1. Converting from string variables to integers
2. Converting from string variables to bytes
The user, or client, will receive instruction of two choices for this conversion application. Then, they input One or Two to start the game. If their input other words or do not follow this syntax (first letter capitalization), they will automatically quit the game.

When user enter the game, both games will let user enter a string. There is no limitation of what they can put in. Then, the server will compute and send the result back to the client. After sending the result back, the server stops. The client receives, prints out the result, and stops the client.

# Client->Server Message Format
HOST: This is the loopback address.
PORT: The port used by the server.
ADDR: This is the address combining HOST and PORT.
client: The socket store the address and maintains connection between client and server.

deal_w_server(): The primary method responsible for starting the client side, guiding clients' action, and integrating other methods to keep every step in track.

s_to_n(client_choice): Used after selecting track 'One'. Receiving calls from the server and gain responses from the server. Also outputs the result.

s_to_b(client_choice): Used after selecting track 'Two'. Receiving calls from the server and gain responses from the server. Also outputs the result.

# Server->Client Message Format
HOST: This is the loopback address
PORT: The port used by the server
ADDR: The combination of HOST and PORT
server: The socket store the address and maintains connection between client and server.

choice(conn, addr): The choice function enables the connection between client and server, detects client's choice in action and starts corresponding methods.

str_to_num(conn): The method to perform the conversion between string input to an integer by receiving inputs (bytes) from the client, decode bytes into string, convert letters from string into a list of characters, convert characters into integers and sum them up.

str_to_bytes(conn): The method to perform the conversion between string input to bytes by receiving inputs from the client and outputs it.

start(): A integrating method to start the server.


# Example Output
*Server 1*
server <starting>
<New Connection> ('127.0.0.1', 56307) connecting
Starting number-letter conversion game :)))
Client choose to convert string to numbers
Starting to convert string to numbers
Convert letters from <byte> to <string>
Convert letters from <string> into <a list of characters>
Convert <a list of characters> into <number>
[SEND THE NUMBER BACK TO CLIENT...]
server is <done>

*Client 1*
Connection start.... Try to connect with server...
Successfully connect to the server
Starting number-letter conversion game :)))
There are two games.
1. Convert your input into number.
2. Convert your input to bytes.
Please enter One or Two:One
choice sent, waiting for reply
Reply received
Please enter a word you want to play with:west
Letter sent to the server, waiting for the final response...
Response Received, the result is 451
test client is done, exiting...

*Server 2*
server <starting>
<New Connection> ('127.0.0.1', 56324) connecting
Starting number-letter conversion game :)))
Client choose to convert from string to bytes
Starting to convert strings to bytes
Convert number from <byte> to <string>
Convert string to <byte>
[SEND THE LETTER BACK TO CLIENT...]
server is <done>

*Client 2*
Connection start.... Try to connect with server...
Successfully connect to the server
Starting number-letter conversion game :)))
There are two games.
1. Convert your input into number.
2. Convert your input to bytes.
Please enter One or Two:Two
choice sent, waiting for reply
Reply received
Please enter a word you want to play with:west
Num sent to the server, waiting for the final response...
Response Received, the result is b'west'
test client is done, exiting...

*Server 3*
server <starting>
<New Connection> ('127.0.0.1', 56342) connecting
Starting number-letter conversion game :)))
This client doesn't want to response.
Connection Off
server is <done>

*Client 3*
Connection start.... Try to connect with server...
Successfully connect to the server
Starting number-letter conversion game :)))
There are two games.
1. Convert your input into number.
2. Convert your input to bytes.
Please enter One or Two:thr
choice sent, waiting for reply
choice sent,quitting...
test client is done, exiting...

# Acknowledgments
This conversion is one directional. We can only convert strings into bytes or numbers but cannot convert them from numbers or bytes into string.
While working on this project, I intensively searched online for python syntax, error handling, and how to establish connection and network using python. The list of websites below includes all the materials I read through while working in this project. The materials are mainly webpages. I did not carefully look through all of them, but I indeed used all of them. They include:
https://docs.python.org/3/library/socket.html#other-functions
https://realpython.com/python-sockets/
https://stackoverflow.com/questions/11469146/client-server-sockets-and-file-transfer
https://stackoverflow.com/questions/4978787/how-do-i-split-a-string-into-a-list-of-characters
https://www.w3schools.com/python/python_for_loops.asp
https://www.geeksforgeeks.org/broken-pipe-error-in-python/
https://stackoverflow.com/questions/19071512/socket-error-errno-48-address-already-in-use
https://ishaileshmishra.medium.com/the-python-flask-problem-socket-error-errno-48-address-already-in-use-4d074847587e
https://github.com/spotipy-dev/spotipy/issues/537
https://stackoverflow.com/questions/11866792/how-to-prevent-errno-32-broken-pipe
https://stackoverflow.com/questions/55032621/oserror-errno-57-socket-is-not-connected
https://stackoverflow.com/questions/66203156/python-socket-programming-multiple-responses-from-server-to-the-same-client
https://stackoverflow.com/questions/36460141/python-ask-for-input-multiple-times-til-a-certain-input-disables-it
https://www.geeksforgeeks.org/how-to-convert-bytes-to-int-in-python/
https://www.geeksforgeeks.org/how-to-convert-bytes-to-int-in-python/
https://www.w3schools.com/python/python_user_input.asp

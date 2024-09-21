# Overview of Application
The conversion client and server application provides two conversion games:
1. Converting from string variables to integers
2. Converting from string variables to bytes



Note that in the letter to symbol server

# Client->Server Message Format


# Server->Client Message Format

# Example Output
*Server*
server <starting>
<New Connection> ('127.0.0.1', 54358) connecting
Starting number-letter conversion game :)))
Client choose to convert string to numbers
Starting to convert letters to numbers
Convert letters from <byte> to <string>
Convert letters from <string> into <a list of characters>
Convert <a list of characters> into <number>
[SEND THE NUMBER BACK TO CLIENT...]
server is <done>

*Client*
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

# Acknowledgments
The acknowledgements lists all the materials I used while working in this project.
The materials are mainly webpages. I did not carefully look through all of them, but I indeed used all of them. They include:
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
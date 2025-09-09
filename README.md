# Python-Assignment-Strings-Escape-Characters-and-Binary-Data
Learning Objectives
Understand and apply escape characters in Python strings (\n, \t, \\, etc.).
Use octal (\ooo) and hexadecimal (\xhh) escapes effectively.
Handle and interpret binary data (bytes, bytearray, and escape sequences).
Explore practical applications of control characters (ASCII-based communication protocols).
Work with binary-like files (images, sound, network packets).
Part A: String Escape Characters
1. Create a string that includes the following escape characters:
Newline, tab, and backslash.
Octal escape for a space (\040).
Hexadecimal escape for @ (\x40).
Print the string to show all escapes working correctly.
2. Write a program that prints a formatted table using escape sequences only (no external formatting functions).
Example:
ID\tName\tCountry\n
1\tAlice\tUSA\n
2\tBob\tIndia
3. Write a function that takes a string and prints its ASCII code values in hex and octal form using escape
notations.
Example: "Hi" → \x48\x69 and \110\151.
Part B: Binary Representation & Control Characters
1. Define the following packet string:
packet = "\x02\x10\xff"
Print the length of the packet.
Convert it into a bytes object.
Show the decimal, hex, and binary representation of each byte.
2. Use ASCII control characters:
Create a string with Start of Text (\x02), End of Text (\x03), and some sample message in between.
Write a parser function read_packet(data) that verifies whether data starts with \x02 and ends with
\x03.
Example:
data = "\x02HELLO\x03"
read_packet(data) # Output: "Valid packet: HELLO"
Part C: Applied Task on Binary Data
28/08/2025, 11:45 Thapar.edu Mail - Python Assignment: Strings, Escape Characters, and Binary Data
https://mail.google.com/mail/u/2/?ik=a2c2f5744f&view=pt&search=all&permthid=thread-a:r-1768641518372327616&simpl=msg-a:r3717369982912144047 1/3
1. Image File Header Check:
Open any .png image file in binary mode.
Read its first 8 bytes.
Verify if it matches the PNG signature:
\x89PNG\r\n\x1a\n
Print "Valid PNG file" or "Invalid file".
2. Network Packet Simulation:
Create a packet with this structure:
[START][LENGTH][MESSAGE][END]
[START] = \x02
[END] = \x03
[LENGTH] = 1 byte storing the length of the message.
[MESSAGE] = user input string.
Example: For input "OK", packet = \x02\x02OK\x03.
Write a function build_packet(msg) and parse_packet(packet) to validate and extract the
message.
Part D: Advanced
1. Binary to Sound File
Create a binary string that simulates part of a .wav file header.
Print the byte values in hex and explain what each part could mean (RIFF, WAVE). (Simplify, no need to
build an actual playable file).
2. Escape Character Visualizer
Write a Python program visualize_escapes(text) that takes a string and shows:
Original string.
Escape representation (repr(text)).
List of ASCII codes.
Example:
visualize_escapes("Hi\n")
# Output:
# Original: Hi
# Repr: 'Hi\n'
# Codes: [72, 105, 10]
Deliverables
A single Python script with all solutions.
Add comments explaining why escape characters or binary values are used in each step.
Short reflection (5–6 lines) on where escape characters and binary data handling are useful in real-world
applications (e.g., networking, file formats, protocols).

# cesar-cypher
#List of chracters to find the unicode numbers of:
letters = ["M", "a", "r", "i", "o"]

#Print the symbol correspomdimg to each Unicode point
print()
print("unicode numbers for", letters)
for i in letters:
    print(ord(i), end=" ")

#List of Unicode points for various symbols
symbols = [0x1F60A, 0x1F601, 0x1F44D, 0x1F389, 0x1F380]

#Print the symbol corresponding to each unicode point
print()
print("Unicode symbols for", symbols)
for j in symbols:
    print(chr(j), end=" ")
# Ask the user for the current hour (1-24)
current_hour = int(input("Enter the current hour (1-24): "))

# Ak the user how many hours to add
hours_to_add = int(input("How many hours do you want to add? "))

# Calculate the new hour using modulo 12 to wrap around after 12
# Adjust by subtracting 1 before the modulo and addding 1 after to ensure the 1-12 range
new_hour = ((current_hour - 1 + hours_to_add)%24) + 1

# Print the result
print("In", hours_to_add, "hours,the time will be", new_hour,":00.")

#Ask the user for th emessage to encrypt
message = input("What is the message you'd like to encrypt?")

#Ask the user for the number of positions to shift+-----
shift = int(input("Enter the amount of shifts you'd like to make")) 

#Create an empty string to hold the encrypted message
encrypted_message = ""

# Loop through each character in the message
for i in message:

    shifted = (ord(i) - ord('A') + shift) % 26

    encrypted_message += chr(shifted + ord('A'))

print("Your encrypted message is:", encrypted_message)

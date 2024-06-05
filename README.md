# encoder_decoder_JSON
# A program that creates a custom JSON encoder and decoder for complex Python objects.

# Example of a JSON string
'{"name":"John", "age":30, "car":null}'

# Encoder - An encoder is a function that takes a value type A and returns a CharSequence
# that represents the encoded value (JSON String).

# The function starts here:

i = 0
import time

while i == 0:

    reqst = input("Would you like to encode or decode files? (encode/decode):")

    if reqst.lower() == 'encode':
    
        g= open("Testing.txt", 'r')

        print("Encoding...")

        #time.sleep(2)
        
        lst = g.readlines()

        lst = [i.split('\n', 1)[0] for i in lst]

        print(lst)
        
        encd_lst_lngth = len(lst)

        print("Found " + str(encd_lst_lngth) + " entries")

        

        print("Thank you for using the program!")
        i = 1

    elif reqst.lower() == 'decode':

        g= open("Testing.txt","r")

        print("Decoding...")

        time.sleep(5)

        print(g.readline())

        print("Thank you for using this program!")
        i = 1

    else:
        print("Invalid entry, try again")

        
# Ideas: the decoding and
# encoding could require access
# to the folder with the data.

# Start of the prog.
# encode or decode?
# if encode,
# takes the text,
# creates it as JSON format (breaks the elements in text for parts)
# finishes.
# if decode,
# takes JSON file
# gets rid of the JSON file ( specifically, parts)
# finishes.

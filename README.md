# encoder_decoder_JSON (DONE (with .txt files))
# A program that creates a custom JSON encoder and decoder for complex Python objects.

# Example of a JSON string
'{"name":"John", "age":30, "car":null}'

# Encoder - An encoder is a function that takes a value type A and returns a CharSequence
# that represents the encoded value (JSON String).

# The functions starts here:

# General variables

import time
import json
i = 0

# Variables used for encoding
jaysn = 0
p = 0
prep = []
fnl_strg = 0
w = 0
jasone = 0
strg = []

# Variables used for decoding
dec = 0
d = 0
dec_prep =[]


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

        while jaysn < len(lst):
            print(lst[p])
            x = lst[p].split()
            print(x)
            prep.append(x)
            p = p + 1
            jaysn = jaysn + 1
        
        lst.clear()
        print(prep)
        print(lst)

        print(len(prep))

        while fnl_strg < len(prep):
            conve = prep[w]
            
            entry = {
                "name":conve[0],
                "age":conve[1],
                "car":conve[2]
                }

            entry_str = json.dumps(entry)
            strg.append(entry_str)
            w = w + 1
            fnl_strg = fnl_strg + 1

        print(strg)
        file = open("Fresult.txt",'w')
        for items in strg:
            file.write(items+'\n')

        file.close()
            




        
        print("Thank you for using the program!")
        i = 1

    elif reqst.lower() == 'decode':

        g= open("Fresult.txt","r")

        print("Decoding...")

        #time.sleep(5)

        lst_dec = g.readlines()

        lst_dec = [i.split('\n', 1)[0] for i in lst_dec]

        print(lst_dec)

        print(len(lst_dec))


        while dec < len(lst_dec):
            q = lst_dec[d]
            print(q)
            time.sleep(2)
            res = json.loads(q)
            print(res)
            dec = dec + 1
            d = d + 1

        #file_final = open("Fresult_decode.txt", "w")

        #file_final.close()








        print("Thank you for using this program!")
        i = 1

    else:
        print("Invalid entry, try again")


        
# Ideas: the decoding and
# encoding could require access
# to the folder with the data.

# Ideas: The entries when split,
# as lists, will be used 
# for further work on JSON
# format. (e.g. ['Brad', '18', 'Chevrolet'] ).

# Ideas : the entries will require a key-value pair 
# as of in the dictionary next.

# ENCODER: DONE.

# Next: DECODER.

# DECODER: DONE.

# Next: To make it work with .json files

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

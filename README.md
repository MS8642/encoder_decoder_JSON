# encoder_decoder_JSON
# A program that creates a custom JSON encoder and decoder for complex Python objects.

# Example of a JSON string
'{"name":"John", "age":30, "car":null}'

# Encoder - An encoder is a function that takes a value type A and returns a CharSequence
# that represents the encoded value (JSON String).

# The function starts here:

reqst = input("Would you like to encode or decode files? (encode/decode):")

if reqst.lower() == 'encode':
    
    print("This is where the encoding will happen")

    print("Thank you for using the program!")
    exit

elif reqst.lower() == 'decode':

    print('This is where the decoding will happen')

    print("Thank you for using this program!")
    exit

       


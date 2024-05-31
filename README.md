# encoder_decoder_JSON
# A program that creates a custom JSON encoder and decoder for complex Python objects.

# Example of a JSON string
'{"name":"John", "age":30, "car":null}'

# Encoder - An encoder is a function that takes a value type A and returns a CharSequence
# that represents the encoded value (JSON String).

# The function starts here:

reqst = input("Would you like to encode files? (yes/no):")

if reqst.lower() == 'yes':
    
    print("This is where the encoding will happen")

elif reqst.lower() == 'no':
    
    reqst_dec = input("Would you like to decode files? (yes/no):")

    if reqst.lower() == "yes":

        print('This is where the decoding will happen')

    elif reqst.lower() == "no":

        print("Thank you for using this program!")
        exit


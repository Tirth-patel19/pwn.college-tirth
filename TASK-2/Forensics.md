# Forensics

## Secret of Polyglot

### Solve

**Flag:** `picoCTF{f1u3n71n_pn9_&_pdf_2a6a1ea8}`

<img width="1919" height="1027" alt="image" src="https://github.com/user-attachments/assets/f13ba60f-b4eb-4c77-93b9-4c2fa4eb834b" />
<img width="1424" height="744" alt="image" src="https://github.com/user-attachments/assets/d4e670b5-3c13-4da4-84d1-ca291b433e06" />
<img width="1919" height="939" alt="image" src="https://github.com/user-attachments/assets/41af7593-6e02-4f80-849d-4c4ff35e3d6f" />

In order to solve this question i first opened the given file in the pdf format then i used the hex editior to open the same file in hex format there in the header i found that the file has png header that means it has a picture in it so to view that picture i saved the file with png format then opened the file and it gave the remainig hal of the flag thus i received my whole flag.

### New Learning
I learnt about the different types of header in a file and the function of those header in the file, I learnt very basics of how to open the file in hex view and how to extract basic informations.
### Reference
NA


## St3gO

### solve

**Flag:** `picoCTF{7h3r3_15_n0_5p00n_a9a181eb}`

for this challenge I First figured out how to flag was encrypted using which method then after finding out i used a python code that i found online to decode then flag from the file.

```bash
#import libraries
import sys
import numpy as np
from PIL import Image
np.set_printoptions(threshold=sys.maxsize)

#encoding function
password = ""
def Encode(src, message, dest,password):

    img = Image.open(src, 'r')
    width, height = img.size
    array = np.array(list(img.getdata()))

    if img.mode == 'RGB':
        n = 3
    elif img.mode == 'RGBA':
        n = 4

    total_pixels = array.size//n

    message += password
    b_message = ''.join([format(ord(i), "08b") for i in message])
    req_pixels = len(b_message)

    if req_pixels > (total_pixels * 3):
        print("ERROR: Need larger file size")

    else:
        index=0
        for p in range(total_pixels):
            for q in range(0, 3):
                if index < req_pixels:
                    array[p][q] = int(bin(array[p][q])[2:9] + b_message[index], 2)
                    index += 1

        array=array.reshape(height, width, n)
        enc_img = Image.fromarray(array.astype('uint8'), img.mode)
        enc_img.save(dest)
        print("Image Encoded Successfully")


#decoding function
def Decode(src, password):

    img = Image.open(src, 'r')
    array = np.array(list(img.getdata()))

    if img.mode == 'RGB':
        n = 3
    elif img.mode == 'RGBA':
        n = 4

    total_pixels = array.size//n

    hidden_bits = ""
    for p in range(total_pixels):
        for q in range(0, 3):
            hidden_bits += (bin(array[p][q])[2:][-1])

    hidden_bits = [hidden_bits[i:i+8] for i in range(0, len(hidden_bits), 8)]

    message = ""
    hiddenmessage = ""
    for i in range(len(hidden_bits)):
        x = len(password)
        if message[-x:] == password:
            break
        else:
            message += chr(int(hidden_bits[i], 2))
            message = f'{message}'
            hiddenmessage = message
    #verifying the password
    if password in message:
        print("Hidden Message:", hiddenmessage[:-x])
    else:
        print("You entered the wrong password: Please Try Again")

#main function
def Stego():
    print("--Welcome to $t3g0--")
    print("1: Encode")
    print("2: Decode")

    func = input()

    if func == '1':
        print("Enter Source Image Path")
        src = input()
        print("Enter Message to Hide")
        message = input()
        print("Enter Destination Image Path")
        dest = input()
        print("Enter password")
        password =  input()
        print("Encoding...")
        Encode(src, message, dest,password)

    elif func == '2':
        print("Enter Source Image Path")
        src = input()
        print("Enter Password")
        password = input()
        print("Decoding...")
        Decode(src,password)

    else:
        print("ERROR: Invalid option chosen")

Stego()
```

### New Learning 
I learnt about steganography.
### Reference
https://github.com/djrobin17/image-stego-tool/blob/master/stego.py  
https://medium.com/swlh/lsb-image-steganography-using-python-2bbbee2c69a2

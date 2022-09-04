
print("Play this CTF at : https://play.picoctf.org/practice/challenge/256?category=3&page=1&search=.py")

import sys

a = "!\"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ"+ \
            "[\\]^_`abcdefghijklmnopqrstuvwxyz{|}~ "


def arg133(arg432):
  # print for figuring out where the script is at when its running
  
  """
  After figuring out where I am by using the print below here the 'arg133' i knew I was in the input password part.
  arg432 = the password input
  if the password input did not equal (==) : 'a[71]+a[64]+a[79]+a[79]+a[88]+a[66]+a[71]+a[64]+a[77]+a[66]+a[68]' then it wouldn't give you the flag.
  So i change it to if it does not (!=) equal the required parameter (a[71]+a[64]+a[79]+a[79]+a[88]+a[66]+a[71]+a[64]+a[77]+a[66]+a[68])
  From here we get the picoCTF flag: 
  """
  print("-----------------------------------\narg133\n-----------------------------------")
  if arg432 != a[71]+a[64]+a[79]+a[79]+a[88]+a[66]+a[71]+a[64]+a[77]+a[66]+a[68]:
      return True
  else:
      print(a[51]+a[71]+a[64]+a[83]+a[94]+a[79]+a[64]+a[82]+a[82]+a[86]+a[78]+a[81]+a[67]+a[94]+a[72]+a[82]+a[94]+a[72]+a[77]+a[66]+a[78]+a[81]+a[81]+a[68]+a[66]+a[83])
      sys.exit(0)
      print("----------------------------------\ndef arg123 else hit!\n-----------------------------------")
      return False


def arg111(arg444):
  # print for figuring out where the script is at when its running
    print("\n-------------------------\narg111 is this\n")
    return "\n\n--------------------- picoCTF Flag --------------------\nYour PicoCTF flag is : " + arg122(arg444.decode(), a[81]+a[64]+a[79]+a[82]+a[66]+a[64]+a[75]+\
a[75]+a[72]+a[78]+a[77]) + "\n----------------------------------------------------------------"

def arg232():
  # print for figuring out where the script is at when its running
    print("\n-----------------------------arg232 is this!\n")
    # comment out the input so it shoudl skip right?
    #return input(a[47]+a[75]+a[68]+a[64]+a[82]+a[68]+a[94]+a[68]+a[77]+a[83]+a[68]+a[81]+a[94]+a[66]+a[78]+a[81]+a[81]+a[68]+a[66]+a[83]+a[94]+a[79]+a[64]+a[82]+a[82]+a[86]+a[78]+a[81]+a[67]+a[94]+a[69]+a[78]+a[81]+a[94]+a[69]+a[75]+a[64]+a[70]+a[25]+a[94])
    print("\n------------------------------------------")

def arg132():
  # print for figuring out where the script is at when its running
    print("\n-----------------------------------------------------------------------\narg132 was hit!\nflag.txt.enc was opened")
    print("Encrypted flag:  ",  open('flag.txt.enc', 'rb').read())
    print("\n------------------------------------------------------------------")
    return open('flag.txt.enc', 'rb').read()

def arg112():
  # print for figuring out where the script is at when its running
    print("\n---------------------------------------------------\narg112 was hit!")
    print(a[54]+a[68]+a[75]+a[66]+a[78]+a[76]+a[68]+a[94]+a[65]+a[64]+a[66]+a[74]+a[13]+a[13]+a[13]+a[94]+a[88]+a[78]+a[84]+a[81]+a[94]+a[69]+a[75]+a[64]+a[70]+a[11]+a[94]+a[84]+a[82]+a[68]+a[81]+a[25])
    print("\n------------------------------------------------------------------")

def arg122(arg432, arg423):
  # print for figuring out where the script is at when its running
    print("\n-------------------------------------------------------------")
    print("\narg122 was hit!\n-------------------------------------------------------------")
    arg433 = arg423
    i = 0
    while len(arg433) < len(arg432):
        arg433 = arg433 + arg423[i]
        i = (i + 1) % len(arg423)        

    return "".join([chr(ord(arg422) ^ ord(arg442)) for (arg422,arg442) in zip(arg432,arg433)])

  # print for figuring out where the script is at when its running
print("\n----------------------\nfunctions:\narg444 = arg132()\narg432 = arg232()\narg133(arg432)\narg112()\narg423 = arg111(arg444)\n---------------------------------------")

arg444 = arg132()
arg432 = arg232()
arg133(arg432)
arg112()
arg423 = arg111(arg444)
print("\n" + arg423 + "\n\nthis is arg423() aka arg232()")
sys.exit(0)


import random , sys
import string , os
users = input("Enter User Name: ")
password =  "".join(random.choice(string.hexdigits) for x in range(random.randint(7, 14)))
if len(users) <= 16 and len(users) >= 8:
    print("Your password is: " + password)
else:
    sys.exit("Please min8, max 16 char")
    
s = input("Do you want to continue? Y/N ")
if s == "Y" or s == "y":
    k = input("Cool! Please take your password here: ")
    
elif s != "Y" or s != "y":
    sys.exit("Okay, goodbye!")        
        
if k == password:
    print("Nice! Welcome " + users)

elif k != password:
       sys.exit("It's not your password, please try again..")
    
p = input("Can you go to the cmd panel? Y/N ")
if p == "Y" or p =="y":
    os.system("start cmd ")
    
elif s != "Y" or s != "y":
    print("Oke, bye")

    ---------------------------------------------------------------------------------------------------------------
import socket,os,sys,random
from subprocess import call
from datetime import datetime


print("-"*34 + "Welcome" + "-"*26)
print("1-Cmd Panel", "2-Chrome", "3-Instagram", 
      "4-Twitter", "5-Linkedin","6-Facebook",
      "7-Github","8-Calculator","9-Port Scan",
      "10-Powershell","11-Make Password","12-DDoS",sep = "\t" )
print(" ")
print("What you want?")
user = input("Write here ---> ")
def pc(user):
        if user == "1":
            return os.system("start cmd")      
        elif user == "2":
            return os.system("start chrome")        
        elif user == "3":
            return os.system("start www.instagram.com")        
        elif user == "4":
            return os.system("start www.twitter.com")        
        elif user == "5":
            return os.system("start www.linkedin.com")       
        elif user == "6":
            return os.system("start www.facebook.com")      
        elif user == "7":
            return os.system("start www.github.com")     
        elif user == "8":
            return call(["calc.exe"]) 
        
        elif user == "9":
            remoteServer = input("Enter a remote host to scan: ")
            remoteServerIP = socket.gethostbyname(remoteServer)
            print ("-" * 60)
            print ("Please wait, scanning remote host", remoteServerIP)
            print ("-" * 60)
            t1 = datetime.now()
            
            try:
                for port in range(1,1024):
                    sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
                    result = sock.connect_ex((remoteServerIP, port))
                    if result == 0:
                        print("Port {}: Open".format(port))
                    else:
                        print("Port {}: Close".format(port))
                    sock.close()
            except KeyboardInterrupt:
                print ("You pressed Ctrl+C")
                sys.exit()
            except socket.gaierror:
                print ('Hostname could not be resolved. Exiting')
                sys.exit()
            except socket.error:
                print ("Couldn't connect to server")
                sys.exit()
            t2 = datetime.now()
            total = t2 - t1
            print ('Scanning Completed in: ', total)
            
            
        elif user == "10":
            return os.system("start powershell")
        
        elif user =="11":
            user_int = input("START: ")
            def pass_gen(y, user_int):
                numbers = ("0","1","2","3","4","5","6","7","8","9","0","!","'","+","?","*","&","/","*","-","^","<", ">")              
                answer = ''.join(random.choice(numbers) for s in range(y))
                if len(user_int) <= 7 and all(x.isalpha() or x.isspace() for x in user_int):
                    return answer
            for i in range(10):
                print(pass_gen(random.choice([80, 100, 120, 150, 170, 200, 250, 300, 400, 500]), user_int=user_int))
                print(30*"--")
        
        else: 
            return "-"*34 + "Bye" + "-"*30
print(pc(user=user))

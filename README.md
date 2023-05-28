# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL
# DATE:16-03-2023
# AIM :
To write a python program to perform stop and wait protocol.

# ALGORITHM :
```
 1.Start the program.
 2.Get the frame size from the user
 3.To create the frame based on the user request.
 4.To send frames to server from the client side.
 5.If your frames reach the server it will send ACK signal to client otherwise,
   it will sendNACK signal to client. 
 6.Stop the program
```
 
 
# PROGRAM :
# CLIENT :
```
# Developed By : RAGHUL.S
# Register Number : 212222040128
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    i=input("Enter a data: ")
    c.send(i.encode())
    ack=c.recv(1024).decode()
    if ack:
        print(ack)
        continue
    else:
        c.close()
        break
 ```
# SERVER :
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recived".encode())
```
# OUTPUT :
# CLIENT :
![GIT](https://github.com/Raghulshanmugam2004/EX-2/assets/119561118/3380e94c-a618-493b-b664-80c3c5431ca8)


# SERVER :
![git 1 1](https://github.com/Raghulshanmugam2004/EX-2/assets/119561118/51c66a0f-e4f4-4349-ba40-cee0cf4d202c)


# RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.


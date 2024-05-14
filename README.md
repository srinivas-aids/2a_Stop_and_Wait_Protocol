# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol

## ALGORITHM
1. Start the program.

2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program

## PROGRAM:
```python
import time

def send_frame(frame):
    print("Sending frame:",frame)
    time.sleep(1)
    ack_received=False
    while not ack_received:
        ack=input("Enter ACK (1 for success, 0 failure):")
        if ack=='1':
            print("ACK received from frame:",frame)
            ack_received=True
        else:
            print("NACK received from frame:",frame)
            print("Resending frame:",frame)
            time.sleep(1)

def main():
    frame_size=int(input("Enter frame size:"))
    frames=[i for i in range(frame_size)]
    for frame in frames:
        send_frame(frame)
    print("All frames sent successfully.")
if __name__=="__main__":
    main()
```
## OUTPUT

![image](https://github.com/srinivas-aids/2a_Stop_and_Wait_Protocol/assets/93427183/edc154b7-9d18-4a66-aae6-28a45915a7fd)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.

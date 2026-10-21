Q - Check your design. Show that (a) every range fits in its field, (b) no two instructions have the 
same code, and (c) a decoder can always tell which instruction it is looking at. (3 marks) 

a) Just refer to the table.
<img width="1627" height="407" alt="Screenshot 2026-10-21 184458" src="https://github.com/user-attachments/assets/09fcf7c5-3edf-46e8-bec8-805eb7648b63" />

b) no two instructions can have same code because -
    if the operations are different then because of the opcodes each will be different.
    if operation is same then the register values or the signed constant values will change.

c) A decoder can easily tell which instruction it is looking at by checking the last 4 bits which tell it which operation it is. 
After that the decoder can find the register and other values too.

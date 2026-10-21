1. Draw the state diagram. Show every state and label each transition with the condition that 
  causes it. (5 marks)

<img width="1600" height="747" alt="WhatsApp Image 2026-10-21 at 7 15 17 PM" src="https://github.com/user-attachments/assets/8359286a-e0f7-452f-aa8f-61d2143b152b" />
(Didn't draw the reset input because it would make it look ugly, but reset makes it so no matter what the state you are in,
 you return to idle state(which is INIT here).
 
2. Create a state-transition table. Include the current state, relevant inputs, next state, and 
outputs. (5 marks)

<img width="1600" height="928" alt="WhatsApp Image 2026-10-21 at 7 15 18 PM" src="https://github.com/user-attachments/assets/f8457a40-0569-479e-91c6-3b7b5049cb9b" />

3. Define the outputs. Show when VALID is high, which reading appears on DATA_OUT, and 
when DONE is high. Also state the output values in the idle state. (4 marks)

<img width="1600" height="624" alt="WhatsApp Image 2026-10-21 at 7 15 182 PM" src="https://github.com/user-attachments/assets/ac4ffbb6-fad0-4536-9b06-befd887845f3" />

4. Handle waiting. Your FSM must hold the current reading (VALID = 1 and DATA_OUT 
unchanged) for as long as READY is low. (3 marks)

  The FSM holds the current value as long as Ready = 0 in the states S1, S2, S3.

5. Handle completion and reset. After C is accepted, assert DONE for exactly one clock cycle 
(with VALID = 0), then return to idle. RESET must return the FSM to its initial (idle) state from 
any state. (3 marks)

The flip flops and registers work at the edge of clock, the FSM returns to INIT uncoditionally but the Done signal remains 1 for 1 clock cycle.

The Reset part is reflected in the table.

7. Timing Excercise
8. 
   <img width="1600" height="515" alt="WhatsApp Image 2026-10-21 at 7 15 19 PM" src="https://github.com/user-attachments/assets/5e880c25-f82f-48ea-ae8b-0e2fffc769e2" />

8.Find the Bug 
A student writes a controller that sets VALID = 0 whenever READY = 0. 
Explain why this is incorrect. In your answer, consider what happens if the receiver waits to see 
VALID before it raises READY, and what can happen to a reading if the controller moves on anyway. 
Then describe what the controller should do instead so that no reading is lost. (4 marks)

<img width="1600" height="731" alt="WhatsApp Image 2026-10-21 at 7 15 19 2PM" src="https://github.com/user-attachments/assets/77217ea5-c40b-4fde-8a96-f8d060c44995" />

# EVM
A microcontroller-based Electronic Voting Machine built using PIC16F877A, R305 fingerprint sensor, GSM module, and LCD interface for secure and transparent voting.
Hardware: 
• PIC16F877A Microcontroller 
• Fingerprint Sensor Module (R305/FPM10A) 
• 16x2 LCD Display 
• GSM Module (SIM800/900) 
• Buzzer 
• Push Buttons (for voting) 
• Power Supply (5V regulated) 
• MAX232 (for serial communication) 
Software: 
• MPLAB X IDE 
• XC8 Compiler 
• Proteus Design Suite (for simulation) 
• Embedded C

The system should be able to: 
1. Store and verify voter fingerprint data securely. 
2. Permit voting only upon successful fingerprint authentication. 
3. Prevent multiple votes by the same individual. 
4. Trigger a buzzer and LED warning (via ADC interface) in case of unauthorized access. 
5. Record and store votes securely for transparent result calculation.

1. The system is initialized and waits for a user to interact. 
2. When a voter places their finger on the fingerprint sensor, the system captures and 
verifies the fingerprint. 
3. If the fingerprint does not match any record in the database or the user has already 
cast a vote: 
o The system activates an alarm. 
o A message is displayed indicating that the user is either unregistered or has 
already voted. 
o The system then resets and returns to the initial waiting state. 
4. If the fingerprint is verified successfully and the user has not voted yet: 
o The system proceeds to the candidate selection stage. 
5. The voter selects their preferred candidate by pressing one of the dedicated keys 
(Party Key-1, Key-2, or Key-3). 
6. The vote is securely stored in the system memory. 
7. A confirmation message is shown to indicate that the vote has been recorded 
successfully. 
8. The system returns to the idle state, ready to process the next voter. 

#Morse-code to Binary-code mapping

The code mapping contained in the file enigma.tex enables Morse code to be used to transmit 
arbitrary binary sequences... Care has to be taken with the way the end of an encoding is handled 
since it is unlikely to neatly coincide with a Morse letter. 

The code is described in the March/April 2024 issue of QEX (ARRL) under the title "Morse-Coded Binary over CW"
see:
https://www.arrl.org/files/file/QEX_Next_Issue/2024/-3%20mar-apr%2024/03-24%20qex%20new%20TOFC.pdf


If for example the binary string is an exact number of bytes then one way to manage this is 
to add to the string a run-out sequence, e.g. 11100000 to the tail end of the intended binary and then   
perform an adjustment at the receiving end to peel of any surplus bits beyond a rounded byte count.
If the received string is a whole number of bytes then a last byte should be removed upon receipt.

Examples of this mapping to be found in cmprs_morse and dcmprs_morse, see:
https://github.com/marktcode/tcodetools-for-Raspberry-Pi-or-mac/tree/main/MsgCompressor 

# 16bitALU
16bit mojo alu

## How to use
* click rst button, mojo will run all 25 test cases with display of the correctness of alu output
   * io_led[2] display most significant 16 bits of alu.out for easy debug
   * io_led[1] display least significant 16 bits of alu.out for easy debug
   * io_led[0][7:3] are on when alu.out is correct
   * io_led[0][0] is on when alu.z is correct
   * io_led[0][0] is on when alu.v is correct
   * io_led[0][0] is on when alu.n is correct
* 7-seg display the test case index in the testcases array in hex, so user can easily find which test case is wrong according to leds and the index
* when io_dip[0][0] is on, if error occurs, test will stop and display the wrong case
* if io_dip[0][]0 is off, error occurs, test won't stop and will continue till the end
* testing stops after all 25 test cases is tested
* oprations of alu
   *  operation alufn[5:0]
   *  ADD        000000
   *  SUB        000001
   *  MUL        000010
   *  DIV        000011
   *  REM        000100
   *  AND        011000
   *  OR         011110
   *  XOR        010110
   *  A          011010
   *  SHL        100000
   *  SHR        100001
   *  SRA        100011
   *  CMPEQ      110011
   *  CMPLT      110101
   *  CMPLE      110111

## C++ Learning Quiz

#### (1pt) Q1. What is the value range of ```c++ unsigned short```?

- [ ] -127 to 127
- [ ] -128 to 128
- [ ] -127 to 128
- [x] -128 to 127
- [ ]    0 to 255

Explanation:
  + Using "one's complement" implementation, an unsigned byte is from -127 to 127 (because we store the value -0 and +0 separately, which distinguishes for example nb/infinity or nb/-infinity)
  + Using "two's complement" implementation, an unsigned byte is from -128 to 127 (because here, we store only one value for 0)
  + The link: https://en.cppreference.com/w/cpp/language/types indicates that: "all C++ compilers use two's complement representation, and as of C++20, it is the only representation allowed by the standard"

#### (1pt) Q2. What is the difference between the printf modifiers %d and %i?

- [ ] %d is 16 bits and %i is 32 bits
- [ ] %d is 32 bits and %i is 16 bits
- [ ] %d is unsigned %i is signed
- [ ] %d is signed and %i is unsigned
- [x] There is no difference

Further reading: https://en.cppreference.com/w/cpp/io/c/fprintf

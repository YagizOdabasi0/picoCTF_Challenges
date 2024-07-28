# Description 
* Know of little and big endian?
* Source
* nc titan.picoctf.net 63388

## My Solution 
* Endianness refers to the order in which bytes are arranged within a larger data format, such as a word or a long integer, in computer memory and there are two main types of endianness.
  * Big-endian -> the most significant byte is stored at the lowest memory address.
    * Lets say our hexadecimal number is `0x1A2B3C4D`, for Big-endian, our memory order will be `0x1A2B3C4D`.

  *  Little-endian -> the least significant byte is stored at the lowest memory address.
      *   For Little-endian, our memory order will be `4D3C2B1A0x`.

* In the challenge, first we need to connect to the server by using `nc titan.picoctf.net 63794`
  
    ![image](https://github.com/YagizOdabasi0/profile-icons/blob/main/nc_titan.png)

* Our word is `xzsqv`. By using RapidTables [ASCII Text to Hex Code Converter](https://www.rapidtables.com/convert/number/ascii-to-hex.html), we can convert our word to hex representation.
* `xzsqv` to `787A737176`
* Little-Endian : `7671737A78`
* Big-Endian : `787A737176`
* After submitting the little-endian and big-endian hex values, we receive the flag to complete the challenge.

    ![image](https://github.com/YagizOdabasi0/profile-icons/blob/main/endianness_solution.png)

* Flag : `picoCTF{3ndi4n_sw4p_su33ess_817b7cfe}`

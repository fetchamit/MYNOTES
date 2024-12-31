# Data Encryption
-------------------
* Encryption is a technique that is used to convert data format.
* It converts data from one format to another format.
* Original format of data is known as `Plain Text or simple text` and encrypted format of data is known as `Ciper text or Encrypted text`.
* Encryption is used to implement security feature in a program.
* We have to use encryption to encrypt sensitive data of project like as passwords, otp, User Id, parameters of URL's etc.
* There are various encryption techniques that are used to encrypt a data. Like as MD5 algorithm,RSA Algorighm etc.
* A User/Programmer can also create it's own encryption algorighm.

## What is MD5
* MD5 is a function that is used to encrypt some data.
* It is not an encryption algorithm it is an encryption function.
* It uses concepts of `Hashing` to encrypt data. Hashing addes some `random garbage data ` in original data.
* After doing encryption by using MD5 we can not decrypt that data.
* `HashCracking` is a technique that is used to guess the hash to decrypt data but it is very almost `impossible` to crack hash data.
* `MD5.Create()` function is used to work with MD5 technique.
* We have to install `System.Security.Cryptography.Algorithms` namespace from nuget package in our project. After that we can use various algorithms of encryption.

## Steps to Implement Cryptography
* Step 1: Install a package inside Nuget package manager and search for `System.Security.Cryptography.MD5` and install `System.Security.Cryptography.Algorithms`.


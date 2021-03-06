# Cryptography (March 30, 2018)

## **Symmetric cipher:**

### Definition

A ***symmetric cipher*** is a reversible mathematical transform **E** whose computation depends, in both directions (direct and inverse), of the same secret information, called a ***Key***. 

Where The same key is used for **encryption AND decryption**

##### Encryption:

To start, we input the **message and key** into the **encryption algorithm** 	

> ​		[ *Message* ] ==> [ *Encryption* ] <== [ *Key* ] 

Which will thusly output the **cipher text**

> ​		[ *Encryption*] ==> [ *Cipher text*]

### Stream Ciphers

- Stream ciphers


- Block ciphers

## *Stream Ciphers*

>  **The transform E** applies to messages of **any size by operating bitwise**.
>
>  > **E** : ( { 0, 1 }^k )  *  ( { 0, 1 } * )  -->  {0,1}* 
>
>  (The cipher text length = the plain text length)
>
>  #### From Caesar to RC4 and beyond:
>
>  ​	Historical evolution of the stream cipher concept, from the Roman Empire to the era of the internet
>
>  ​	**String algorithms**, when inadequately integrated, can easily conduct to a weak system (recurrent design error)

## *Caesar Cipher*

> Technique adopted by Julius Caesar to exchange messages with his generals.
>
> Consists of replacing each letter from the message by the third letter after it in the Latin alphabet
>
> ***Advantage:*** 
>
> ​	Increased decryption cost for the adversary, who does not know the key
>
> ***Disadvantage***: 
>
> ​	Once you know how to break the cipher, you can decrypt any message
>
> ```
> Note: Latin alphabet has no U, W or J
> ```
>
> ***
>
> ### Generalization:
>
> The key in the  **Caesar cipher** is the displacement of the letters in the alphabet, and can be itself 			represented by a letter according to the numbering ( namely, K = 3 = D )
>
> Obviously, there's nothing special in the value k = 3
>
> ### Exercise:
>
> ​	Decrypt the following message:
>
> ​			RH EINR HNBHN SIXH FCANA HXOX PNIGN IXQRBQX
>
> ​	Answer: ( in Latin )
>
> ​			ET QVAE TANTA FVIT CAVSA TIBI ROMAM VIDENDI

## Vigenere Cipher

> The **key** can consist of several characters:
>
> > K  = ( k <sub>0</sub> ), ( k <sub>0</sub> ), ...  ( k <sub>n-1</sub> ) 
> >
> > ​	(Cyclically repeated)
>
> #### Cifra de Vigenere
>
> > ( C <sub>i</sub> ) <== (M <sub>i</sub> )  ( k <sub>*i*mod*n*</sub>) mod ( k <sub>n-1</sub> ) 
>
> **Advantage**: 
>
> ​	Exponentially increased decryption cost for the adversary ( P<sup>n</sup> chaves possiveis )

## Vernam Cipher:

> Arbitrary sets of *p* characters as alphabets
>
> In the extreme case, p = 2 (binary alphabet): 
>
> > C <sub>i</sub> <-- (M <sub>i</sub> +  K<sub>imodn</sub>)mod2 = M <sub>i</sub> ***XOR*** K<sub>imodn</sub>

## One-Time Pad

> Entirely **random key** of the **same length as the message** itself
>
> One time pad:
>
> > C<sub>i</sub> <-- M<sub>i</sub> XOR K<sub>i</sub>
>
> **Advantage**: unconditionally secure (Shannon's Theorem)
>
> **Disadvantage**: the problem of protecting the message "reduces" to the problem of protecting the key




0.01 BTC Puzzle by Corey Phillips
Status: UNSOLVED
Prize: 0.01 BTC
Creator: Corey Phillips
Start Date: 2019-07-09
Address: bc1qcyrndzgy036f6ax370g8zyvlw86ulawgt0246r 
 0.01
 0.01
 1
Description
The mnemonic for the kitten photo without a passphrase contains roughly 0.00095133 BTC. Feel free to claim it if you manage to sweep the keys in time.

As a challenge, I have also sent 0.01 BTC to the following address, “bc1qcyrndzgy036f6ax370g8zyvlw86ulawgt0246r”. This address was generated using the kitten image along with a BIP39 passphrase. If you manage to claim it, congrats!

0.01 BTC Puzzle by Corey Phillips

Source: https://twitter.com/aantonop/status/603701870482300928

Solution
Every file can be broken down, defined and represented as a Base64 string. Bitimage extracts the Base64 string from the data URI of any file that you feed it and uses that string to generate a mnemonic phrase.

The Base64 string for the kitten image is rather long so I’ve shortened it for presentation purposes here, “/9j/4AAQSkZJRg …. +MbzXZF3n/2Q==”. Since the Base64 string is rather unwieldy we hash it using the sha256 hash function leaving us with the following, “1808d35318ac7cb98b69ff9779b699d6a631f15e0b353ac89b7c4020774832ed”.

We then pass this hash off to bip39’s “entropyToMnemonic” function to generate our mnemonic phrase. With the mnemonic phrase in hand we can generate our seed with or without a passphrase. Including a passphrase will prevent any random person with access to the file from accessing our funds, assuming the passphrase is sufficient and cannot be easily brute-forced.

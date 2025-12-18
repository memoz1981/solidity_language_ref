### General

- There are two kinds of accounts in Ethereum which share the same address space: **Externally-owned accounts** that are controlled by public-private key pairs (i.e. humans) and **contract accounts** which are controlled by the code stored together with the account.

### Storage, Transient Storage, Memory and the Stack

- 4 Places to store data -> Storage, Transient Storage, Memory and the Stack

#### Storage

- persistent between function calls and transactions
- key-value store that maps 256-bit words to 256-bit words
- costly

#### Transient Storage

- Similar to storage -> but persists only within the tranaction, and then resets
- cost lower than storage

#### Memory

- Allocates for each function call
- Linear
- Reads are limited to 1 word = 256 bits = 32 bytes
- Writes -> either 8 bit or 256 bits wide
- Memory is expanded by words (256 bits) for read/write 
- Gas should be paid for each memory expansion
- cost of memory increases quadratically as it increases

#### Stack

- All calculations happen in stack
- 
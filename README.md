# 8D-DAG-Lattice-Encryption
8D DAG Lattice Encrtption
Libraries:
The code includes various libraries such as <iostream>, <vector>, <random>, <sstream>, <iomanip>, <fstream>, <memory>, <thread>, <bitset>, and <chrono>. These libraries provide functionalities for input/output, data structures, random number generation, string manipulation, multithreading, and timing.

Structures:

LatticeSymbol: Represents a lattice symbol with Unicode symbol, color, shade, and complexity.
DAGNode: Represents a node in the Directed Acyclic Graph (DAG) structure. It contains a vector of parent indices and a LatticeSymbol.
createLattice Function:

Generates an 8D lattice structure based on the provided dimensions (width, height, depth, time, energy, spirit, mind, soul).
Uses a random number generator to assign random Unicode symbols, colors, shades, and complexity values to each lattice node.
Connects the lattice nodes based on adjacency, establishing parent-child relationships.
encryptMessageWithDiffusion Function:

Takes a message and the generated lattice structure as input.
Converts each character of the message to its corresponding lattice index.
Retrieves the Unicode symbol from the lattice at the computed index.
Stores the symbols in a vector (encryptedData) and returns it.
decryptMessageWithDiffusion Function:

Takes the encrypted data (vector of Unicode symbols) and the lattice structure as input.
Iterates over each symbol in the encrypted data.
Searches the lattice for the corresponding index that matches the symbol.
Converts the lattice index to the original character and constructs the decrypted message.
unicodeToString Function:

Converts a list of Unicode code points (vector of unsigned integers) to a string representation by converting each code point to its hexadecimal representation.
xorWithKey Function:

Performs the XOR operation between the message (vector of unsigned integers) and a given key (vector of unsigned integers).
The key is repeated cyclically to match the length of the message.
Returns the result as a vector of unsigned integers.
parallelEncryptWithDiffusion Function:

This function is used to encrypt a portion of the message in parallel using multiple threads.
It takes the message, lattice structure, and the range of indices to encrypt.
Generates an artificial delay (1 to 1000 microseconds) to simulate encryption complexity.
Retrieves the lattice index corresponding to each character of the message and stores the symbol in the encryptedData vector.
main Function:

Initializes the dimensions of the lattice (width, height, depth, time, energy, spirit, mind, soul).
Creates the 8D lattice structure using the createLattice function.
Defines a message to be encrypted ("Hello, World!") and an empty vector (encryptedData) to store the encrypted symbols.
Determines the number of threads based on the hardware concurrency.
Divides the message into chunks and assigns each chunk to a separate thread for parallel encryption using the parallelEncryptWithDiffusion function.
Joins all the threads once encryption is complete.
Decrypts the encrypted data using the decryptMessageWithDiffusion function.
Prints the original message, encrypted data in Unicode format, and the decrypted message.
Overall, this code generates an 8D lattice structure with random symbols, colors, shades, and complexity. It then encrypts a given message by mapping each character to its corresponding lattice symbol and stores the encrypted data. The encryption process can be parallelized using multiple threads. Finally, the encrypted data is decrypted back to the original message using the lattice structure.

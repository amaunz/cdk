# CDK

Calculate CDK descriptors.
Input: SDF. With 3D coordinates present more descriptors are calculated.
Output: CSV, with SMILES as row identifiers and descriptor names in the columns.

Compile:

  javac -cp "*.jar:." ApplyCDKDescriptors.java

Run:

  java -cp "*.jar:." ApplyCDKDescriptors

This runs the program on the hard-coded (hamster) input file and calculates all descriptors (see main function).

API:

  ApplyCDKDescriptors acd = new ApplyCDKDescriptors("/path/to/input.sdf", "/path/to/output.csv", "Desc1,Desc2,...,Descn")

This runs the program on the specified input file and calculates the specified descriptors. Set to empty string to calculate all descriptors.
Descriptors are a subset of the ones listed here: http://pele.farmbio.uu.se/nightly/dnames.html. Use the names from the first column and append `Descriptor`.

Example: Use `LargestChainDescriptor` when `LargestChain` should be calculated.


# cibyl-testing
Repository for validating Cibyl compiler (mips-cibyl-elf-gcc) and toolchain builds.

Latest version of the Cibyl environment can be downloaded from here:  https://github.com/DeviousMalcontent/cibyl/releases

## Testing process: 

After forking this Repository,

Using a fresh workspace, pull down the latest build with:
```
wget https://github.com/DeviousMalcontent/cibyl/releases/download/v180/mips-cibyl-elf.tar.bz2
```

Extract it with:
```
tar -xjf mips-cibyl-elf.tar.bz2
```

Install a reference to the compiler with:
```
echo 'export PATH="/workspaces/cibyl-testing/mips-cibyl-elf/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

Then ```cd hello``` and run **make**.

After confirming that the jar executable has been compiled, run it with the following command:

```
java -jar program.jar
```

The expected result is a Hello, World! to be printed on the screen.
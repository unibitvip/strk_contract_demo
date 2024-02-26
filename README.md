
```
$ scarb build
   Compiling strk_contract v0.1.0 (/Users/zhuxh/RustHub/strk_contract/Scarb.toml)
    Finished release target(s) in 1 second
```

```
$ starkli declare target/dev/strk_contract_hello.contract_class.json
Enter keystore password: 
Sierra compiler version not specified. Attempting to automatically decide version to use...
Network detected: goerli. Using the default compiler version for this network: 2.4.0. Use the --compiler-version flag to choose a different version.
Declaring Cairo 1 class: 0x0074cfb9e423d32c130d359987a70600b81da685712f076d44c3eb8d43f67a9a
Compiling Sierra class to CASM with compiler version 2.4.0...
CASM class hash: 0x062e3c287124d6f6b37b7c55d2ce336fdf07f6402fca77efdc2cd2a7d478a3bb
Contract declaration transaction: 0x00516d20ab86b3351ead27ca77702e41c0b98e22edaf396cad690eb67e221191
Class hash declared:
0x0074cfb9e423d32c130d359987a70600b81da685712f076d44c3eb8d43f67a9a
```

https://goerli.voyager.online/

https://goerli.voyager.online/class/0x0074cfb9e423d32c130d359987a70600b81da685712f076d44c3eb8d43f67a9a


```
% starkli to-cairo-string starknetbook
0x737461726b6e6574626f6f6b

$ starkli deploy \
        0x0074cfb9e423d32c130d359987a70600b81da685712f076d44c3eb8d43f67a9a \
        0x737461726b6e6574626f6f6b

Enter keystore password: 
Deploying class 0x0074cfb9e423d32c130d359987a70600b81da685712f076d44c3eb8d43f67a9a with salt 0x01e4cab06dabbca4e55f9a156bd13ddaf8a8c1381e86bbc39c2c8ce25a055709...
The contract will be deployed at address 0x04412ad67b518c21ace2078d9dbf2178b346f0183d8bcdd0a79542aaa1b8f1fa
Contract deployment transaction: 0x04e4c9b8794430a8a54838b7fe3d756b7e2338fd093d7111d842cd2169726b0f
Contract deployed:
0x04412ad67b518c21ace2078d9dbf2178b346f0183d8bcdd0a79542aaa1b8f1fa

```

```
% starkli to-cairo-string hellostark
0x68656c6c6f737461726b


$ starkli call \
    0x04412ad67b518c21ace2078d9dbf2178b346f0183d8bcdd0a79542aaa1b8f1fa \
    get_name

[
    "0x0000000000000000000000000000000000000000000068656c6c6f737461726b"
]

$ starkli parse-cairo-string 0x0000000000000000000000000000000000000000000068656c6c6f737461726b
hellostark
```

```
$ starkli to-cairo-string histark   
0x6869737461726b

% starkli invoke \
    0x04412ad67b518c21ace2078d9dbf2178b346f0183d8bcdd0a79542aaa1b8f1fa \
    set_name \
    0x6869737461726b

Enter keystore password: 
Invoke transaction: 0x05327096ae5d68d23d433e7efa2f38775b7bda2735ef398024a55d1fceb9e586

https://testnet.starkscan.co/tx/0x5327096ae5d68d23d433e7efa2f38775b7bda2735ef398024a55d1fceb9e586
```

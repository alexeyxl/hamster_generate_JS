# hamster_generate_JS: JS library for generate wallets on bip39

A lightweight Monster's implementation for generate wallets on bip39. Used libs: ethereum-cryptography and @noble 


Fully compatible with MinterTeam/minterjs-wallet:
const wallet = ent.generateWallet();
const wallet = ent.walletFromMnemonic('surround tape away million into program organ tonight write prefer inform cool');
const wallet = ent.walletFromPrivateKey(privateKey);
wallet.getAddress();
wallet.getAddressString();
wallet.getMnemonic();
wallet.getPrivateKey();
wallet.getPrivateKeyString()
wallet.getPublicKey();
wallet.getPublicKeyString()

const mnemonic = ent.generateMnemonic()
const isValid = isValidMnemonic('surround tape away million into program organ tonight write prefer inform cool');

Main functions:
#entropy
##ent.entropy.new(strength, rng)
  ent.entropy.new() it's similar ent.entropy.new(128)
  ent.entropy.new(256) .... 
  rng - for fixed entropy
  result new entropy // Uint8Array(32) [129, 13, 149, 8, 140, 200, 101, 126, 108, 187, 59, 170, 125, 190, 132, 140, 115, 227, 80, 47, 74, 164, 227, 32, 9, 213, 206, 67, 4, 99, 4, 246, buffer: ArrayBuffer(32), byteLength: 32, byteOffset: 0, length: 32, Symbol(Symbol.toStringTag): 'Uint8Array']
##ent.entropy.isValide(entropy)
  result true / false 




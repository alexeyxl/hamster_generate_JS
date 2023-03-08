# hamster_generate_JS: JS library for generate wallets on bip39<br/>

A lightweight Monster's implementation for generate wallets on bip39. Used libs: ethereum-cryptography and @noble <br/>


Fully compatible with MinterTeam/minterjs-wallet:<br/>
const wallet = ent.generateWallet();<br/>
const wallet = ent.walletFromMnemonic('surround tape away million into program organ tonight write prefer inform cool');<br/>
const wallet = ent.walletFromPrivateKey(privateKey);<br/>
wallet.getAddress();<br/>
wallet.getAddressString();<br/>
wallet.getMnemonic();<br/>
wallet.getPrivateKey();<br/>
wallet.getPrivateKeyString()<br/>
wallet.getPublicKey();<br/>
wallet.getPublicKeyString()<br/>
<br/>
const mnemonic = ent.generateMnemonic()<br/>
const isValid = isValidMnemonic('surround tape away million into program organ tonight write prefer inform cool');<br/>
<br/>
Main functions:<br/>
#entropy<br/>
##ent.entropy.new(strength, rng)<br/>
  ent.entropy.new() it's similar ent.entropy.new(128)<br/>
  ent.entropy.new(256) .... <br/>
  rng - for fixed entropy<br/>
  result new entropy // Uint8Array(32) [129, 13, 149, 8, 140, 200, 101, 126, 108, 187, 59, 170, 125, 190, 132, 140, 115, 227, 80, 47, 74, 164, 227, 32, 9, 213, 206, 67, 4, 99, 4, 246, buffer: ArrayBuffer(32), byteLength: 32, byteOffset: 0, length: 32, Symbol(Symbol.toStringTag): 'Uint8Array']<br/><br/>
##ent.entropy.isValide(entropy)<br/>
  result true / false <br/><br/>




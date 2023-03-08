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
#ent.entropy<br/><br/>
ent.entropy.new().....
##.new(strength, rng)<br/>
  strength = 128 (is def) || 160 || 192 || 224 || 256<br/>
  rng - it's a fixed entropy<br/>
<br/>
##.isValide(entropy)<br/>
  result true / false <br/>
  <br/>
##.toPositions(entropy)<br/>
  in result array of words mnemonic possitions<br/>
<br/>
##.toMnemonic(entropy,wordlist)<br/>
  in lib exist default wordlist<br/>
  <br/>
##.toSeed(entropy, pswd, wordlist)<br/>
##.toHdkey(entropy, pswd, wordlist,path = {})<br/>
##.toPrivKey(entropy, pref, pswd, wordlist)<br/>
  if used pref (for example '0x') return 0xA1d3........ else return Buffer Array <br/>
##.toPubKey(entropy, pref, pswd, wordlist)<br/>
   if used pref (for example '0x') return 0xA1d3........ else return Buffer Array<br/>
##.toAddress(ent,pref, pswd, wordlist)<br/>
   if used pref (for example 'Mx') return MxA1d3........ else return 0xA1d3........<br/>
   <br/><br/>
#ent.mnemonic<br/><br/>
##.new(strength, rng, wordlist)<br/>
##.isValide(mnemonic, wordlist)<br/>
  result true / false <br/>
##.toPositions(mnemonic,wordlist)<br/>
##.toSeed(mnemonic,pswd)<br/>
##.toHdkey(mnemonic,pswd,path)<br/>
##.toPrivKey(mnemonic,pref,pswd,path)<br/>
##.toPubKey(mnemonic,pref,pswd,path)<br/>
##.toAddress(mn,pref, pswd,path)<br/>
<br/><br/>
#ent.seed<br/><br/>
##.isValide(seed)<br/>
##.toHdkey(seed, path)<br/>
##.toPrivKey(seed,pref, path)<br/>
##.toPubKey(seed,pref, path)<br/>
##.toAddress(seed, pref , path)<br/>

#ent.privKey<br/><br/>
##.new(strength, pref , pswd, rng, wordlist, path)<br/>
##.format(privKey,pref)<br/>
  return formated private key in array [private key without prefix, prefix]<br/>
##.isValide(privKey)<br/>
##.toPubKey(privKey,pref)<br/>
##.toAddress(privKey, pref)<br/>

#ent.pubKey <br/><br/>
##.isValide(pubKey)<br/>
##.format(pubKey,pref)<br/>
 return formated publick key in array [publick key without prefix, prefix]<br/>
##.toAddress(pubKey, pref)<br/>

#ent.wallet <br/><br/>
##.new(strength, rng, wordlist, path)<br/>
##.fromMnemonic(mnemonic,path)<br/>
##.fromPrivate(privKey,path)<br/>

#ent.address <br/><br/>
##.isValide(address,pref,len)<br/>
  len is default = 40<br/>
  pref if need check by prefix for example 'Mx'<br/>
##.format(address,pref,len)<br/>
##.toBufAddress(addr,pref,len=40)<br/>


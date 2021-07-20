# Releases

## Binary Integrity Check

All released files after 3.7 will provide signatures signed by the Tron Account: `TKeAcHxgErbVXrG3N3TZiSV6AT566BHTj2`.

### Signature Verification

You can verify the signature by tronweb.

```js
const Trx = require('tronweb').Trx;

console.log(Trx.verifySignature(SHA256, ADDRESS, SIGNATURE));
```

Suppose we got a `FullNode.jar` with a SHA256 hash `2fca93b09da4ac62641e03838e77fce99b4711ddb0c09aa91656c80fc9556d2e`, and a Tron signature `21435e32131feb6d00ba8048df04e112e02569ec851064d8ecad2d4dd5da44b7628ddce16823dadfff6fd683fc58cee74964970621a845ee459e2c96a750de551b`.

To verify the integrity of the released file:

```shell
# First calculate the sha256 hash

sha256sum FullNode.jar  # or shasum -a 256 FullNode.jar (macOS)
# 2fca93b09da4ac62641e03838e77fce99b4711ddb0c09aa91656c80fc9556d2e  FullNode.jar

# Then check the signature

npm install -g tronweb
node -e 'console.log(require("tronweb").Trx.verifySignature(
    "2fca93b09da4ac62641e03838e77fce99b4711ddb0c09aa91656c80fc9556d2e",
    "TKeAcHxgErbVXrG3N3TZiSV6AT566BHTj2",
    "21435e32131feb6d00ba8048df04e112e02569ec851064d8ecad2d4dd5da44b7628ddce16823dadfff6fd683fc58cee74964970621a845ee459e2c96a750de551b"
  ))'
# true

# Now you've verified the integrity of the binary release file.
```

### Version Signature
- Odyssey-3.7 
```shell
FullNode sha256sum: 2fca93b09da4ac62641e03838e77fce99b4711ddb0c09aa91656c80fc9556d2e  
FullNode signature: 21435e32131feb6d00ba8048df04e112e02569ec851064d8ecad2d4dd5da44b7628ddce16823dadfff6fd683fc58cee74964970621a845ee459e2c96a750de551b   
SolidityNode sha256sum: fcdea8b3e511306218ba442fb0828f0413574012d646c39c212a59f6ba5844bc  
SolidityNode signature: 6dcad6e02f17467e5cfebeefa0f9963da08e7da10feebefdec47d689fecc30f104c9b7f5e784b883e7ceb786fe55188356c42c306d727fb7819eed2a71f788361c  
```

- GreatVoyage-4.0.0
```shell
FullNode sha256sum: d3f8f9fde64bdefaadae784d09de97172e5e8a3fe539217e12b89963983a530d  
FullNode signature: e788dbaf2fe35f099f65b2403cfb0d7cbe7f4611f8c5ff8151e4bd84ae468d2e541043c9cde9e74500003027ae9f25cdda81a9bcd60abb45ca7a69f965f4dcc71c  
SolidityNode sha256sum: adddf88423c6c31f1f25ed39b10779c24dd7cdcf37f2325c02b2f2ecfc97e1f6  
SolidityNode signature: e3b9859f178f7851dedb7a0a8deb715e5f1e3af10b1064c36f2727ec2b8825510df4fd7b09d7d049204e5df3e8d5b87778e83a15ca96ce786f7977a6cb48bca91b  
```

- GreatVoyage-4.1.1
```shell
FullNode sha256sum: 30e716b86b879af1e006c2b463903ae3835e239e32e2b01c2a1b903a153897fe  
FullNode signature: 5faee65a448bb9aa77835992ca3d24e50d8a76b7934f80664ad38e83179c8114278fdef4494de7231f8e40de86461676a7aa4a54c795f4c692e91d90e156ec471b  
SolidityNode sha256sum: 10a160181053b421109ecace74df5fc0f8860bc8a70181add65fd9a292c35a44  
SolidityNode signature: 1d1413b13adf7778f9a720294eca066ac728ad636d166505276f5ff1f63973c100c04778f937f240f10107edb7de477604857867fc4dbdb68238169c978fc3da1b  
```

- GreatVoyage-v4.1.2
```shell
FullNode sha256sum: 4ded44b6c1a3dbd25212e14ab413142b5463dcbf30a528f83ded529048542547
FullNode signature: 57a094c1b8a5ec301ef913eb718de2498b5695eb999530863df05252ba8919ba6866c8490e29d36f7dbf34537c898ece5ef0111efb134419c3a5fd6fc9ec03b81c
SolidityNode sha256sum: 3db36cadbd1f7641aafc8164983f28df4b7ceff8174e090327ed407012cf12cb
SolidityNode signature: d07604f6811cbed628dd6e5c07880c2fdd3025848fd5365925531c7748467d5228fea2e18326864acc27f3b51c73b364fa44c450d8ec4b5080a7ddb7566724701c
```

- GreatVoyage-v4.1.3(Thales)
```shell
FullNode sha256sum: c5fb99ad5b024bb7877118f30fb6065f6e6febd11a3cfa241521cbed73cca181
FullNode signature: d80ec371e791c4316925d80ff3400cf51b14c8a4d4c696b7817c517eb094823622932b45b9b37f9e9657513c3eddb1134fbbb1ee56727c0957e8a3b40c67409b1c
SolidityNode sha256sum: 4b941d71b561a8b2e0b97d7498823d900eaf287910eea1eaafc649f5aad14036
SolidityNode signature: f8a8e8d411b009d02986cad1e19e745f8107384a274f146bcae60c570111b13556ff9ab528eb5d1fb4734bd4ef488ade4038781d06ab6420e35f28be6135fe9b1c
```

- GreatVoyage-v4.2.0(Plato)
```shell
FullNode sha256sum:
bbf103432be016b582452137b4862140af15ccf7c5daa9be738450705317fdb8
FullNode signature:
326701699a5eb8d497eb454b5b74c1559961417fb6f262b4e6314052d73f5977312e0450937fa485236f51f706b434acf8659ce1325d704097c5748629e736ef1c
SolidityNode sha256sum:
1db544cbca9dc814683ccf9bef28f7d6ca4469289052230394aaf4e3bcd08615
SolidityNode signature:
47fea27df940db0d2a4c0abf6d06969882c027bc4f17449205a28ae5cd25b8ba5339e21f105fe1c25e799d0f4ffea64a15046b9baf5b54341411b5180da439011b
```

- GreatVoyage-v4.2.1(Origen)
```shell
FullNode sha256sum:
9888710c915a4027f1bc3dcb1d5d983e0c00d4c438f6fa307d412f62ff6862ea
FullNode signature:
6e7d8ef9d033ebf9213118b7511f4ecc5def97442844fbd34de3ef76dd417a0d45da3e2e70fc213475d7fc0a44df1c54732874d858ec980159c5dbffc975680a1c
SolidityNode sha256sum:
c70edffa3022e9c25bf845ee978e3500c3ada89b473d895a715acf1738b83f10
SolidityNode signature:
0e366acce33bb7c6b02fa143a57d9380c94d3513a9fba8692efe2862a8f7df93156edbddd075f1844f2f81398b14f2db6a03e21f0f6b8ab25649fae4dc16ae731b
```

- GreatVoyage-v4.2.2(Lucretius)
```shell
FullNode sha256sum:
8a7f8143b3351ea6b5d8e3dfc857b09256d363d4907ba3ab0288f67f77c2a58f
FullNode signature:
71c6300ace5cbf16d78a32aa4602c3f129cb768e32acffaecd17b4134b5955bf37efda1d27025e894e521184a21174e5eddf4e7d1f86761657827795cbddfcfd1c
SolidityNode sha256sum:
2d0d5334a232b7b74df8ed3211d9e0ac957894f81e9172010732f2159da261ad
SolidityNode signature:
0696f8cb3c65324c4b04f9ecf89d939bf7e1b955144e3fe75eeca6bd4c639e463afbe24e31ae38a6889d4d0649ae03fafeeb7c337b34a36fbac33962f64651671b
```

- GreatVoyage-v4.2.2.1(Epictetus)
```shell
FullNode sha256sum:
8bd040a8db16ccba3e957ed3558b82d145928153a53f9688302849658a72f9bc
FullNode signature:
3137a8ba8fa5556e4c4a7597aec8f5f46ebb79a64edcf9e2925d2e3314afde3e0f42fd4080e5e4f4d3d1eff263d30478b0322e6dbcc71c43b534f614004b5c561b
SolidityNode sha256sum:
ee8abd39732e4901828a61124880f1d2eab62f7f3d97150f1e1921bf7da10e54
SolidityNode signature:
092b08184677449dd283a31cc486f994166cd9f5ad312a9c80d3e06689ec540774ac9a1334dffeb6412039ed70ee912ead39c4025dd69b688ea9df4dd831b5771c
```
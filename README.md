# Cerastes

> _Cerastes_ is a genus of small vipers, often hiding by burying themselves in the sand. These are ambush predators that lie buried in the sand, waiting for prey to pass by. -Wikipedia.

<img width="2560" height="1198" alt="image" src="https://github.com/user-attachments/assets/08d7c133-b9c1-48fc-87be-7a679a42371b" />

Cerastes is a compact, single-file HTML tool that obfuscates your code using XOR-based encryption at runtime. It takes your Unicode input, generates a random key matching its length, and encrypts the code byte by byte-producing a fully obfuscated output.

Alongside, Cerastes creates a lightweight JavaScript snippet that automatically decrypts the code at runtime and injects it into the DOM.

Like its namesake-the horned desert viper-Cerastes is small, stealthy, and strikes without being seen.

## Example Output:

**For the following input**:
```javascript
alert("Boo! 👻");
```

**The key generates randomly, so you'd get something like this**:
```javascript
const d=[87,89,85,71,71,24,88,46,25,95,71,75,149,229,226,218,70,31,77];
const k="650530zlv0fkezsad6v";
const s=document.createElement("script");
const y=d.map((v,i)=>String.fromCharCode(v^k.charCodeAt(i%k.length))).join("");
const z=new TextDecoder("utf-8").decode(Uint8Array.from(y,(c)=>c.charCodeAt(0)));
s.innerHTML=z;
document.body.appendChild(s);
```

## Contributions

If you have suggestions or something isn't working - please open an issue with all the details, also, attach example inputs and outputs.

Contibutions are always welcomed, just fork the project, implement your code and create a PR.

## Disclaimer & Responsible Use

While Cerastes can be used to obscure JavaScript for protection, testing, or novelty, it must not be used to hide malicious behavior or violate any terms of service, platform guidelines, or local laws.

The author assumes no liability for misuse of this tool. Always use obfuscation tools ethically and responsibly.

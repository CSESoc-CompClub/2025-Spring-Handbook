# 🕵️ SUBSTITUTION CIPHERS 🕵️
Substitution ciphers are where one character is replaced by another character. 

## Frequency & Word Analysis
<a href="https://brianveitch.com/websites/cryptography/random.html" target="_blank">Decryption helper website</a>
<a href="https://webspace.maths.qmul.ac.uk/b.noohi/MTH6115/SubTool.html" target="_blank">Decryption helper website from the lecture</a>


<a href="https://www.boxentriq.com/code-breaking/frequency-analysis" target="_blank">Frequency analysis website</a>

> [!TIP] Breaking substitution ciphers tips
> - Look for one/two letter words
> - Look for apostrophes
> - Look for repeating letters
> - Use the above website to analyse the frequency of words and compare against common letters

## Decrypting Substitution Ciphers
> [!SUCCESS] Task
> Decrypt the following ciphers. Note that **punctuation matters** when inputting your answers. Upper and lower case does not matter.
> 
> The following all have different cipher keys.

### Cipher 1
VJIF RPF GJPY XPFRE, VJIF RKDAFLF XPFREYFVV, RYH VJIF DRLF XPFREYFVV EDPUVE UNJY EDFI.

<!-- rgkhfwxdaotqiyjnmpveulbzsc -->
<div class="answer-box">
    <input class="answer-input" type="text" id="answerinput1" placeholder="Enter your answer">
    <button class="answer-button" onclick="checkAnswer('answerinput1', 'result1', 'U29tZSBhcmUgYm9ybiBncmVhdCwgc29tZSBhY2hpZXZlIGdyZWF0bmVzcywgYW5kIHNvbWUgaGF2ZSBncmVhdG5lc3MgdGhydXN0IHVwb24gdGhlbS4=')">Check Answer</button>
</div>

<div id="result1"></div>

### Cipher 2
HM'S V UZRRI MKHRW, VQCHMHJR. HM NVR MVPT JRT MJ SZCOHQT KTHWKMS JG KVGGJLHRW YTXMKS. VRY SJQTMHQTS MKTI VGT JRT VRY MKT SVQT.

<!-- vcnytuwkhfpoqrjxbgsmzeldia -->
<div class="answer-box">
    <input class="answer-input" type="text" id="answerinput2" placeholder="Enter your answer">
    <button class="answer-button" onclick="checkAnswer('answerinput2', 'result2', 'SXQncyBhIGZ1bm55IHRoaW5nLCBhbWJpdGlvbi4gSXQgY2FuIHRha2Ugb25lIHRvIHN1YmxpbWUgaGVpZ2h0cyBvciBoYXJyb3dpbmcgZGVwdGhzLiBBbmQgc29tZXRpbWVzIHRoZXkgYXJlIG9uZSBhbmQgdGhlIHNhbWUu')">Check Answer</button>
</div>

<div id="result2"></div>

### Cipher 3
DST HTEIFL YEEC TEIC WNOCE WE'TE OK VNEF. OV'L DKCP WNEK WE WIBE WE TEICOLE VNOKML WETE LVTIKME.

<!-- igqheymnoabcfkdxjtlvszwrpu -->
<div class="answer-box">
    <input class="answer-input" type="text" id="answerinput3" placeholder="Enter your answer">
    <button class="answer-button" onclick="checkAnswer('answerinput3', 'result3', 'T3VyIGRyZWFtcyBmZWVsIHJlYWwgd2hpbGUgd2UncmUgaW4gdGhlbS4gSXQncyBvbmx5IHdoZW4gd2Ugd2FrZSB3ZSByZWFsaXNlIHRoaW5ncyB3ZXJlIHN0cmFuZ2Uu')">Check Answer</button>
</div>

<div id="result3"></div>

<script>
    function checkAnswer(inputId, resultId, enAnswer) {
        const input = document.getElementById(inputId);
        const result = document.getElementById(resultId);
        const correctAnswer = atob(enAnswer);
        
        if (input.value.trim().toLowerCase() === correctAnswer.toLowerCase()) {
            result.className = 'correct';
            result.textContent = '✓ Correct Answer!';
        } else {
            result.className = 'incorrect';
            result.textContent = '✗ Incorrect. Try again!';
        }
        
        result.style.display = 'block';
    }
</script>

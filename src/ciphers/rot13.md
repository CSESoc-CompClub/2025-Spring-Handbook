# 🔑 ROT13 CIPHER 🔑
The ROT13 cipher is a substitution cipher where each letter is replaced by the letter 13 places down the alphabet. It is a special case of the Caesar cipher with a shift of 13.

## How It Works
- Replace each letter with the letter 13 positions down the alphabet.
- Wrap around to the beginning of the alphabet if necessary.
- Applying ROT13 twice returns the original text.
- USE YOUR CIPHER WHEEL!

## Decrypting ROT13 Ciphers
> [!SUCCESS] Task
> Decrypt the following ciphers. Note that **punctuation matters** when inputting your answers. Upper and lower case does not matter.
> 
> The following all use the ROT13 cipher.

### Cipher 1
Qvq lbh xabj... Cvenpl jnf na rkgerzryl pbzcrgvgvir ohfvarff. Cvengrf jbhyq bsgra wbva sbeprf jvgu bar nabgure, sbezvat nyyvnaprf naq syrrgf, va beqre gb vapernfr gurve punaprf bs fhpprff naq znkvzvfr gurve cebsvgf.

<!-- ROT13 -->
<div class="answer-box">
    <input class="answer-input" type="text" id="answerinput1" placeholder="Enter your answer">
    <button class="answer-button" onclick="checkAnswer('answerinput1', 'result1', 'RGlkIHlvdSBrbm93Li4uIFBpcmFjeSB3YXMgYW4gZXh0cmVtZWx5IGNvbXBldGl0aXZlIGJ1c2luZXNzLiBQaXJhdGVzIHdvdWxkIG9mdGVuIGpvaW4gZm9yY2VzIHdpdGggb25lIGFub3RoZXIsIGZvcm1pbmcgYWxsaWFuY2VzIGFuZCBmbGVldHMsIGluIG9yZGVyIHRvIGluY3JlYXNlIHRoZWlyIGNoYW5jZXMgb2Ygc3VjY2VzcyBhbmQgbWF4aW1pc2UgdGhlaXIgcHJvZml0cy4=')">Check Answer</button>
</div>

<div id="result1"></div>

### Cipher 2
Va gur pnaqyryvg unyyf bs Ubtjnegf, frpergf geniry snfgre guna bjyf, naq rirel juvfcre pneevrf gur jrvtug bs zntvp naq zvfpuvrs.

<!-- ROT13 -->
<div class="answer-box">
    <input class="answer-input" type="text" id="answerinput2" placeholder="Enter your answer">
    <button class="answer-button" onclick="checkAnswer('answerinput2', 'result2', 'SW4gdGhlIGNhbmRsZWxpdCBoYWxscyBvZiBIb2d3YXJ0cywgc2VjcmV0cyB0cmF2ZWwgZmFzdGVyIHRoYW4gb3dscywgYW5kIGV2ZXJ5IHdoaXNwZXIgY2FycmllcyB0aGUgd2VpZ2h0IG9mIG1hZ2ljIGFuZCBtaXNjaGllZi4=')">Check Answer</button>
</div>

<div id="result2"></div>

<script>
    function checkAnswer(inputId, resultId, enAnswer) {
        const input = document.getElementById(inputId);
        const result = document.getElementById(resultId);
        let correctAnswer;

        try {
            correctAnswer = atob(enAnswer);
        } catch (e) {
            result.className = 'error';
            result.textContent = 'Error decoding the answer. Please contact support.';
            result.style.display = 'block';
            return;
        }

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
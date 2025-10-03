# 🔒 CAESAR CIPHER 🔒
The Caesar cipher is a substitution cipher where each letter in the plaintext is shifted by a fixed number of places down the alphabet.

## How It Works
- Choose a shift value (e.g., 3).
- Replace each letter with the letter that is `shift` positions down the alphabet.
- Wrap around to the beginning of the alphabet if necessary.
- USE YOUR CIPHER WHEEL!

## Decrypting Caesar Ciphers
> [!SUCCESS] Task
> Decrypt the following ciphers. Note that **punctuation matters** when inputting your answers. Upper and lower case does not matter.
> 
> The following all use a Caesar cipher with different shift values.

### Cipher 1
Y qcapcr kcqqyec uyq upgrrcl ml rfc uyjjq md rfc aytcpl, uygrgle dmp qmkcmlc ajctcp clmsef rm qmjtc gr.

<!-- Shift: 3 -->
<div class="answer-box">
    <input class="answer-input" type="text" id="answerinput1" placeholder="Enter your answer">
    <button class="answer-button" onclick="checkAnswer('answerinput1', 'result1', 'QSBzZWNyZXQgbWVzc2FnZSB3YXMgd3JpdHRlbiBvbiB0aGUgd2FsbHMgb2YgdGhlIGNhdmVybiwgd2FpdGluZyBmb3Igc29tZW9uZSBjbGV2ZXIgZW5vdWdoIHRvIHNvbHZlIGl0Lg==')">Check Answer</button>
</div>

<div id="result1"></div>

### Cipher 2
Oek adem jxqj vuubydw oek wuj mxud oekhu ijqdtydw yd q xywx fbqsu... ikttud khwu je zkcf?... Y tedj xqlu yj. - Sqfjqyd Zqsa Ifqhhem.

<!-- Shift: 3 -->
<div class="answer-box">
    <input class="answer-input" type="text" id="answerinput2" placeholder="Enter your answer">
    <button class="answer-button" onclick="checkAnswer('answerinput2', 'result2', 'WW91IGtub3cgdGhhdCBmZWVsaW5nIHlvdSBnZXQgd2hlbiB5b3VyZSBzdGFuZGluZyBpbiBhIGhpZ2ggcGxhY2UuLi4gc3VkZGVuIHVyZ2UgdG8ganVtcD8uLi4gSSBkb250IGhhdmUgaXQuIC0gQ2FwdGFpbiBKYWNrIFNwYXJyb3cu')">Check Answer</button>
</div>

<div id="result2"></div>

### Cipher 3
Liztqvo, pwtl ug pivl. Vwbpqvo jmiba i Rmb bew pwtqlig, ivl zqopb vwe gwc kiv aidm nqnbg xwcvla xmz xmzawv. Bpiba bew pcvlzml xwcvla wnn nwz i niuqtg wn nwcz.

<!-- Shift: 3 -->
<div class="answer-box">
    <input class="answer-input" type="text" id="answerinput3" placeholder="Enter your answer">
    <button class="answer-button" onclick="checkAnswer('answerinput3', 'result3', 'RGFybGluZywgaG9sZCBteSBoYW5kLiBOb3RoaW5nIGJlYXRzIGEgSmV0IHR3byBob2xpZGF5LCBhbmQgcmlnaHQgbm93IHlvdSBjYW4gc2F2ZSBmaWZ0eSBwb3VuZHMgcGVyIHBlcnNvbi4gVGhhdHMgdHdvIGh1bmRyZWQgcG91bmRzIG9mZiBmb3IgYSBmYW1pbHkgb2YgZm91ci4=')">Check Answer</button>
</div>

<div id="result3"></div>

<script>
    function checkAnswer(inputId, resultId, enAnswer) {
        const input = document.getElementById(inputId);
        const result = document.getElementById(resultId);
        let correctAnswer;

        try {
            correctAnswer = atob(enAnswer);
        } catch (e) {
            result.className = 'error';
            result.textContent = e;
            result.style.display = 'block';
            return;
        }

        if (input.value.trim().toLowerCase() === correctAnswer.toLowerCase()) {
            result.className = 'correct';
            result.textContent = '✓ Correct Answer!';
        } else {
            result.className = 'incorrect';
            // result.textContent = '✗ Incorrect. Try again!';
            result.textContent = correctAnswer;
        }

        result.style.display = 'block';
    }
</script>
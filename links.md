---
layout: default
---

## Links

Deputy Director at the <a href="https://consumerchoicecenter.org">Consumer Choice Center</a>

Host of <a href="https://omny.fm/shows/consumerchoiceradio">Consumer Choice Podcast</a>

Collaborator on the <a href="https://fixthemoney.net">Fix The Money</a> podcast and substack

Visiting Fellow at the <a href="https://www.btcpolicy.org/authors/yael-ossowski">Bitcoin Policy Institute</a>

Nostr + Lightning address: <a href="https://nostr.at/npub15dnln6cukw3yrflnv3hnrntdt9amh0uw466u6tns05ymqp3nal4qzz3lfc">yael[at]yael.at</a>

X/Twitter: <a href="https://twitter.com/yaeloss">@YaelOss</a>

LinkedIn: <a href="https://www.linkedin.com/in/yaeloss/">@yaeloss</a>

PayNym (BIP47): <a href="https://paynym.is/+yael">+yael</a>

BTCPay Server:

<style> .btcpay-form { display: inline-flex; align-items: center; justify-content: center; } .btcpay-form--inline { flex-direction: row; } .btcpay-form--block { flex-direction: column; } .btcpay-form--inline .submit { margin-left: 15px; } .btcpay-form--block select { margin-bottom: 10px; } .btcpay-form .btcpay-custom-container{ text-align: center; }.btcpay-custom { display: flex; align-items: center; justify-content: center; } .btcpay-form .plus-minus { cursor:pointer; font-size:25px; line-height: 25px; background: #DFE0E1; height: 30px; width: 45px; border:none; border-radius: 60px; margin: auto 5px; display: inline-flex; justify-content: center; } .btcpay-form select { -moz-appearance: none; -webkit-appearance: none; appearance: none; color: currentColor; background: transparent; border:1px solid transparent; display: block; padding: 1px; margin-left: auto; margin-right: auto; font-size: 11px; cursor: pointer; } .btcpay-form select:hover { border-color: #ccc; } .btcpay-form option { color: #000; background: rgba(0,0,0,.1); } .btcpay-input-price { -moz-appearance: textfield; border: none; box-shadow: none; text-align: center; font-size: 25px; margin: auto; border-radius: 5px; line-height: 35px; background: #fff; }.btcpay-input-price::-webkit-outer-spin-button, .btcpay-input-price::-webkit-inner-spin-button { -webkit-appearance: none; margin: 0; } </style>

<form class="btcpay-form btcpay-form--block" action="https://pay.yael.at/api/v1/invoices" method="POST"><input name="storeId" type="hidden" value="CA5tDjffoAhfTrjctNeF2pifYhdN73Q6CWdF8dTqVQ5M" />
<div class="btcpay-custom-container">
<div class="btcpay-custom"><button class="plus-minus" type="button" data-type="-" data-step="1" data-min="1" data-max="300">-</button>
<input class="btcpay-input-price" style="width: 3em;" max="300" min="1" name="price" step="1" type="number" value="1" data-price="1" />
<button class="plus-minus" type="button" data-type="+" data-step="1" data-min="1" data-max="300">+</button></div>
<select name="currency">
<option selected="selected" value="USD">USD</option>
<option value="GBP">GBP</option>
<option value="EUR">EUR</option>
<option value="BTC">BTC</option>
</select>

</div>
<input class="submit" style="width: 209px;" alt="Pay with BTCPay Server, a Self-Hosted Bitcoin Payment Processor" name="submit" src="https://pay.yael.at/img/paybutton/pay.svg" type="image" />

</form><script>
    function handlePlusMinus(event) {
        event.preventDefault();
        const root = event.target.closest('.btcpay-form');
        const el = root.querySelector('.btcpay-input-price');
        const step = parseInt(event.target.dataset.step) || 1;
        const min = parseInt(event.target.dataset.min) || 1;
        const max = parseInt(event.target.dataset.max);
        const type = event.target.dataset.type;
        const price = parseInt(el.value) || min;
        if (type === '-') {
            el.value = price - step < min ? min : price - step; } else if (type === '+') { el.value = price + step > max ? max : price + step;
        }
    }
    document.querySelectorAll(".btcpay-form .plus-minus").forEach(function(el) {
        if (!el.dataset.initialized) {
            el.addEventListener('click', handlePlusMinus);
            el.dataset.initialized = true;
        }
    });
    
    function handlePriceInput(event) {
        event.preventDefault();
        const root = event.target.closest('.btcpay-form');
        const price = parseInt(event.target.dataset.price);
        if (isNaN(event.target.value)) root.querySelector('.btcpay-input-price').value = price;
        const min = parseInt(event.target.getAttribute('min')) || 1;
        const max = parseInt(event.target.getAttribute('max'));
        if (event.target.value < min) { event.target.value = min; } else if (event.target.value > max) { 
            event.target.value = max;
        }
    }
    document.querySelectorAll(".btcpay-form .btcpay-input-price").forEach(function(el) {
        if (!el.dataset.initialized) {
            el.addEventListener('input', handlePriceInput);
            el.dataset.initialized = true;
        }
    });
</script>


[back](./)

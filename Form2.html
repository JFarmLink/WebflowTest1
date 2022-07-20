<!-- FORM: HEAD SECTION -->

    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
    <meta name="referrer" content="no-referrer-when-downgrade">
            <script type="text/javascript">
        document.addEventListener("DOMContentLoaded", function(){
            const FORM_TIME_START = Math.floor((new Date).getTime()/1000);
            let formElement = document.getElementById("tfa_0");
            if (null === formElement) {
                formElement = document.getElementById("0");
            }
            let appendJsTimerElement = function(){
                let formTimeDiff = Math.floor((new Date).getTime()/1000) - FORM_TIME_START;
                let cumulatedTimeElement = document.getElementById("tfa_dbCumulatedTime");
                if (null !== cumulatedTimeElement) {
                    let cumulatedTime = parseInt(cumulatedTimeElement.value);
                    if (null !== cumulatedTime && cumulatedTime > 0) {
                        formTimeDiff += cumulatedTime;
                    }
                }
                let jsTimeInput = document.createElement("input");
                jsTimeInput.setAttribute("type", "hidden");
                jsTimeInput.setAttribute("value", formTimeDiff.toString());
                jsTimeInput.setAttribute("name", "tfa_dbElapsedJsTime");
                jsTimeInput.setAttribute("id", "tfa_dbElapsedJsTime");
                jsTimeInput.setAttribute("autocomplete", "off");
                if (null !== formElement) {
                    formElement.appendChild(jsTimeInput);
                }
            };
            if (null !== formElement) {
                if(formElement.addEventListener){
                    formElement.addEventListener('submit', appendJsTimerElement, false);
                } else if(formElement.attachEvent){
                    formElement.attachEvent('onsubmit', appendJsTimerElement);
                }
            }
        });
    </script>

    <link href="https://www.tfaforms.com/dist/form-builder/5.0.0/wforms-layout.css?v=1658281087" rel="stylesheet" type="text/css" />

    <link href="https://www.tfaforms.com/uploads/themes/theme-79705.css" rel="stylesheet" type="text/css" />
    <link href="https://www.tfaforms.com/dist/form-builder/5.0.0/wforms-jsonly.css?v=1658281087" rel="alternate stylesheet" title="This stylesheet activated by javascript" type="text/css" />
    <script type="text/javascript" src="https://www.tfaforms.com/wForms/3.11/js/wforms.js?v=1658281087"></script>
    <script type="text/javascript">
        wFORMS.behaviors.prefill.skip = false;
    </script>
        <script type="text/javascript" src="https://www.tfaforms.com/wForms/3.11/js/localization-en_US.js?v=1658281087"></script>
<script type="text/javascript" src="https://js.stripe.com/v2/"></script>
<script type="text/javascript">

    /**
     * Gets the form for Stripe JS usage
     */
    function getStripeForm() {
        return document.querySelector('.wForm > form');
    }

    /**
     * Appends Stripe token input to form after a tokenization call
     * This is "normal" operation
     */
    function appendStripeTokenInputToForm(response) {
        var stripeForm = getStripeForm();
        // attach token to the form so we can pass it to stripe
        var stripeTokenInput = document.createElement("input");
        stripeTokenInput.type = "hidden";
        stripeTokenInput.name = "stripeSourceToken";
        stripeTokenInput.id = "stripeSourceToken";
        stripeTokenInput.value = response.id;
        stripeForm.appendChild(stripeTokenInput);
    }

    /**
     * check if an element is visible
     */
    function isVisible(element) {
        if (element.offsetWidth > 0 && element.offsetHeight > 0) {
            return true;
        }
        return false;
    }

    /**
     * remove invisible elements from a collection
     */
    function removeInvisibleElements(elements) {
        let visibleElements = [];
        if (elements) {
            let i;
            for(i=0;i<elements.length;i++) {
                if(isVisible(elements[i])) {
                    visibleElements.push(elements[i]);
                }
            }
        }
        return visibleElements;
    }

    /**
     * There are cases where forms may hide payment info if conditions are met to skip payment (discount codes, etc)
     * We must try to determine this as best we can in order to figure out if payment info is missing due to respondent error or if it's intended
     * Here we assume that if all the payment info fields are hidden from view, the form is intending to skip payment and treats it as such
     */
    function determineIfStripeTokenizationCallShouldBeMade(ccNumberInput, cvcNumberInput, expiryMonthInput, expiryYearInput) {
        return (ccNumberInput.disabled === false && cvcNumberInput.disabled === false && expiryMonthInput.disabled === false && expiryYearInput.disabled === false);
    }

    /**
     * get value from input
     */
    function getValueFromInput(input) {
        if (input) {
            let choiceMapping = null;
            let mappings = {"credit_card_number":{"id":"tfa_21"},"card_expiration_month":{"id":"tfa_23"},"card_expiration_year":{"id":"tfa_24"},"credit_card_code":{"id":"tfa_25"},"cardholder_full_name":{"id":"tfa_20"},"line_1":{"id":"tfa_2222"},"line_2":{"id":""},"city":{"id":"tfa_2224"},"zip":{"id":"tfa_2226"},"state":{"id":"tfa_2237"},"tfa_2237":{"choice_mapping":{"tfa_2280":"TN","tfa_2270":"NY","tfa_2281":"TX","tfa_2260":"MI","tfa_2271":"NC","tfa_2282":"UT","tfa_2250":"ID","tfa_2261":"MN","tfa_2272":"ND","tfa_2283":"VT","tfa_2240":"AZ","tfa_2251":"IL","tfa_2262":"MS","tfa_2273":"OH","tfa_2284":"VA","tfa_2241":"AR","tfa_2252":"IN","tfa_2263":"MO","tfa_2274":"OK","tfa_2285":"WA","tfa_2242":"CA","tfa_2253":"IA","tfa_2264":"MT","tfa_2275":"OR","tfa_2286":"WV","tfa_2243":"CO","tfa_2254":"KS","tfa_2265":"NE","tfa_2276":"PA","tfa_2287":"WI","tfa_2244":"CT","tfa_2255":"KY","tfa_2266":"NV","tfa_2277":"RI","tfa_2288":"WY","tfa_2245":"DE","tfa_2256":"LA","tfa_2267":"NH","tfa_2278":"SC","tfa_2246":"DC","tfa_2257":"ME","tfa_2268":"NJ","tfa_2279":"SD","tfa_2247":"FL","tfa_2258":"MD","tfa_2269":"NM","tfa_2248":"GA","tfa_2259":"MA","tfa_2238":"AL","tfa_2249":"HI","tfa_2239":"AK"}},"country":{"id":""}};
            switch(input.type) {
                case "radio":
                case "checkbox":
                    if (
                        mappings &&
                        input.checked &&
                        mappings[input.name] &&
                        mappings[input.name]['choice_mapping'] &&
                        mappings[input.name]['choice_mapping'][input.value]
                    ) {
                        choiceMapping = mappings[input.name]['choice_mapping'][input.value];
                    }
                    return choiceMapping;
                case "select":
                case "select-one":
                    if (
                        mappings &&
                        mappings[input.name] &&
                        mappings[input.name]['choice_mapping'] &&
                        mappings[input.name]['choice_mapping'][input.value]
                    ) {
                        choiceMapping = mappings[input.name]['choice_mapping'][input.value];
                    }
                    return choiceMapping;

                default:
                    return input.value;
            }
        }
        return null;
    }

    /**
     * get id or value from stripe (handles both static and webform values)
     */
    function getIdOrValueFromStripe(field)
    {
        if (field && field.value) {
            return field.value;
        } else if (field && field.id) {
            var fieldInput = document.getElementById(field.id);
            if (fieldInput && fieldInput.type == 'radio' && document.querySelector("[name='" + stripe.id + "']:checked")) {
                fieldInput = document.querySelector("[name='" + stripe.id + "']:checked")
            }
            return getValueFromInput(fieldInput);
        }
        return null;
    }

    /**
     * add stripe address fields if applicable
     */
    function addStripeAddressFields(stripeFields)
    {
        stripeFields.address_line1 = getIdOrValueFromStripe({"id":"tfa_2222"});
        stripeFields.address_line2 = getIdOrValueFromStripe({"id":""});
        stripeFields.address_city = getIdOrValueFromStripe({"id":"tfa_2224"});
        stripeFields.address_state = getIdOrValueFromStripe({"id":"tfa_2237"});
        stripeFields.address_zip = getIdOrValueFromStripe({"id":"tfa_2226"});
        stripeFields.address_country = getIdOrValueFromStripe({"id":""});
        return stripeFields;
    }

    /**
     * function to handle the response from stripe createToken
     *
     * @param status
     * @param response
     */
    function stripeCardResponseHandler(status, response) {
        if (response.error) { // Problem!
            stripeErrorHandler(response.error);
        } else { // Token was created!
            Stripe.source.create({
                type: 'card',
                token: response.id
            }, stripeSourceResponseHandler);
        }
    }

    /**
     * Handler for stripe source creation
     *
     * @param response
     */
    function stripeSourceResponseHandler(status, response) {
        if (response.error) {
            stripeErrorHandler(response.error);
        } else {
            appendStripeTokenInputToForm(response);
            var stripeForm = getStripeForm();

            // submit the form
            stripeForm.submit();
        }
    }

    /**
     * Displays error from stripe.js call
     *
     * @param error
     */
    function stripeErrorHandler(error) {
        // inserting our error message after wFormHeader (to match current behavior of the app)
        var wFormHeaderNode = document.getElementsByClassName("wFormHeader")[0];
        // start setting up our error node
        var errorNode = document.createElement("div");
        errorNode.className = "stripeError errorMessage errMsg";
        errorNode.innerHTML = "Please review the error(s) below.<br />"
            + "<ul><li>" + error.message + "</li></ul>";
        wFormHeaderNode.parentNode.insertBefore(errorNode, wFormHeaderNode.nextSibling);
        errorNode.scrollIntoView();
        // make our submit button useable again (wFormsValidation which has already run and passed disabled it)
        var submit = base2.DOM.Element.querySelector(this.target,'.actions .primaryAction[type="submit"]');
        submit.removeAttribute('disabled');
        submit.removeAttribute('style');
        submit.setAttribute('value',submit.getAttribute('data-label'));
    }

    Stripe.setPublishableKey('pk_live_0v0XfpkBXXS85ndPpaMxr3zK00EMXLYwKC');
    document.addEventListener("wFORMSLoaded", function() {
        var stripeForm = getStripeForm();
        stripeForm.addEventListener('submit', function(event) {
            // if we have a stripe error already remove it since we are revalidating
            var errorNode = document.getElementsByClassName('stripeError')[0];

            if (errorNode) {
                errorNode.parentElement.removeChild(errorNode);
            }
            var errFields = document.getElementsByClassName('errFld');
            errFields = removeInvisibleElements(errFields);
            // only try to create a token if we dont have any errors (we re ready to submit actually)
            if (errFields.length <= 0) {
                // Remove stripeSourceToken input if it already exists
                var cardTokenField = document.getElementById('stripeSourceToken');
                if (cardTokenField) {
                    cardTokenField.parentElement.removeChild(cardTokenField);
                }

                var stripeFields = {};

                var creditCardNumberInput = document.getElementById("tfa_21");
                var cvcInput = document.getElementById("tfa_25");
                var expiryMonthInput = document.querySelector("[name='tfa_23']");
                if (expiryMonthInput && expiryMonthInput.type == 'radio' && document.querySelector("[name='tfa_23']:checked")) {
                    expiryMonthInput = document.querySelector("[name='tfa_23']:checked");
                }
                var expiryYearInput = document.querySelector("[name='tfa_24']");
                if (expiryMonthInput && expiryYearInput.type == 'radio' && document.querySelector("[name='tfa_23']:checked")) {
                    expiryMonthInput = document.querySelector("[name='tfa_23']:checked");
                }
                var tokenizationCallShouldBeMade = determineIfStripeTokenizationCallShouldBeMade(creditCardNumberInput, cvcInput, expiryMonthInput, expiryYearInput);
                if (tokenizationCallShouldBeMade === true) {
                    // collect info from stripe mapped fields
                    stripeFields.number = creditCardNumberInput.value;
                    stripeFields.cvc = cvcInput.value;
                    stripeFields.exp_month = getValueFromInput(expiryMonthInput);
                    stripeFields.exp_year = getValueFromInput(expiryYearInput);
                    // full name is not a required field only include if it exists
                                            stripeFields.name = document.getElementById("tfa_20").value;
                                        stripeFields = addStripeAddressFields(stripeFields);
                    // create the token using stripe and use the response handler to deal with the result
                    Stripe.card.createToken(stripeFields, stripeCardResponseHandler);
                    // prevent default we dont want to submit the form until we get our response back
                    event.preventDefault();
                }
            }
        });
    });
</script>
<!-- FORM: BODY SECTION -->
<div class="wFormContainer" >
    <div class="wFormHeader"></div>
    <style type="text/css">
                #tfa_2232,
                *[id^="tfa_2232["] {
                    width: 106px !important;
                }
                #tfa_2232-D,
                *[id^="tfa_2232["][class~="field-container-D"] {
                    width: auto !important;
                }
            
                #tfa_5,
                *[id^="tfa_5["] {
                    width: 240.36363649368286px !important;
                }
                #tfa_5-D,
                *[id^="tfa_5["][class~="field-container-D"] {
                    width: auto !important;
                }
            
                #tfa_20,
                *[id^="tfa_20["] {
                    width: 210px !important;
                }
                #tfa_20-D,
                *[id^="tfa_20["][class~="field-container-D"] {
                    width: auto !important;
                }
            
                #tfa_21,
                *[id^="tfa_21["] {
                    width: 200.36363649368286px !important;
                }
                #tfa_21-D,
                *[id^="tfa_21["][class~="field-container-D"] {
                    width: auto !important;
                }
            
                #tfa_23,
                *[id^="tfa_23["] {
                    width: 40.36363649368286px !important;
                }
                #tfa_23-D,
                *[id^="tfa_23["][class~="field-container-D"] {
                    width: auto !important;
                }
            
                #tfa_23-L,
                label[id^="tfa_23["] {
                    width: 60px !important;
                    min-width: 0px;
                }
            
                #tfa_24,
                *[id^="tfa_24["] {
                    width: 30px !important;
                }
                #tfa_24-D,
                *[id^="tfa_24["][class~="field-container-D"] {
                    width: auto !important;
                }
            
                #tfa_24-L,
                label[id^="tfa_24["] {
                    width: 40px !important;
                    min-width: 0px;
                }
            
                #tfa_25,
                *[id^="tfa_25["] {
                    width: 50px !important;
                }
                #tfa_25-D,
                *[id^="tfa_25["][class~="field-container-D"] {
                    width: auto !important;
                }
            
                #tfa_25-L,
                label[id^="tfa_25["] {
                    width: 120px !important;
                    min-width: 0px;
                }
            
                #tfa_2222,
                *[id^="tfa_2222["] {
                    width: 396px !important;
                }
                #tfa_2222-D,
                *[id^="tfa_2222["][class~="field-container-D"] {
                    width: auto !important;
                }
            
                #tfa_2224,
                *[id^="tfa_2224["] {
                    width: 190.18181824684143px !important;
                }
                #tfa_2224-D,
                *[id^="tfa_2224["][class~="field-container-D"] {
                    width: auto !important;
                }
            
                #tfa_2226,
                *[id^="tfa_2226["] {
                    width: 176px !important;
                }
                #tfa_2226-D,
                *[id^="tfa_2226["][class~="field-container-D"] {
                    width: auto !important;
                }
            
                #tfa_2368-L,
                label[id^="tfa_2368["] {
                    width: 311px !important;
                    min-width: 0px;
                }
            </style><div class=""><div class="wForm" id="4846959-WRPR" dir="ltr">
<div class="codesection" id="code-4846959"><style type="text/css">  .wFormContainer .supportInfo {    display: none; }  .wForm .actions { text-align: center; }</style></div>
<h3 class="wFormTitle" data-testid="form-title" id="4846959-T">Renew Your Membership</h3>
<form method="post" action="https://www.tfaforms.com/api_v2/workflow/processor" class="hintsBelow labelsAbove" id="4846959" role="form">
<div id="tfa_11" class="section group"><div id="tfa_2230" class="section inline group">
<div class="oneField field-container-D    " id="tfa_39-D" role="radiogroup" aria-labelledby="tfa_39-L" data-tfa-labelledby="-L tfa_39-L">
<label id="tfa_39-L" class="label preField reqMark">Registration Amount</label><br><div class="inputWrapper"><span id="tfa_39" class="choices vertical required" aria-required="true"><span class="oneChoice"><input type="radio" value="tfa_2292" class="calc-Amount calcval-25" id="tfa_2292" name="tfa_39" aria-required="true" aria-labelledby="tfa_2292-L" data-tfa-labelledby="tfa_39-L tfa_2292-L"><label class="label postField" id="tfa_2292-L" for="tfa_2292"><span class="input-radio-faux"></span>$25 One-year registration</label></span><span class="oneChoice"><input type="radio" value="tfa_2353" class="calc-Amount calcval-35" id="tfa_2353" name="tfa_39" aria-required="true" aria-labelledby="tfa_2353-L" data-tfa-labelledby="tfa_39-L tfa_2353-L"><label class="label postField" id="tfa_2353-L" for="tfa_2353"><span class="input-radio-faux"></span>$35 Add my $10 contribution</label></span><span class="oneChoice"><input type="radio" value="tfa_2354" class="calc-Amount calcval-50" id="tfa_2354" name="tfa_39" aria-required="true" aria-labelledby="tfa_2354-L" data-tfa-labelledby="tfa_39-L tfa_2354-L"><label class="label postField" id="tfa_2354-L" for="tfa_2354"><span class="input-radio-faux"></span>$50 Add my $25 contribution</label></span><span class="oneChoice"><input type="radio" value="tfa_2355" class="calc-Amount calcval-100" id="tfa_2355" name="tfa_39" aria-required="true" aria-labelledby="tfa_2355-L" data-tfa-labelledby="tfa_39-L tfa_2355-L"><label class="label postField" id="tfa_2355-L" for="tfa_2355"><span class="input-radio-faux"></span>$100 Add my $75 contribution</label></span><span class="oneChoice"><input type="radio" value="tfa_2231" class="calc-Amount calcval-Other" id="tfa_2231" name="tfa_39" aria-required="true" data-conditionals="#tfa_2232" aria-labelledby="tfa_2231-L" data-tfa-labelledby="tfa_39-L tfa_2231-L"><label class="label postField" id="tfa_2231-L" for="tfa_2231"><span class="input-radio-faux"></span>Other</label></span></span></div>
</div>
<div class="oneField field-container-D    " id="tfa_2232-D">
<label id="tfa_2232-L" class="label preField reqMark" for="tfa_2232">Other Amount</label><br><div class="inputWrapper"><input aria-required="true" type="text" id="tfa_2232" name="tfa_2232" value="" min="25" data-condition="`#tfa_2231`" title="Other Amount" class="validate-integer calc-OtherAmount required"></div>
</div>
</div></div>
<div id="tfa_2" class="section group">
<label class="label preField" id="tfa_2-L"><b>Contact Information</b></label><br><div id="tfa_4" class="section inline group">
<div class="oneField field-container-D    " id="tfa_1-D">
<label id="tfa_1-L" class="label preField reqMark" for="tfa_1">First Name</label><br><div class="inputWrapper"><input aria-required="true" type="text" id="tfa_1" name="tfa_1" value="" title="First Name" class="required"></div>
</div>
<div class="oneField field-container-D    " id="tfa_3-D">
<label id="tfa_3-L" class="label preField reqMark" for="tfa_3">Last Name</label><br><div class="inputWrapper"><input aria-required="true" type="text" id="tfa_3" name="tfa_3" value="" title="Last Name" class="required"></div>
</div>
<div class="oneField field-container-D    " id="tfa_5-D">
<label id="tfa_5-L" class="label preField reqMark" for="tfa_5">Email Address</label><br><div class="inputWrapper"><input aria-required="true" type="text" id="tfa_5" name="tfa_5" value="" title="Email Address" class="validate-email required"></div>
</div>
<div class="oneField field-container-D    " id="tfa_2363-D">
<label id="tfa_2363-L" class="label preField reqMark" for="tfa_2363">Phone</label><br><div class="inputWrapper"><input aria-required="true" type="text" id="tfa_2363" name="tfa_2363" value="" autoformat="###-###-####" title="Phone" class="required"></div>
</div>
<div class="oneField field-container-D    " id="tfa_2364-D" role="radiogroup" aria-labelledby="tfa_2364-L" data-tfa-labelledby="-L tfa_2364-L">
<label id="tfa_2364-L" class="label preField reqMark">Type of phone</label><br><div class="inputWrapper"><span id="tfa_2364" class="choices horizontal required" aria-required="true"><span class="oneChoice"><input type="radio" value="tfa_2365" class="" id="tfa_2365" name="tfa_2364" aria-required="true" aria-labelledby="tfa_2365-L" data-tfa-labelledby="tfa_2364-L tfa_2365-L"><label class="label postField" id="tfa_2365-L" for="tfa_2365"><span class="input-radio-faux"></span>Mobile</label></span><span class="oneChoice"><input type="radio" value="tfa_2366" class="" id="tfa_2366" name="tfa_2364" aria-required="true" aria-labelledby="tfa_2366-L" data-tfa-labelledby="tfa_2364-L tfa_2366-L"><label class="label postField" id="tfa_2366-L" for="tfa_2366"><span class="input-radio-faux"></span>Home</label></span><span class="oneChoice"><input type="radio" value="tfa_2367" class="" id="tfa_2367" name="tfa_2364" aria-required="true" aria-labelledby="tfa_2367-L" data-tfa-labelledby="tfa_2364-L tfa_2367-L"><label class="label postField" id="tfa_2367-L" for="tfa_2367"><span class="input-radio-faux"></span>Work</label></span></span></div>
</div>
</div>
</div>
<div class="htmlSection" id="tfa_13"><div class="htmlContent" id="tfa_13-HTML">&nbsp;</div></div>
<div class="htmlSection" id="tfa_38"><div class="htmlContent" id="tfa_38-HTML">&nbsp;</div></div>
<div id="tfa_19" class="section group">
<label class="label preField" id="tfa_19-L"><b>Payment Details</b></label><br><div id="tfa_50" class="section inline group">
<div class="oneField field-container-D    " id="tfa_20-D">
<label id="tfa_20-L" class="label preField reqMark" for="tfa_20">Name on Card</label><br><div class="inputWrapper"><input aria-required="true" type="text" id="tfa_20" name="tfa_20" value="" title="Name on Card" class="required"></div>
</div>
<div class="oneField field-container-D    " id="tfa_21-D">
<label id="tfa_21-L" class="label preField reqMark" for="tfa_21">Card Number</label><br><div class="inputWrapper"><input aria-required="true" type="text" id="tfa_21" name="tfa_21" value="" autocomplete="off" placeholder="●●●●●●●●●●●●●●●●●●" title="Card Number" class="validate-custom /^\d+$/g required"></div>
</div>
</div>
<div id="tfa_49" class="section inline group">
<div class="oneField field-container-D    " id="tfa_23-D">
<label id="tfa_23-L" class="label preField reqMark" for="tfa_23">MM</label><br><div class="inputWrapper"><input aria-required="true" type="text" id="tfa_23" name="tfa_23" value="" placeholder="MM" min="1" max="12" title="MM" class="validate-integer required"></div>
</div>
<div class="oneField field-container-D    " id="tfa_24-D">
<label id="tfa_24-L" class="label preField reqMark" for="tfa_24">YY</label><br><div class="inputWrapper"><input aria-required="true" type="text" id="tfa_24" name="tfa_24" value="" placeholder="YY" max="9999" title="YY" class="validate-integer required"></div>
</div>
<div class="oneField field-container-D    " id="tfa_25-D">
<label id="tfa_25-L" class="label preField reqMark" for="tfa_25">CVC Code</label><br><div class="inputWrapper"><input aria-required="true" type="text" id="tfa_25" name="tfa_25" value="" autocomplete="off" placeholder="●●●" title="CVC Code" class="required"></div>
</div>
</div>
</div>
<div class="htmlSection" id="tfa_2228"><div class="htmlContent" id="tfa_2228-HTML">&nbsp;</div></div>
<div id="tfa_2218" class="section group">
<label class="label preField" id="tfa_2218-L"><b>Billing Address</b></label><div class="oneField field-container-D    " id="tfa_2222-D">
<label id="tfa_2222-L" class="label preField " for="tfa_2222">Street</label><br><div class="inputWrapper"><input type="text" id="tfa_2222" name="tfa_2222" value="" title="Street" class=""></div>
</div>
<div id="tfa_2229" class="section inline group">
<div class="oneField field-container-D    " id="tfa_2224-D">
<label id="tfa_2224-L" class="label preField " for="tfa_2224">City</label><br><div class="inputWrapper"><input type="text" id="tfa_2224" name="tfa_2224" value="" title="City" class=""></div>
</div>
<div class="oneField field-container-D    " id="tfa_2237-D">
<label id="tfa_2237-L" class="label preField " for="tfa_2237">State</label><br><div class="inputWrapper"><select id="tfa_2237" name="tfa_2237" title="State" class="calc-states"><option value="">Please select...</option>
<option value="tfa_2238" id="tfa_2238" class="calcval-AL">AL</option>
<option value="tfa_2239" id="tfa_2239" class="calcval-AK">AK</option>
<option value="tfa_2240" id="tfa_2240" class="calcval-AZ">AZ</option>
<option value="tfa_2241" id="tfa_2241" class="calcval-AR">AR</option>
<option value="tfa_2242" id="tfa_2242" data-conditionals="#tfa_2234" class="calcval-CA" selected data-default-value="true">CA</option>
<option value="tfa_2243" id="tfa_2243" class="calcval-CO">CO</option>
<option value="tfa_2244" id="tfa_2244" class="calcval-CT">CT</option>
<option value="tfa_2245" id="tfa_2245" class="calcval-DE">DE</option>
<option value="tfa_2246" id="tfa_2246" class="calcval-DC">DC</option>
<option value="tfa_2247" id="tfa_2247" class="calcval-FL">FL</option>
<option value="tfa_2248" id="tfa_2248" class="calcval-GA">GA</option>
<option value="tfa_2249" id="tfa_2249" class="calcval-HI">HI</option>
<option value="tfa_2250" id="tfa_2250" class="calcval-ID">ID</option>
<option value="tfa_2251" id="tfa_2251" class="calcval-IL">IL</option>
<option value="tfa_2252" id="tfa_2252" class="calcval-IN">IN</option>
<option value="tfa_2253" id="tfa_2253" class="calcval-IA">IA</option>
<option value="tfa_2254" id="tfa_2254" class="calcval-KS">KS</option>
<option value="tfa_2255" id="tfa_2255" class="calcval-KY">KY</option>
<option value="tfa_2256" id="tfa_2256" class="calcval-LA">LA</option>
<option value="tfa_2257" id="tfa_2257" class="calcval-ME">ME</option>
<option value="tfa_2258" id="tfa_2258" class="calcval-MD">MD</option>
<option value="tfa_2259" id="tfa_2259" class="calcval-MA">MA</option>
<option value="tfa_2260" id="tfa_2260" class="calcval-MI">MI</option>
<option value="tfa_2261" id="tfa_2261" class="calcval-MN">MN</option>
<option value="tfa_2262" id="tfa_2262" class="calcval-MS">MS</option>
<option value="tfa_2263" id="tfa_2263" class="calcval-MO">MO</option>
<option value="tfa_2264" id="tfa_2264" class="calcval-MT">MT</option>
<option value="tfa_2265" id="tfa_2265" class="calcval-NE">NE</option>
<option value="tfa_2266" id="tfa_2266" class="calcval-NV">NV</option>
<option value="tfa_2267" id="tfa_2267" class="calcval-NH">NH</option>
<option value="tfa_2268" id="tfa_2268" class="calcval-NJ">NJ</option>
<option value="tfa_2269" id="tfa_2269" class="calcval-NM">NM</option>
<option value="tfa_2270" id="tfa_2270" class="calcval-NY">NY</option>
<option value="tfa_2271" id="tfa_2271" class="calcval-NC">NC</option>
<option value="tfa_2272" id="tfa_2272" class="calcval-ND">ND</option>
<option value="tfa_2273" id="tfa_2273" class="calcval-OH">OH</option>
<option value="tfa_2274" id="tfa_2274" class="calcval-OK">OK</option>
<option value="tfa_2275" id="tfa_2275" class="calcval-OR">OR</option>
<option value="tfa_2276" id="tfa_2276" class="calcval-PA">PA</option>
<option value="tfa_2277" id="tfa_2277" class="calcval-RI">RI</option>
<option value="tfa_2278" id="tfa_2278" class="calcval-SC">SC</option>
<option value="tfa_2279" id="tfa_2279" class="calcval-SD">SD</option>
<option value="tfa_2280" id="tfa_2280" class="calcval-TN">TN</option>
<option value="tfa_2281" id="tfa_2281" class="calcval-TX">TX</option>
<option value="tfa_2282" id="tfa_2282" class="calcval-UT">UT</option>
<option value="tfa_2283" id="tfa_2283" class="calcval-VT">VT</option>
<option value="tfa_2284" id="tfa_2284" class="calcval-VA">VA</option>
<option value="tfa_2285" id="tfa_2285" class="calcval-WA">WA</option>
<option value="tfa_2286" id="tfa_2286" class="calcval-WV">WV</option>
<option value="tfa_2287" id="tfa_2287" class="calcval-WI">WI</option>
<option value="tfa_2288" id="tfa_2288" class="calcval-WY">WY</option></select></div>
</div>
</div>
<div id="tfa_2235" class="section inline group">
<div class="oneField field-container-D    " id="tfa_2226-D">
<label id="tfa_2226-L" class="label preField reqMark" for="tfa_2226">Zip Code</label><br><div class="inputWrapper"><input aria-required="true" type="text" id="tfa_2226" name="tfa_2226" value="" title="Zip Code" class="validate-integer required"></div>
</div>
<div class="oneField field-container-D    " id="tfa_2234-D">
<label id="tfa_2234-L" class="label preField reqMark" for="tfa_2234">County</label><br><div class="inputWrapper"><select aria-required="true" id="tfa_2234" name="tfa_2234" data-condition="`#tfa_2242`" title="County" class="required"><option value="">Please select...</option>
<option value="tfa_2296" id="tfa_2296" class="">Alameda</option>
<option value="tfa_2297" id="tfa_2297" class="">Alpine</option>
<option value="tfa_2298" id="tfa_2298" class="">Amador</option>
<option value="tfa_2299" id="tfa_2299" class="">Butte</option>
<option value="tfa_2300" id="tfa_2300" class="">Calaveras</option>
<option value="tfa_2301" id="tfa_2301" class="">Colusa</option>
<option value="tfa_2302" id="tfa_2302" class="">Contra Costa</option>
<option value="tfa_2303" id="tfa_2303" class="">Del Norte</option>
<option value="tfa_2304" id="tfa_2304" class="">El Dorado</option>
<option value="tfa_2305" id="tfa_2305" class="">Fresno</option>
<option value="tfa_2306" id="tfa_2306" class="">Glenn</option>
<option value="tfa_2307" id="tfa_2307" class="">Humboldt</option>
<option value="tfa_2308" id="tfa_2308" class="">Imperial</option>
<option value="tfa_2309" id="tfa_2309" class="">Inyo</option>
<option value="tfa_2310" id="tfa_2310" class="">Kern</option>
<option value="tfa_2311" id="tfa_2311" class="">Kings</option>
<option value="tfa_2312" id="tfa_2312" class="">Lake</option>
<option value="tfa_2313" id="tfa_2313" class="">Lassen</option>
<option value="tfa_2314" id="tfa_2314" class="">Los Angeles</option>
<option value="tfa_2315" id="tfa_2315" class="">Madera</option>
<option value="tfa_2316" id="tfa_2316" class="">Marin</option>
<option value="tfa_2317" id="tfa_2317" class="">Mariposa</option>
<option value="tfa_2318" id="tfa_2318" class="">Mendocino</option>
<option value="tfa_2319" id="tfa_2319" class="">Merced</option>
<option value="tfa_2320" id="tfa_2320" class="">Modoc</option>
<option value="tfa_2321" id="tfa_2321" class="">Mono</option>
<option value="tfa_2322" id="tfa_2322" class="">Monterey</option>
<option value="tfa_2323" id="tfa_2323" class="">Napa</option>
<option value="tfa_2324" id="tfa_2324" class="">Nevada</option>
<option value="tfa_2325" id="tfa_2325" class="">Orange</option>
<option value="tfa_2326" id="tfa_2326" class="">Placer</option>
<option value="tfa_2327" id="tfa_2327" class="">Plumas</option>
<option value="tfa_2328" id="tfa_2328" class="">Riverside</option>
<option value="tfa_2329" id="tfa_2329" class="">Sacramento</option>
<option value="tfa_2330" id="tfa_2330" class="">San Benito</option>
<option value="tfa_2331" id="tfa_2331" class="">San Bernardino</option>
<option value="tfa_2332" id="tfa_2332" class="">San Diego</option>
<option value="tfa_2333" id="tfa_2333" class="">San Francisco</option>
<option value="tfa_2334" id="tfa_2334" class="">San Joaquin</option>
<option value="tfa_2335" id="tfa_2335" class="">San Luis Obispo</option>
<option value="tfa_2336" id="tfa_2336" class="">San Mateo</option>
<option value="tfa_2337" id="tfa_2337" class="">Santa Barbara</option>
<option value="tfa_2338" id="tfa_2338" class="">Santa Clara</option>
<option value="tfa_2339" id="tfa_2339" class="">Santa Cruz</option>
<option value="tfa_2340" id="tfa_2340" class="">Shasta</option>
<option value="tfa_2341" id="tfa_2341" class="">Sierra</option>
<option value="tfa_2342" id="tfa_2342" class="">Siskiyou</option>
<option value="tfa_2343" id="tfa_2343" class="">Solano</option>
<option value="tfa_2344" id="tfa_2344" class="">Sonoma</option>
<option value="tfa_2345" id="tfa_2345" class="">Stanislaus</option>
<option value="tfa_2346" id="tfa_2346" class="">Sutter</option>
<option value="tfa_2347" id="tfa_2347" class="">Tehama</option>
<option value="tfa_2348" id="tfa_2348" class="">Trinity</option>
<option value="tfa_2349" id="tfa_2349" class="">Tulare</option>
<option value="tfa_2350" id="tfa_2350" class="">Tuolumne</option>
<option value="tfa_2351" id="tfa_2351" class="">Ventura</option>
<option value="tfa_2371" id="tfa_2371" class="">Yolo</option>
<option value="tfa_2372" id="tfa_2372" class="">Yuba</option>
<option value="tfa_2373" id="tfa_2373" class="">Out of State</option></select></div>
</div>
</div>
</div>
<div class="htmlSection" id="tfa_15"><div class="htmlContent" id="tfa_15-HTML">&nbsp;</div></div>
<div class="oneField field-container-D  labelsAbove  " id="tfa_2368-D" role="group" aria-labelledby="tfa_2368-L" data-tfa-labelledby="-L tfa_2368-L" aria-required="true">
<label id="tfa_2368-L" class="label preField reqMark" aria-label="Privacy Notice and Terms of Service   required">Privacy Notice and Terms of Service</label><br><div class="inputWrapper"><span id="tfa_2368" class="choices vertical required" aria-required="true"><span class="oneChoice"><input type="checkbox" value="tfa_2369" class="" id="tfa_2369" name="tfa_2369" aria-labelledby="tfa_2369-L" data-tfa-labelledby="tfa_2368-L tfa_2369-L"><label class="label postField" id="tfa_2369-L" for="tfa_2369"><span class="input-checkbox-faux"></span><span id="tfa_2368" class="choices vertical required ui-sortable"><span class="oneChoice">Check here&nbsp;<span id="tfa_2368" class="choices  required ui-sortable"><span class="oneChoice"> to state that you have read and agree to our <a href="http://www.californiafarmlink.org/privacy-policy/">Privacy Notice</a>,&nbsp;</span></span></span><a style="white-space: nowrap;" target="_blank" href="https://www.californiafarmlink.org/client-code-of-conduct/">Client Code of Conduct&nbsp;<span style="caret-color: initial; color: rgb(0, 0, 0); word-spacing: normal; -webkit-text-decorations-in-effect: initial; -webkit-text-fill-color: initial; -webkit-text-stroke-color: initial; -webkit-text-stroke-width: initial; text-decoration: none;">and </span></a><a style="word-spacing: normal; -webkit-text-decorations-in-effect: initial; -webkit-text-fill-color: initial; -webkit-text-stroke-color: initial; -webkit-text-stroke-width: initial;" href="http://www.californiafarmlink.org/terms-of-service/">Terms of Service</a><span style="caret-color: initial; color: rgb(0, 0, 0); word-spacing: normal; -webkit-text-decorations-in-effect: initial; -webkit-text-fill-color: initial; -webkit-text-stroke-color: initial; -webkit-text-stroke-width: initial; text-decoration: none;">.</span><br></span></label></span></span></div>
</div>
<input type="hidden" id="tfa_2236" name="tfa_2236" value="" class='formula=Amount=="Other"?OtherAmount:Amount'><input type="hidden" id="tfa_2352" name="tfa_2352" value="" class=""><input type="hidden" id="STRIPE_CUSTOMER_254258" name="STRIPE_CUSTOMER_254258" value="" class=""><input type="hidden" id="STRIPE_SUBSCR_254258" name="STRIPE_SUBSCR_254258" value="" class=""><input type="hidden" id="STRIPE_CHARGE_254258" name="STRIPE_CHARGE_254258" value="" class=""><input type="hidden" id="STRIPE_CUSTOMER_403423" name="STRIPE_CUSTOMER_403423" value="" class=""><input type="hidden" id="STRIPE_SUBSCR_403423" name="STRIPE_SUBSCR_403423" value="" class=""><input type="hidden" id="STRIPE_CHARGE_403423" name="STRIPE_CHARGE_403423" value="" class=""><input type="hidden" id="STRIPE_CUSTOMER_427234" name="STRIPE_CUSTOMER_427234" value="" class=""><input type="hidden" id="STRIPE_SUBSCR_427234" name="STRIPE_SUBSCR_427234" value="" class=""><input type="hidden" id="STRIPE_CHARGE_427234" name="STRIPE_CHARGE_427234" value="" class=""><div class="actions" id="4846959-A"><input type="submit" data-label="Renew Membership" class="primaryAction" id="submit_button" value="Renew Membership"></div>
<div style="clear:both"></div>
<input type="hidden" value="4846959" name="tfa_dbFormId" id="tfa_dbFormId"><input type="hidden" value="" name="tfa_dbResponseId" id="tfa_dbResponseId"><input type="hidden" value="31b96271fbd1c4b1d1943e8f0699e402" name="tfa_dbControl" id="tfa_dbControl"><input type="hidden" value="" name="tfa_dbWorkflowSessionUuid" id="tfa_dbWorkflowSessionUuid"><input type="hidden" value="3" name="tfa_dbVersionId" id="tfa_dbVersionId"><input type="hidden" value="" name="tfa_switchedoff" id="tfa_switchedoff">
</form>
</div></div><div class="wFormFooter"><p class="supportInfo"><a target="new" class="contactInfoLink" href="https://www.tfaforms.com/forms/help/4678004" data-testid="contact-info-link">Contact Information</a><br></p></div>
  <p class="supportInfo" >
      </p>
 </div>

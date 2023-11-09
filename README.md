# reCaptcha v3 Human-like Score Solver

This solver is designed to provide reCaptcha v3 solutions with human-equivalent scores ranging from 0.7 to 0.9.

## Important Instructions

Ensure the accuracy of **pageAction** and **websiteURL** for optimal results.

## Obtaining Correct Parameters

The Capsolver extension is essential for acquiring the necessary values.

### Step-by-Step Guide:

1. **Extension Installation**:
   - Add the [Captcha Solver Auto Bypass](https://chrome.google.com/webstore/detail/captcha-solver-auto-bypas/pgojnojmmhpofjgdmaebadhbocahppod) to your Chrome browser.

2. **Configuring Capsolver**:
   - Access [Capsolver](https://www.capsolver.com/).
   - Launch the browser's developer tools by pressing "F12".
   - Find the **Capsolver Captcha Detector** tab within the tools.
     ![Capsolver Detector Panel](https://assets.capsolver.com/prod/images/post/2023-10-31/2115f05d-a7eb-40b6-9693-53baa45d39a9.png)

3. **Trigger and Detect**:
   - Keep the Capsolver panel open and navigate to the target website to initiate the CAPTCHA challenge.
   - Activate the CAPTCHA without closing the Capsolver panel.

The following details will be displayed:
![Captured reCaptcha Data](https://assets.capsolver.com/prod/images/post/2023-10-31/57a3dfd6-5048-4772-9e6c-9956f9acc916.png)

Transfer the JSON data provided by Capsolver into your configuration without alteration, except for the task type, which should be changed from `ReCaptchaV3TaskProxyless` or `ReCaptchaV3TaskEnterpriseProxyless` to `ReCaptchaV3M1TaskProxyLess`.

The final configuration JSON should appear as follows:

```json
{
    "clientKey": "YOUR_API_KEY",
    "task": {
        "type": "ReCaptchaV3M1TaskProxyLess",
        "websiteURL": "https://example.com",
        "websiteKey": "6LdyC2cUAAAAACGuDKpXeDorzUDWXmdqeg-xy696",
        "anchor": "specified_value",
        "reload": "specified_value",
        "pageAction": "specified_example_action"
    }
}
```

In this JSON structure, replace placeholder data such as `anchor`, `reload`, `pageAction`, `websiteURL`, and `websiteKey` with the actual values returned by the Capsolver extension for accurate task execution.

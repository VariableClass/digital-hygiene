# Securing Your Accounts

Now comes the tedious part. Having laid the foundations for a more secure future, it's time to wade through your existing accounts. For each account in your password manager, follow the steps laid out below. Remember that this is a marathon, not a sprint. It typically takes several weeks to get through all your accounts but this is mercifully a one-time process.

Try to set a goal of doing all of the accounts under a letter of the alphabet each time you sit down to attack it, or getting through 10 accounts a day or whatever you find achievable. The most important thing is to keep going; better that it take 6 months but you get through the list than getting 10% of the way through and giving up.

## Contents

- [Delete the account if you no longer need it](#1-delete-the-account-if-you-no-longer-need-it)
- [Change your password](#2-change-your-password)
- [Enable MFA](#3-enable-mfa)
- [Improve your privacy settings](#4-improve-your-privacy-settings)
- [Use an e-mail alias](#5-use-an-e-mail-alias)
- [Migrate away from "Sign in with..."](#6-migrate-away-from-sign-in-with)
- [Update payment information](#7-update-payment-information)
- [Update address information](#8-update-address-information)

## 1. Delete the account if you no longer need it

Decide whether you really need the account any more.

Even if you think you may use the service again, ask yourself whether you specifically need *this* account - could you just create a new account were you to use the service again or do you need the data that is against specifically this account (e.g. order history/receipts)?

If you feel you can get rid of the account, you can try to delete it. You can do this by either:

- Logging into the account and trying to find a button specifically using the word **Delete**. Do not be fooled by *Close* or *Deactivate*. These are NOT equivalent. In some rare cases, they may perform the same function, but better safe than sorry. If you are unable to locate this button, it's over to the alternative.

- Following link to the company's **Privacy Policy**. This can typically be found at the bottom of their homepage. In the privacy policy, find the section that applies to the GDPR "Right to be forgotten"/"Right to deletion"/similar. Here you will find either a link to a web form you can fill out specifically requesting a GDPR deletion or, more likely, an privacy-specific e-mail address you can send a request to. This typically looks something like dpo@company.com, privacy@company.com or gdpr@company.com. Some companies simply use their customer service e-mail address. You can then proceed to send the following e-mail;

  ```markdown
    To: privacy@company.com
    Subject: GDPR Deletion Request

    Please delete my account and all associated personal information in accordance with GDPR.
  ```

In either case, if the account was not immediately deleted, mark the account as having **requested deletion** in your password manager, either by renaming it (eg. `onlineshop.com` -> `REQUESTED DELETION: someonlineshop.com`, moving it to a folder dedicated to items pending deletion or adding a custom field; `Requested deletion: [x]`

## 2. Change your password

One of the major benefits to having a password manager is that you no longer need to remember passwords yourself. This means that you no longer have to reuse the 1, 5 or even 10 passwords you rotate on various websites, but instead can use a unique password for every account you have. This greatly reduces the impact were one of these accounts to be compromised since the password is not reused on any other sites.

> NB. Using e-mail aliases is a way to amplify this effect, since not only would each account have a unique password, but also a unique e-mail address, rendering this information practically useless to bad actors.

Moreover, these unique passwords will be far more resilient to brute-force attacks, since you can make them as long & complicated as your password manager allows.

Set up your password manager's default password generation to:

- Be as many characters as possible
- Use both capital and lower case letters
- Use numbers
- Use symbols
- Use similar characters

This will result in passwords that look something like this:

`YjXysQzJukRn9hTwtyz8u%tcgydRSkh^N5eSaB$>Q6SQvfu+rqKxa3x(Buh$b*!e`

You may need to adjust these settings down for websites that may not use best practices when it comes to passwords (e.g. Only accepting passwords up to 20 characters and no special characters), but it's best to do this on a case-by-case basis, rather than having it be the default.

Log in to the account and navigate to the change password. Some websites may instead require you to follow the *Forgot password* link on the login page. You can now use your password manager to generate a new password to replace the one associated with the account. Make sure you are prompted to update the password for this account.

## 3. Enable MFA

Multifactor Authentication (MFA) is one of the best measures you can take to secure your online accounts, as it introduces the need for a second piece of login information to be able to log in. It is worth noting that not all multifactor authentication is created equal;

- **S tier**: Hardware security keys (e.g. Yubikey)
- **A tier**: Time-based One Time Passwords (TOTP)
- **B tier**: Trusted device confirmation (e.g. app/web notification)
- **C tier**: E-mail confirmation (e.g. e-mailed code/"magic" link)
- **D tier**: SMS codes

Enable the highest option on this list available to you. This will often mean scanning a QR-code with your TOTP app and entering the code it generates.

### Backup Codes

Often, you will subsequently be presented with a list of backup codes. It's very important to hold on to these codes/an alternative backup MFA since, if you lose your phone or Yubikey then you'll need an alternative way to get in to your account.

These codes can be saved to your password manager as a custom field on the account or as a separate note called something like `SomeOnlineShop | 2FA Backup Codes`. If you are not presented with these codes, they are typically available as an individual security option you can set up in your account's security settings.

## 4. Improve your privacy settings

Since you are now anyway logged in to the account, this is an ideal time to go through the various security & privacy settings and make sure everything looks good. I found myself typically turning off/opting out of multiple privacy settings. Often these settings were not limited to the **Privacy** section of the menu, either, but tucked away in some other menu. For example, what elements of your profile are visible to the public on LinkedIn. This is also an ideal opportunity to unsubscribe from unwanted e-mail/SMS newsletters.

Facebook is one of the worst offenders here. Multiple UIs, disjointed menus and sneaky hidden settings mean that you should be prepared for a fight, but the best thing is to just delete your Facebook account if you can.

## 5. Use an e-mail alias

Use your e-mail aliasing service to generate a new alias for the current account.

Ideally, include a randomly-generated suffix such that your e-mail addresses can't simply be guessed by using the company name and your domain. This also makes your aliases easier to regenerate should the need arise. For example: **facebook.2j49f@example.com**.

Using an alias like this, especially in combination with a service like [have i been pwned?](https://haveibeenpwned.com), means that you will be able to directly pinpoint who is guilty in selling or leaking your information. You may even know about a leak before they do!

### Randomly generated username

It's a good idea to use a unique, randomly generated username for each account, this will make it more difficult to associate your information across the web. Bitwarden includes a username generator, but you can just as easily pick a random dictionary word and append a random number. Make sure you save this in your password manager, along with the e-mail and password you use to sign in to the account.

## 6. Migrate away from "Sign in with..."

As with almost this entire guide, this is down to personal choice, but in my view; with unique passwords/e-mail addresses, the benefit of using a third party identity provider is somewhat moot.

Whilst you are entrusting credentials to the service you sign into when using a traditional e-mail/password combination, since both your e-mail address and password are now entirely unique to each individual service, the damage is isolated were one of these services to be compromised. It also means that, were your Google/Apple/Microsoft account to be compromised, the hacker would not gain access to any services you sign into using this account.

Always signing in with a unique e-mail address can help maintain a clear picture of what you have signed up for, as well as a fine-grained control over account access.

Look for settings referring to *Social Connections*/*Social Login*/similar. Here you should simply be able to select **Unlink** to remove the connection with the identity provider.

## 7. Update payment information

Saving your credit card information on various sites puts it at risk of being leaked. Wherever possible, use a service such as Apple Pay or Vipps to abstract your payment information away from the site you are buying something from. Virtual credit cards from sites like [privacy.com](https://privacy.com) are currently only available in the US, but Apple Pay/Vipps perform an analagous, if not **more** secure, function - providing one-time use payment details at checkout.

Remove any saved credit card information from the account if possible.

## 8. Update address information

On sites you regularly use and have secured, it can be a good idea to ensure that your address information is up-to-date, so that things get delivered to your current address.

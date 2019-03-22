---
title: password-standard
---

<b>This guidance applies to everyone who works for the MOJ, or who supply systems or services to the MOJ.</b>

[acs]: https://intranet.justice.gov.uk/guidance/security/it-computer-security/ict-security-policy-framework/moj-enterprise-access-control-policy/
[gcs]: https://intranet.justice.gov.uk/guidance/security/it-computer-security/government-classification-scheme/
[cyberawarepasswords]: https://www.cyberaware.gov.uk/passwords
[govukpasswords]: https://www.cyberaware.gov.uk/passwords
[hmgias2]: https://www.ncsc.gov.uk/guidance/information-risk-management-hmg-ia-standard-numbers-1-2
[ncsccertificates]: https://www.ncsc.gov.uk/guidance/provisioning-and-securing-security-certificates
[ncscmfa]: https://www.ncsc.gov.uk/guidance/multi-factor-authentication-online-services
[ncscpasswordguidance]: https://www.ncsc.gov.uk/guidance/using-passwords-protect-your-data
[ncscpasswordguidancesimplify]: https://www.ncsc.gov.uk/guidance/password-guidance-simplifying-your-approach
[pg]: https://intranet.justice.gov.uk/guidance/security/it-computer-security/ict-security-policy-framework/password-guidance/
[sa]: https://intranet.justice.gov.uk/guidance/security/it-computer-security/ict-security-policy-framework/system-administrators/
[smdp]: https://www.gov.uk/service-manual/design/passwords
[tcp]: https://intranet.justice.gov.uk/guidance/security/it-computer-security/ict-security-policy-framework/technical-controls-policy/
[uas]: https://www.ncsc.gov.uk/content/files/guidance_files/IG%203%20-%20User%20Authentication%20Systems%20-%20issue%201.1%20Oct%2015%20-%20NCSC%20Web.pdf
<!--
[hmgspf]: https://www.gov.uk/government/publications/security-policy-framework
[suas]: https://intranet.justice.gov.uk/guidance/security/it-computer-security/ict-security-policy-framework/system-users-and-application-administrators/
-->

## About this document

This document is the MOJ IT Security - Password Standard. It helps you protect MOJ IT systems by telling you about choosing and using passwords. Whenever you see the word 'system' here, it applies to:

- hardware, such as laptops, PCs, servers, mobile devices, and any ICT equipment
- software, such as the OS, or applications installed on hardware, or mobile device apps
- services, such as remote databases or cloud-based tools like [Slack](https://slack.com/)

You can see the formal [User Password Management](https://intranet.justice.gov.uk/guidance/security/it-computer-security/ict-security-policy-framework/technical-controls-policy/#user-password-management) rules in the [IT Security - Technical Controls Policy][tcp].

This document has guidance on passwords for [all users](#all-users). It also includes more detail for [system administrators or developers](#system-administrators-or-developers).

<a id="all-users"></a>

## All users

The MOJ password guidance uses [NCSC guidance][ncscpasswordguidance]. It recommends a [simpler][ncscpasswordguidancesimplify] approach to passwords. Some agencies or bodies might have specific requirements or variations. Check your team Intranet or ask your Line Manager for more information.

Follow the [CyberAware advice][cyberawarepasswords] to generate your passwords. Always use a separate and unique password for each account or service.

Make sure you read the MOJ [guidance][pg] information about passwords. The most important points are that passwords should be:

- at least 8 characters long
- no more than 128 characters long
- not obvious
- not a dictionary word. A combination of dictionary words might be suitable, such as '`CorrectHorseBatteryStaple`'
- unique for each account or service

If a system or another person provides you with a password, change it before doing any MOJ work on that system. Examples of 'single-use' passwords include:

- your own account on a work-provided laptop
- a shared account for accessing a data analytics service
- all supplier or vendor supplied accounts

You must change a password whenever:

- there has been a security incident involving your account or password. For example, someone guessed your password, or you used it on another account
- there was a security incident with the service that you access using the password. For example, if someone broke into the system that provides the service you use
- your line manager or other authorised person tells you to do so

When required to change a password, you must do so as soon as possible. If you don't change the password soon enough, you might be locked out of your account automatically. The following table shows the maximum time allowed:

| Type of system | Maximum time to change a password |
|---|---|
| Single-user systems, such as laptops | 1 week |
| All other systems | 1 day |

<a id="password-expiry"></a>

You don't have to change a password because it is old. The reason is that time-expiry of passwords is an "[...outdated and ineffective practice](https://www.ncsc.gov.uk/blog-post/your-password-expiry-policy-may-have-reached-its-expiry-date)".

Some current or legacy systems don't allow passwords that follow MOJ [guidance][pg]. For example, some mobile devices, laptop hard drive encryption tools, or older computers might not be able to support a mix of character types. For such systems, choose passwords that are as close as possible to MOJ [guidance][pg].

<!--

Use a [password manager](#password-managers) to help you keep track of your passwords.

<a id="password-managers"></a>

### Password managers

[ncschelpingendusers]: https://www.ncsc.gov.uk/guidance/helping-end-users-manage-their-passwords
[ncscpwm]: https://www.ncsc.gov.uk/blog-post/what-does-ncsc-think-password-managers

These are tools that help you create, use, and manage your passwords. A useful overview is available [here][ncscpwm].

As passwords become more complex, and you need to look after more of them, it becomes increasingly necessary to use a password manager. For example, development teams in MOJ Digital &amp; Technology use `RatticDB`. Other popular password managers include [`LastPass`](https://lastpass.com/) and [`1Password`](https://1password.com/).

You still need to remember one password. This is the password that gets you into the manager application. Once you have access, the application works like a simple database, storing all the passwords associated with your various accounts and services. Some managers have extra features, such as password generators. Some managers can even automatically fill-in username and password fields for you when during log in.

The password manager database is often stored in the cloud so that you can use it anywhere. The database is encrypted, so only you can open it. That's why your single password key is so important. Without it, you can never get access to the password database again.

Using a password manager for your MOJ account and service details is recommended. Ask your Line Manager for permission to install one of the applications listed in this doc

Extra guidance for system administrators or developers is available [here][ncschelpingendusers].

-->

<a id="system-administrators-or-developers"></a>

## System administrators or developers

Follow the [Government Service Manual for Passwords][smdp] when you administer or develop MOJ systems or services.

Suppliers and vendors must ensure that systems support the password requirements. Systems must be able to issue, change, reset, and revoke passwords. This must be possible using well-defined and fully-described processes. Supply enough information and procedures to fulfil MOJ password policy.

The [NCSC guidance][ncscpasswordguidancesimplify] for simplifying passwords says that forcing complex passwords has:

- marginal security benefit
- a high user burden

Technical controls are more effective at protecting password-based authentication. Examples include:

- [locking accounts](#password-access-attempts) after repeated access attempts
- [blocking](#blocking-bad-passwords) common password choices

<a id="user-facing-services"></a>

### User facing services

Authenticate people accessing user facing services by using the [GOV.UK Verify](https://www.gov.uk/government/publications/introducing-govuk-verify/introducing-govuk-verify) service. It is not necessary for someone to be a UK Citizen to use the GOV.UK Verify service, but they must have a UK address.

If it is not possible to use GOV.UK Verify, follow the advice in this standard to support citizen passwords. Pay extra attention to the following points:

- people should have complex passwords which are different for each service they use. Make it easy for people to have complex passwords by supporting password managers. For example, services should always let users paste passwords into web forms
- don't force [regular password expiry](#password-expiry). Make it easy to [change passwords](#password-reset) when required
- force password changes when required. For example, after [exceeding a count of unsuccessful password entry attempts](#password-access-attempts)
- make the process of [resetting a password](#password-reset) like providing a password for the first time. Include a way to [prevent attackers using the reset process](#distributing-passwords-to-users) to conduct an attack

<a id="service-accounts"></a>

### Service Accounts

System and application authentication must always use service accounts . Use certificates for service account authentication. Follow [NCSC guidelines][ncsccertificates] for issuing and securing the certificates. If you can't use certificates, passwords are an acceptable alternative.

Service account passwords must:

- be system generated
- be at least 15 characters long
- be no more than 128 characters long
- be complex, including upper-case and lower-case letters, digits, punctuation, and special characters
- be kept secure, by using hashes or encryption
- not be stored in the clear in any systems or applications
- not be used by standard or administrative users for any purpose

### Default passwords

Change all default passwords when a new, modified, or replacement system arrives. Complete the changes before making the system available for any MOJ work.

### Multi-factor Authentication (MFA)

[Multi-factor Authentication (MFA)](https://en.wikipedia.org/wiki/Multi-factor_authentication) provides extra security for login and access controls. MFA is also referred to as Two-Factor Authentication or 2FA.

Use MFA in systems for privileged or important step confirmation. For example, the user must enter their MFA code when deleting a record.

Follow the [NCSC guidance][ncscmfa] for enabling MFA.

Use [Time-based One-Time Password Algorithm (TOTP)](https://en.wikipedia.org/wiki/Time-based_One-time_Password_algorithm) or hardware and software tokens. If possible, avoid using SMS or email messages containing one-time login codes. If TOTP applications, or hardware- or software-based tokens, are not available to you, then SMS MFA or email MFA is still better than no MFA.

Systems must offer MFA alternatives to users where they are available. For example, MFA codes sent by SMS are not suitable if mobile devices are not allowed in the room or building.

### Extra measures

Check that a system, service, or information protected by a password is not [classified][gcs] as `SECRET` or `TOP SECRET`. Make sure that it doesn't contain delicate material. Examples include contracts, or personal data or information. If it does contain such material, you might need extra access control.

Check which other systems have access to the system or service. Make sure that the access control suits the material at both ends of the connection.

Appropriate extra measures might include tokens or other multi-factor authentication devices. Think about using an existing authentication system other than passwords. Avoid creating new authentication systems. Try to reduce what a user must remember. For more information about authentication, see the [IT Security - Access Control Standard][acs].

A technical risk assessment helps identifies extra controls for systems. This is mandatory for systems that need formal accreditation. Multi-user systems are also subject to a Business Impact Assessment (BIA).

For example, an assessment might find that you need extra checks for logging in to an account or service. The checks might depend on various factors such as:

- time of login
- location of login
- number of previous connections from the connecting IP address
- whether to allow more than one login at a time

Examples of these extra mechanisms include:

- biometrics
- tokens
- certificate-based authentication

### Password storage

Never store, display or print passwords [in the clear](https://en.wikipedia.org/wiki/Plaintext). If you must store them, do so by using [salt](https://www.owasp.org/index.php/Password_Storage_Cheat_Sheet#Use_a_cryptographically_strong_credential-specific_salt)ed [hash](https://en.wikipedia.org/wiki/Hash_function)es.

Suitable storage tools include:

- [Argon2](https://en.wikipedia.org/wiki/Argon2)
- [bcrypt](https://en.wikipedia.org/wiki/Bcrypt)
- [PBKDF2](https://en.wikipedia.org/wiki/PBKDF2)
- [scrypt](https://en.wikipedia.org/wiki/Scrypt)

Make sure the password storage security matches the system or data [classification][gcs]. Contact the Security Engineering or Information Assurance team for help determining suitable security.

Ensure the password storage security matches the [classification][gcs] of the system or data. For help with the appropriate strength of hashing, contact:

- [information assurance](https://intranet.justice.gov.uk/guidance/knowledge-information/protecting-information/information-assurance-roles/)
- security engineering

Extra information on handling and protecting passwords is in the [IT Security SyOPs - System Administrators][sa] guide.

<a id="password-access-attempts"></a>

### Password access attempts

If a password is ever entered incorrectly, a count should start. After at most 10 (ten) consecutive failed attempts at using the correct password, lock the account or system access. A successful use of the password resets the count to zero again.

<a id="password-reset"></a>

If a password lock occurs, a reset is necessary. This requires action by the system administrator or MOJ Service Desk. The process should be like issuing the password for the first time. Other account details are not changed during the reset. This helps avoid losing any work. Checks ensure that an attacker cannot use the password reset process.

<a id="blocking-passwords"></a>
<a id="blocking-bad-passwords"></a>

### Blocking bad passwords

Don't let users choose [obvious passwords](https://en.wikipedia.org/wiki/List_of_the_most_common_passwords). Check for and block obvious passwords embedded within a password. For example, `MySecretPassword` is not a good password!

Use password and hash lists from [SecLists](https://github.com/danielmiessler/SecLists/tree/master/Passwords) or [Have I Been Pwned](https://haveibeenpwned.com/Passwords), to help prevent bad passwords.

<a id="distributing-passwords-to-users"></a>

### Distributing passwords to users

There are times when a system must send a password to a user. An example is when granting access to a service for the first time. To send a password to a user, the mechanism used must be secure. The protection should match the sensitivity of the information protected by password.

Passwords created for a user should always be [single-use](#single-use-passwords). Use an out-of-band channel to send the password to the user. For example, send the password to the user's line manager who will give it to the user.

<a id="single-use-passwords"></a>

### Single-use passwords

Some passwords are 'one time' or single-use. Administrators and developers use these to grant access to a service for the first time. After using the password once, the user must immediately change the password.

Single-use passwords are time limited. If they are not used within a specific time after generation, they must become invalid.

The following table shows the valid lifetime of a single-use password:

| Type of system | Lifetime of a single-use password |
|---|---|
| Single-user systems, such as laptops | 1 week |
| All other systems | 1 day |

### Multi-user systems and services

All multi-user systems and services must check for redundant User IDs and accounts. If necessary, remove the redundant IDs or accounts. The [IT Security - Access Control Standard][acs] discusses the management and removal of accounts. If someone is no longer allowed to access a system, check for and change any shared account or common password they might still have.

### Identity Providers and Single Sign-On

When you need an authentication solution, try to use existing MOJ services. Examples include Identity Provider (IdP) or Single Sign-On (SSO) services, such as Office 365 or Digital and Technology G-Suite.

This helps reduce the need to design, create, deploy and manage yet another solution.

SSO integration in existing IdP solutions improves the user experience. This is because you can authenticate to systems using existing MOJ credentials.

<a id="account-management"></a>

### Account management

The guidance on passwords is separate from guidance on account management. You should still follow the rules and processes for managing accounts. In particular, while you don't need to [change passwords after a period of time](#password-expiry), you should still expire accounts promptly. Examples would be when accounts are no longer required, or have fallen out of use.

---

<table>
<tr><td colspan='4'>This guidance is dated October 2018.
<p>
To provide feedback on this document, please contact us: <a href="mailto:itpolicycontent+password-standard@digital.justice.gov.uk?subject=password-standard">itpolicycontent@digital.justice.gov.uk</a>, or click one of the following icons.</p></td></tr>
<tr>
<td width='25%'><a href="mailto:itpolicycontent+password-standard-2@digital.justice.gov.uk?subject=password-standard-2"><img src="https://s3-eu-west-2.amazonaws.com/intranet-prod-storage-1dvcquh7kophi/uploads/2018/04/DoubleCross.gif" alt="Content was very unhelpful">Very unhelpful.</a></td>
<td width='25%'><a href="mailto:itpolicycontent+password-standard-1@digital.justice.gov.uk?subject=password-standard-1"><img src="https://s3-eu-west-2.amazonaws.com/intranet-prod-storage-1dvcquh7kophi/uploads/2018/04/Cross.gif" alt="Content was unhelpful">Unhelpful.</a></td>
<td width='25%'><a href="mailto:itpolicycontent+password-standard+1@digital.justice.gov.uk?subject=password-standard+1"><img src="https://s3-eu-west-2.amazonaws.com/intranet-prod-storage-1dvcquh7kophi/uploads/2018/04/Tick.gif" alt="Content was helpful">Helpful.</a></td>
<td width='25%'><a href="mailto:itpolicycontent+password-standard+2@digital.justice.gov.uk?subject=password-standard+2"><img src="https://s3-eu-west-2.amazonaws.com/intranet-prod-storage-1dvcquh7kophi/uploads/2018/04/DoubleTick.gif" alt="Content was very helpful">Very helpful.</a></td>
</table>

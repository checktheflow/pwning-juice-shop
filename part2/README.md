# Part II - Challenge hunting

This part of the book can be read from end to end as a _hacking guide_.
Used in that way you will be walked through various types of web
vulnerabilities and learn how to exploit their occurrences in the Juice
Shop application. Alternatively you can start hacking the Juice Shop on
your own and use this part simply as a reference and _source of hints_
in case you get stuck at a particular challenge.

In case you want to look up hints for a particular challenge, the
following tables lists all challenges of the OWASP Juice Shop grouped by
their difficulty and in the same order as thery appear on the Score
Board.

_The challenge hints found in this release of the companion guide are
compatible with `{{book.juiceShopVersion}}` of OWASP Juice Shop._

### Trivial Challenges (  :star:  )

| Challenge            | Description                                                            | Hints                                                                                               |
|:---------------------|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| Admin Section        | Access the administration section of the store.                        | [  :bulb:  ](broken-access-control.md#access-the-administration-section-of-the-store)               |
| Confidental Document | Access a confidential document.                                        | [  :bulb:  ](sensitive-data-exposure.md#access-a-confidential-document)                             |
| Error Handling       | Provoke an error that is not very gracefully handled.                  | [  :bulb:  ](security-misconfiguration.md#provoke-an-error-that-is-not-very-gracefully-handled)     |
| Redirects Tier 1     | Let us redirect you to a donation site that went out of business.      | [  :bulb:  ](forgotten-content.md#let-us-redirect-you-to-a-donation-site-that-went-out-of-business) |
| Score Board          | Find the carefully hidden 'Score Board' page.                          | [  :bulb:  ](score-board.md#find-the-carefully-hidden-score-board-page)                             |
| XSS Tier 0           | Perform a _reflected_ XSS attack with `<script>alert("XSS")</script>`. | [  :bulb:  ](xss.md#perform-a-reflected-xss-attack)                                                 |
| XSS Tier 1           | Perform a _DOM_ XSS attack with `<script>alert("XSS")</script>`.       | [  :bulb:  ](xss.md#perform-a-dom-xss-attack)                                                       |
| Zero Stars           | Give a devastating zero-star feedback to the store.                    | [  :bulb:  ](improper-input-validation.md#give-a-devastating-zero-star-feedback-to-the-store)       |

### Easy Challenges (  :star::star:  )

| Challenge            | Description                                                                                                  | Hints                                                                                                                                             |
|:---------------------|:-------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| Basket Access        | Access someone else's basket.                                                                                | [  :bulb:  ](broken-access-control.md#access-someone-elses-basket)                                                                                |
| Christmas Special    | Order the Christmas special offer of 2014.                                                                   | [  :bulb:  ](injection.md#order-the-christmas-special-offer-of-2014)                                                                              |
| Deprecated Interface | Use a deprecated B2B interface that was not properly shut down.                                              | [  :bulb:  ](forgotten-content.md#use-a-deprecated-b2b-interface-that-was-not-properly-shut-down)                                                 |
| Five-Star Feedback   | Get rid of all 5-star customer feedback.                                                                     | [  :bulb:  ](broken-access-control.md#get-rid-of-all-5-star-customer-feedback)                                                                    |
| Login Admin          | Log in with the administrator's user account.                                                                | [  :bulb:  ](injection.md#log-in-with-the-administrators-user-account)                                                                            |
| Login MC SafeSearch  | Log in with MC SafeSearch's original user credentials without applying SQL Injection or any other bypass.    | [  :bulb:  ](sensitive-data-exposure.md#log-in-with-mc-safesearchs-original-user-credentials)                                                     |
| Password Strength    | Log in with the administrator's user credentials without previously changing them or applying SQL Injection. | [  :bulb:  ](broken-authentication.md#log-in-with-the-administrators-user-credentials-without-previously-changing-them-or-applying-sql-injection) |
| Security Policy      | Behave like any "white hat" should                                                                           | [  :bulb:  ](roll-your-own-security.md#behave-like-any-white-hat-should)                                                                          |
| Weird Crypto         | Inform the shop about an algorithm or library it should definitely not use the way it does.                  | [  :bulb:  ](sensitive-data-exposure.md#inform-the-shop-about-an-algorithm-or-library-it-should-definitely-not-use-the-way-it-does)               |

### Medium Challenges (  :star::star::star:  )

| Challenge              | Description                                                                                                          | Hints                                                                                                    |
|:-----------------------|:---------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| Blockchain Tier 1      | Learn about the Token Sale before its official announcement.                                                         | [  :bulb:  ](security-through-obscurity.md#learn-about-the-token-sale-before-its-official-announcement)  |
| Forged Feedback        | Post some feedback in another users name.                                                                            | [  :bulb:  ](broken-access-control.md#post-some-feedback-in-another-users-name)                          |
| Forgotten Sales Backup | Access a salesman's forgotten backup file.                                                                           | [  :bulb:  ](security-misconfiguration.md#access-a-salesmans-forgotten-backup-file)                      |
| Login Bender           | Log in with Bender's user account.                                                                                   | [  :bulb:  ](injection.md#log-in-with-benders-user-account)                                              |
| Login Jim              | Log in with Jim's user account.                                                                                      | [  :bulb:  ](injection.md#log-in-with-jims-user-account)                                                 |
| Payback Time           | Place an order that makes you rich.                                                                                  | [  :bulb:  ](improper-input-validation.md#place-an-order-that-makes-you-rich)                            |
| Product Tampering      | Change the `href` of the link within the O-Saft product description into http://kimminich.de.                        | [  :bulb:  ](broken-access-control.md#change-the-href-of-the-link-within-the-o-saft-product-description) |
| Reset Jim's Password   | Reset Jim's password via the Forgot Password mechanism with _the truthful answer_ to his security question.          | [  :bulb:  ](broken-authentication.md#reset-jims-password-via-the-forgot-password-mechanism)             |
| Upload Size            | Upload a file larger than 100 kB.                                                                                    | [  :bulb:  ](improper-input-validation.md#upload-a-file-larger-than-100-kb)                              |
| Upload Type            | Upload a file that has no .pdf extension.                                                                            | [  :bulb:  ](improper-input-validation.md#upload-a-file-that-has-no-pdf-extension)                       |
| XSS Tier 2             | Perform a _persisted_ XSS attack with `<script>alert("XSS")</script>` bypassing a client-side security mechanism.    | [  :bulb:  ](xss.md#perform-a-persisted-xss-attack-bypassing-a-client-side-security-mechanism)           |
| XSS Tier 3             | Perform a _persisted_ XSS attack with `<script>alert("XSS")</script>` without using the frontend application at all. | [  :bulb:  ](xss.md#perform-a-persisted-xss-attack-without-using-the-frontend-application-at-all)        |
| XXE Tier 1             | Retrieve the content of `C:\Windows\system.ini` or `/etc/passwd` from the server.                                    | [  :bulb:  ](xxe.md#retrieve-the-content-of-cwindowssystemini-or-etcpasswd-from-the-server)              |

### Hard Challenges (  :star::star::star::star:  )

| Challenge                  | Description                                                                                                                        | Hints                                                                                                        |
|:---------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| CSRF                       | Change Bender's password into _slurmCl4ssic_ without using SQL Injection.                                                          | [  :bulb:  ](broken-authentication.md#change-benders-password-into-slurmcl4ssic-without-using-sql-injection) |
| Easter Egg Tier 1          | Find the hidden easter egg.                                                                                                        | [  :bulb:  ](roll-your-own-security.md#find-the-hidden-easter-egg)                                           |
| Easter Egg Tier 2          | Apply some advanced cryptanalysis to find _the real_ easter egg.                                                                   | [  :bulb:  ](security-through-obscurity.md#apply-some-advanced-cryptanalysis-to-find-the-real-easter-egg)    |
| Eye Candy                  | Travel back in time to the golden era of web design.                                                                               | [  :bulb:  ](forgotten-content.md#travel-back-in-time-to-the-golden-era-of-web-design)                       |
| Forgotten Developer Backup | Access a developer's forgotten backup file.                                                                                        | [  :bulb:  ](roll-your-own-security.md#access-a-developers-forgotten-backup-file)                            |
| Login Bjoern               | Log in with Bjoern's user account without previously changing his password, applying SQL Injection, or hacking his Google account. | [  :bulb:  ](broken-authentication.md#log-in-with-bjoerns-user-account)                                      |
| Misplaced Signature File   | Access a misplaced SIEM signature file.                                                                                            | [  :bulb:  ](roll-your-own-security.md#access-a-misplaced-siem-signature-file)                               |
| NoSQL Injection Tier 1     | Let the server sleep for some time. (It has done more than enough hard work for you)                                               | [  :bulb:  ](injection.md#let-the-server-sleep-for-some-time)                                                |
| NoSQL Injection Tier 2     | Update multiple product reviews at the same time.                                                                                  | [  :bulb:  ](injection.md#update-multiple-product-reviews-at-the-same-time)                                  |
| Redirects Tier 2           | Wherever you go, there you are.                                                                                                    | [  :bulb:  ](roll-your-own-security.md#wherever-you-go-there-you-are)                                        |
| Reset Bender's Password    | Reset Bender's password via the Forgot Password mechanism with _the truthful answer_ to his security question.                     | [  :bulb:  ](broken-authentication.md#reset-benders-password-via-the-forgot-password-mechanism)              |
| Steganography Tier 1       | Rat out a notorious character hiding in plain sight in the shop. (Mention the exact name of the character)                         | [  :bulb:  ](security-through-obscurity.md#rat-out-a-notorious-character-hiding-in-plain-sight-in-the-shop)  |
| Typosquatting Tier 1       | Inform the shop about a _typosquatting_ trick it has become victim of. (Mention the exact name of the culprit)                     | [  :bulb:  ](vulnerable-components.md#inform-the-shop-about-a-typosquatting-trick-it-has-become-victim-of)   |
| User Credentials           | Retrieve a list of all user credentials via SQL Injection                                                                          | [  :bulb:  ](injection.md#retrieve-a-list-of-all-user-credentials-via-sql-injection)                         |
| Vulnerable Library         | Inform the shop about a vulnerable library it is using. (Mention the exact library name and version in your comment)               | [  :bulb:  ](vulnerable-components.md#inform-the-shop-about-a-vulnerable-library-it-is-using)                |
| XSS Tier 4                 | Perform a _persisted_ XSS attack with `<script>alert("XSS")</script>` bypassing a server-side security mechanism.                  | [  :bulb:  ](xss.md#perform-a-persisted-xss-attack-bypassing-a-server-side-security-mechanism)               |

### Dreadful Challenges (  :star::star::star::star::star:  )

| Challenge               | Description                                                                                                                                              | Hints                                                                                                                              |
|:------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| CAPTCHA Bypass          | Submit 10 or more customer feedbacks within 10 seconds.                                                                                                  | [  :bulb:  ](roll-your-own-security.md#submit-10-or-more-customer-feedbacks-within-10-seconds)                                     |
| Extra Language          | Retrieve the language file that never made it into production.                                                                                           | [  :bulb:  ](forgotten-content.md#retrieve-the-language-file-that-never-made-it-into-production)                                   |
| JWT Issues Tier 1       | Forge an essentially unsigned JWT token that impersonates the (non-existing) user _jwtn3d@juice-sh.op_.                                                  | [  :bulb:  ](vulnerable-components.md#forge-an-essentially-unsigned-jwt-token)                                                     |
| Login CISO              | Exploit OAuth 2.0 to log in with the Chief Information Security Officer's user account.                                                                  | [  :bulb:  ](broken-authentication.md#exploit-oauth-20-to-log-in-with-the-cisos-user-account)                                      |
| RCE Tier 1              | Perform a Remote Code Execution that would keep a less hardened application busy forever.                                                                | [  :bulb:  ](insecure-deserialization.md#perform-a-remote-code-execution-that-would-keep-a-less-hardened-application-busy-forever) |
| Reset Bjoern's Password | Reset Bjoern's password via the Forgot Password mechanism with _the truthful answer_ to his security question.                                           | [  :bulb:  ](broken-authentication.md#reset-bjoerns-password-via-the-forgot-password-mechanism)                                    |
| Reset Morty's Password  | Reset Morty's password via the Forgot Password mechanism with _his obfuscated answer_ to his security question.                                          | [  :bulb:  ](security-misconfiguration.md#reset-mortys-password-via-the-forgot-password-mechanism)                                 |
| Retrieve Blueprint      | Deprive the shop of earnings by downloading the blueprint for one of its products                                                                        | [  :bulb:  ](forgotten-content.md#deprive-the-shop-of-earnings-by-downloading-the-blueprint-for-one-of-its-products)               |
| Supply Chain Attack     | Inform the development team about a danger to some of _their_ credentials. (Send them the URL of the _original report_ or the CVE of this vulnerability) | [  :bulb:  ](broken-authentication.md#inform-the-development-team-about-a-danger-to-some-of-their-credentials)                     |
| Typosquatting Tier 2    | Inform the shop about a more literal instance of _typosquatting_ it fell for. (Mention the exact name of the culprit)                                    | [  :bulb:  ](vulnerable-components.md#inform-the-shop-about-a-more-literal-instance-of-typosquatting-it-fell-for)                  |
| XXE Tier 2              | Give the server something to chew on for quite a while.                                                                                                  | [  :bulb:  ](xxe.md#give-the-server-something-to-chew-on-for-quite-a-while)                                                        |

### Diabolic Challenges (  :star::star::star::star::star::star:  )

| Challenge           | Description                                                                                                     | Hints                                                                                                                                       |
|:--------------------|:----------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| Forged Coupon       | Forge a coupon code that gives you a discount of at least 80%.                                                  | [  :bulb:  ](sensitive-data-exposure.md#forge-a-coupon-code-that-gives-you-a-discount-of-at-least-80)                                       |
| Imaginary Challenge | Solve challenge #99. Unfortunately, this challenge does not exist.                                              | [  :bulb:  ](sensitive-data-exposure.md#solve-challenge-99)                                                                                 |
| JWT Issues Tier 2   | Forge an almost properly RSA-signed JWT token that impersonates the (non-existing) user _rsa_lord@juice-sh.op_. | [  :bulb:  ](vulnerable-components.md#forge-an-almost-properly-rsa-signed-jwt-token)                                                        |
| Login Support Team  | Log in with the support team's original user credentials without applying SQL Injection or any other bypass.    | [  :bulb:  ](security-misconfiguration.md#log-in-with-the-support-teams-original-user-credentials)                                          |
| Premium Paywall     | Unlock Premium Challenge to access exclusive content.                                                           | [  :bulb:  ](sensitive-data-exposure.md#unlock-premium-challenge-to-access-exclusive-content)                                               |
| RCE Tier 2          | Perform a Remote Code Execution that occupies the server for a while without using infinite loops.              | [  :bulb:  ](insecure-deserialization.md#perform-a-remote-code-execution-that-occupies-the-server-for-a-while-without-using-infinite-loops) |


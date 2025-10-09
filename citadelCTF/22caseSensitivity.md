# Case Sensitivity

**Flag:** `citadel{d34th_d035_n07_fr33_y0u_fr0m_7h3_gu17ar15t}`

This took a LOT of time. Pretty much everything was blocked, and the program gave weird hints like `print is very close`. GPT wasn't of any use either, it kept telling me to type `import` even though I told it that doesn't work. I figured out that print and environ have the same *you're close* message. Then the name of the challenge hit me and I found out that `.lower()` was working. Soon, I ran `exec('PRINT(ENVIRON)'.lower())` to finally get the flag.


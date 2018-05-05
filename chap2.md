# How The Attacker Will Attempt, Succeed, And Fail To Unlock/Bypass FileVault 2 Encryption On Target’s Computer

## Attacker Obtaining The 256-bit XTS-AES Key

To recover the 256-bit XTS-AES key, an attacker has to dump the content of the OS X system’s RAM into a file. Unfeasible since the adversary wishes that the user is logged into his/her account which would mean that the access to the hard disk is available. Not always possible.

## Attacker Obtaining Recovery Key

In terms of the recovery key: The attacker could acquire a warrant, look for it at the user’s premises \(If he/she is dumb enough to store a physical copy in the first place\). The warrant is futile when the user did not store the recovery key in his/her iCloud account. \(Who honestly would store it in their iCloud account?\)

In reality, the adversary has no chance in recovering a recovery key even if he has tremendous resources like a supercomputer.

## Attacker Obtaining User Password

To retrieve the user password, the well-funded attacker would run a brute-force tool that is commercially available for purchase by digital forensic companies.

With the brute-force tool, the adversary will attempt to extract the imperative information regarding the encrypted volume and save the file. Adversary proceeds to run the brute-force utility on the saved file with the dictionary wordlist carefully chosen. If the brute-force attack is successful, the attacker obtains the password to unlock the OS X system that contains the encrypted volume.

Clearly, the adversary cannot always win. This is especially true when the Mac user has a long and complex password consisting of mixed case/numbers/symbols that are randomly selected. The attacker is essentially defeated since he does not have 10 centuries and probably lacks a quantum computer. The adversary that has a NVIDIA GTX 1080 GPU on his computer will run a brute force attack approximately trying 10,000 passwords per second. This is mediocre. But if the adversary has 4 GTX 1080 GPUs on a single computer, the brute-force speed will be 40,000. Without a GPU accelerator, the CPU speed will range from 18 to 50 passwords per second.

We know that brute-force will always win at the end given enough time, but even one century is a long time to wait.

## Weaken Attackers’ Ability To Unlock Encrypted Volume By Limiting The Number Of OS User Accounts On Computer

Do not enable additional user accounts which can be used and exploited to unlock the encrypted FileVault 2 volume. Do not create more than one user account on the OS X computer. An adversary with tremendous forensic capabilities will have a better chance of recovering one of the interested passwords. Hence, avoid deploying more than one FileVault 2 Password.


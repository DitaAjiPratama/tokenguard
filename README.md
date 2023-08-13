# TokenGuard

Python Script for authentication with JWT method and RS256 algorithm.

It need pyjwt[crypto] python library.

## Usage

Here is for encode

    import tokenguard

    payload     = {
        "your_parameters" : "your_value"
    }

    private_key = "your_ssh_dir/id_rsa"
    passphrase  = b'your_pass'      # if you use password
    passphrase  = None              # if you don't use password

    token       = tokenguard.encode(payload, private_key, passphrase)

and here is for decode

    import tokenguard

    token       = "xxxxxx.xxxxxx.xxxxxx"
    public_key  = "your_ssh_dir/id_rsa.pub"

    payload     = tokenguard.decode(token, public_key)

# auto-aws-sync
A simple bash script to automatically update an AWS bucket as you work.

# Dependencies
This script has two dependencies:
- The CLI for Amazon Web Services, `aws-cli`
- `inotify-tools`, to watch for changes in a specific folder

# Supported Operating Systems
This script supports Windows 10 with WSL (Windows Subsystem for Linux,
Mac OS X, and Linux (so long as you have bash, most distros do).

# Installation
Copy and paste this script into a file, change permissions to 755, and
save. You may wish to include this in your Bash `PATH` variable.

If need be, copy/paste this into your terminal.

```
cd ~;
wget https://raw.githubusercontent.com/dandalton1/auto-aws-sync/master/auto-aws-sync;
chmod 755 auto-aws-sync;
echo "Woo-hoo! You did it!";
```

# Invocation
Run `auto-aws-sync` in the folder you want updated, with your bucket name as a
parameter. For example, say your bucket name is named `www.john.com`, run the
script with `auto-aws-sync www.john.com`.

# PUT Requests
Note that using the CLI to update AWS will count against your account's PUT
request limit. See [Amazon S3 Pricing](https://aws.amazon.com/s3/pricing/) for
more details.

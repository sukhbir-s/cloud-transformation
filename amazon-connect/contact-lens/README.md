## Prerequisites:

You should have the following prerequisites:

- An [AWS account](https://portal.aws.amazon.com/billing/signup/resume&client_id=signup) with both management console and programmatic administrator access
- An existing [Amazon Connect](http://aws.amazon.com/connect) instance with Contact Lens enabled and configured within an appropriate contact flow
- Upgrade AWS CLI with the latest version from this [link](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html) based on the Operating System that you are using.

## Getting Started

## Downloading Contact Lens Rules Library from Github
Download the Contact Rules library from GitHub. You can do that by cloning our public repository here:

```
$ git clone https://github.com/sukhbir-s/cloud-transformation.git
```

Once you download the files, navigate to the directory where you have downloaded the json files.

## Creating Contact Lens Rules using AWS CLI
- Replace "YOUR_INSTANCE_ID" with your unique Amazon Connect Instance ID.  This can be found by navigating to your Amazon Connect console at https://console.aws.amazon.com/connect/, opening the instance page, and choosing your instance alias.  The information after **instance/** is your instance ID.
- Replace [FOLDER]/[RULE] with the file name of the Contact Lens rule you intend to upload.

```
$ aws connect create-rule --instance-id "YOUR_INSTANCE_ID" --cli-input-json file://[FOLDER]/[RULE].json
```
-  As an example if you wanted to deploy the Apology rule you would end up with the following command:
```
$ aws connect create-rule --instance-id abcdefgh-ijkl-mnop-qrst-uvwxyz123456 --cli-input-json file://Apology/create-apology-voice-postcall.json
```
## License

This library is licensed under the MIT-0 License. See the LICENSE file.


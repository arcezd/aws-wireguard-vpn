# Wireguard Server VPN | Cloudformation template

## Prerequisites
- AWS Account
- Cloudformation CLI

## Getting started
1. Create a copy of the `parameters.example.json` as `parameters.json` and modify your values:
```json
[
  {
    "ParameterKey": "OriginIP",
    "ParameterValue": "1.2.3.4/32"
  },
  {
    "ParameterKey": "KeyName",
    "ParameterValue": "YOUR_KEY_NAME"
  }
]
```
2. Deploy cloudformation stack executing:
```shell
  aws cloudformation create-stack \
  --stack-name wireguardvpn \
  --template-body file://WireguardVPN_AmazonLinux2.template \
  --parameters file://parameters.example.json
```

## Useful links
- [https://www.wireguard.com/](https://www.wireguard.com/)
- [Amazon Linux 2 AMI is now available with kernel 5.10](https://aws.amazon.com/about-aws/whats-new/2021/11/amazon-linux-2-ami-kernel-5-10/)
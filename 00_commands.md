# Verify version
```sh
python3 --version
Python 3.8.1

pip3 --version
pip 19.2.3 from /Library/Frameworks/Python.framework/Versions/3.8/lib/python3.8/site-packages/pip (python 3.8)
```

# Install cli

```sh
pip3 install --user aws-sam-cli
```


# git: push an existing repository from the command line

```sh
git init
git remote add origin https://github.com/robin8a/getting_started_with_aws_sam.git
git add .
git ci -m "Initial commit"

git push -u origin master
```


# SAM

## S3 Bucket
```sh
aws s3 mb s3://kl-tbu-sam-chatbot-translator
```

## Cloud formation
```sh
# package cloudformation
aws cloudformation package help
aws cloudformation package --s3-bucket kl-tbu-sam-chatbot-translator --template-file template.yaml --output-template-file gen/template-generated.yaml

# execute the following command to deploy the packaged template
xecute the following command to deploy the packaged template
aws cloudformation deploy --template-file /Users/robin8a/Documents/getting_started_with_aws_sam/gen/template-generated.yaml --stack-name <YOUR STACK NAME>

aws cloudformation deploy --template-file gen/template-generated.yaml --stack-name kl-st-udemy-hello-world-sam

aws cloudformation deploy --template-file gen/template-generated.yaml --stack-name kl-st-udemy-hello-world-sam --capabilities CAPABILITY_IAM --parameter-overrides IdentityNameParameter=xyz

```
# alibaba-python-sdk-examples

## Feature
* ECS

## Pre-requesteries

### Install pip

There mutliple ways to install pip. The easier being:
```bash
$ wget https://bootstrap.pypa.io/get-pip.py
Saving to: ‘get-pip.py’

$ sudo python get-pip.py
Collecting pip
...
Installing collected packages: pip, wheel
...
Successfully installed pip-9.0.1 wheel-0.30.0

$ pip -V
pip 9.0.1 from /Library/Python/2.7/site-packages (python 2.7)
```

You can refer to [the official page](https://pip.pypa.io/en/stable/installing/ "PIP's Homepage") for alternative installation procedure

### Create SDK Key on Alibaba Cloud

#### Notes

This repository is only for the people using the Public Cloud of Alibaba Cloud. For further assistance on the Private Cloud, please refer to the [official documentation](https://www.alibabacloud.com/help/zh/doc-detail/43039.htm "公共云版")

We will create the **access key ID** and **access key secret** necessary to call the Open API used by Alibaba Cloud SDK.

#### Access key creation

Visit your Alibaba Cloud console at this URL: https://home.console.aliyun.com/

Once logged in, ALL THE SCREENS

### Install Alibaba Cloud Python SDK(s)

You need to install the **aliyuncli** first in order to use the Python SDK from command line
```bash
$ sudo pip install aliyuncli
Collecting aliyuncli
...
Installing collected packages: colorama, jmespath, aliyuncli
...
Successfully installed aliyuncli-2.1.9 colorama-0.3.3 jmespath-0.7.1
```

Now you can install each SDK via pip using the following command:
```bash
$ sudo pip install [ sdk-name ]
```

#### [ sdk-name ] used in this repository
* aliyun-python-sdk-ecs

You can refer to [the official page](https://develop.aliyun.com/tools/sdk?#/python "Alibaba Cloud Python SDK's Homepage") for other SDK(s)


### Configure Alibaba Cloud Python SDK(s)

After creating the access key and access secret, you may configure aliyuncli: :

```bash
$ aliyuncli configure
Aliyun Access Key ID [None]: <Your aliyun access key id>
Aliyun Access Key Secret [None]: <Your aliyun access key secret>
Default Region Id [None]: <your preferred region>
Default output format [None]: <your proferred output-format>
```

#### Regions Available:
* cn-qingdao 
* cn-beijing
* cn-zhangjiakou
* cn-hangzhou
* cn-shanghai
* cn-shenzhen
* cn-hongkong
* ap-northeast-1
* ap-southeast-1
* ap-southeast-2
* us-east-1
* us-west-1
* me-east-1
* eu-central-1

Alternatively you can query them later on with the following command:
```bash
$ aliyuncli ecs DescribeRegions --output json --filter Regions.Region[*].RegionId
```

#### Output Format Available:
* table
* JSON
* text

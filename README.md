# assume-role
## Prerequisite 
Assume Role requires to have installed the following:
* [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-install-macos.html)
* [Java 1.8](https://docs.oracle.com/javase/8/docs/technotes/guides/install/install_overview.html)
* [Okta AWS CLI Assume Role Tool](https://github.com/oktadeveloper/okta-aws-cli-assume-role#installation)

## Installation
Into the root project, execute the following command:
```bash
$ ./assume-role install
```
Assume Role copies itself into `/usr/local/bin` to be widely available. 

## Usage
### Adding a new profile 
```bash
$ assume-role add <profile>
```

You will be asked to fill the needed information to create a AWS Session through the `Okta AWS CLI Assume Role tool` which are:

 1. The Okta orgianization (OKTA_ORG). 
 2. The AWS APP URL (OKTA_AWS_APP_URL) that you can get by login the browser and then copy the link for the chiclet. 
 4. The AWS default region (AWS_REGION)
 5. The AWS default output (AWS_OUTPUT)

### Removing a profile

Deletes the profile

```bash
$ assume-role remove <profile>
```

### Listing available profiles

Displays a list of all available profiles

```bash
$ assume-role list
```


### Login 

```bash
$ assume-role login <profile>
```

### Logout 

Logout will invalidate all present sessions. 

```bash
$ assume-role logout
```


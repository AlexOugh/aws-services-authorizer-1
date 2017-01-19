
# Custom Authorizer

Lambda Function for custom authorizer in API Gateway

![aws-services][aws-services-image]

## How To Setup a CodePipeline

Please see here, https://github.com/SungardAS/aws-services-federation#how-to-setup-a-codepipeline

And follow either way to set input parameter values of the template when creating a build action whose mode is 'Create of replace a change set'

  1. Using a configuration file

    > Create a configuration json file that has input parameter values as below

          {
              "Parameters": {
                "SSOHost": "value1",
                "SSOBasicAuthUsername": "value2",
                "SSOBasicAuthPassword": "value2",
                "SSOMasterToken": "value2"
              }
          }

    > Set the name of the above json file in 'Template configuration' using below format

        InputArtifactName::TemplateConfigurationFileName

    like

        MyAppBuild::env_dev.json

  2. Set the parameter json in 'Parameter overrides' under 'Advanced' setting


## How To Test Lambda Functions

- $ cd tests
- Export environment variables, SSO_HOST, SSO_BASIC_AUTH_USERNAME, SSO_BASIC_AUTH_PASSWORD, SSO_MASTER_TOKEN
- Replace \<username\> and \<password\> with proper values in 'test_authorizer.py'
- $ python test_authorizer.py

## [![Sungard Availability Services | Labs][labs-logo]][labs-github-url]

This project is maintained by the Labs group at [Sungard Availability
Services](http://sungardas.com)

GitHub: [https://sungardas.github.io](https://sungardas.github.io)

Blog:
[http://blog.sungardas.com/CTOLabs/](http://blog.sungardas.com/CTOLabs/)

[labs-github-url]: https://sungardas.github.io
[labs-logo]: https://raw.githubusercontent.com/SungardAS/repo-assets/master/images/logos/sungardas-labs-logo-small.png
[aws-services-image]: ./docs/images/logo.png?raw=true
[aws-services-image]: ./docs/images/logo.png?raw=true

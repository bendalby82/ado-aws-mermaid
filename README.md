# Azure DevOps - Drawing AWS Diagrams with Mermaid
## Introduction
Ever wondered what this button does in the Azure DevOps Wiki Editor?  

![Azure DevOps Wiki Editor](https://github.com/bendalby82/ado-aws-mermaid/blob/main/images/azure-devops-mermaid-button.png)

Azure DevOps Wiki has native support for Mermaid, which means you can draw pretty good diagrams right there in your markdown:  

![Serverless Architecture](https://github.com/bendalby82/ado-aws-mermaid/blob/main/images/azure-devops-wiki.png)  
  
This is not as good as a full-featured editor like Visio, but on the other hand it is extremely easy to maintain, and Mermaid does the heavy lifting of working out how your diagram nodes are connected together.  

## Sample Code
You can see the code behind the diagram right [here](https://raw.githubusercontent.com/bendalby82/ado-aws-mermaid/main/wiki/Architecture.md)  
  
## Limitations  
1. Font Awesome is not supported by Azure DevOps Wiki, plus another couple of things ([see here](https://docs.microsoft.com/en-us/azure/devops/project/wiki/wiki-markdown-guidance?view=azure-devops#add-mermaid-diagrams-to-a-wiki-page))
2. It is all manual work to make Mermaid objects look vaguely AWS-like - but adding the right colours and a few different shapes goes a long way
3. It seems that 'Provisioned' Wikis have slightly better support than 'Published' Wikis for Mermaid - special characters (&amp;) are parsed correctly in provisioned Wikis, but are treated as syntax errors by published Wikis. ([see here for intro to the differences](https://docs.microsoft.com/en-us/azure/devops/project/wiki/provisioned-vs-published-wiki?view=azure-devops))

## Further Reading
**Syntax for Mermaid Flowcharts**  
https://mermaid-js.github.io/mermaid/#/flowchart

**Publish an Azure DevOps Git repository to a wiki**  
https://docs.microsoft.com/en-us/azure/devops/project/wiki/publish-repo-to-wiki?view=azure-devops&tabs=browser#publish-a-git-repository-to-a-wiki-1

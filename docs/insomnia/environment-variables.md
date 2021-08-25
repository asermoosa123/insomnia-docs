---
layout: article-detail
title:  Environment Variables
category: "Get Started"
category-url: get-started
---

When communicating with APIs, it's common to repeat identical values across multiple requests. Manually typing the value each time can be cumbersome and also makes it difficult to modify in the future. Environment variables solve this problem by allowing you to define a value once, as an environment variable, and reference that value wherever it's needed.

Common variables are base URLs, authentication tokens, and resource IDs.

Example using base_url and petId variables in the URL.

## Environment Basics

An environment is a [JSON object](https://www.json.org/json-en.html) containing key-value pairs of the data you want to reference. Access the environment manager through the environment dropdown menu at the top of the sidebar. From here, you can edit the base environment, create sub environments, assign colors, and more. Here's an example of what an environment might look like.

{:.alert .alert-primary}
**Note**: Variable names must only contain letters, numbers, and underscores.

## Referencing Environment Variables

Environment variables can be referenced in (almost) any text input within of the Insomnia application. There are two ways to do this:

1. Summon the autocomplete dropdown by pressing Control+Space
2. Allow the autocomplete to show automatically as you type

Once a variable is selected, it will be displayed with a colored placeholder. Clicking on the button will show a modal dialog for further editing.

{:.alert .alert-primary}
**Note**: Hovering over the placeholder with your mouse will show the current value.

## Base Environment

A base environment is assigned to every workspace within Insomnia and can be accessed via the environment manager. Variables in the base environment are available throughout the entire workspace, even if other environments are defined. A common use for the base environment is to store default variables that will not change across production, staging, or development services such as resource names, languages, sample data, etc.

## Sub Environments
Sub environments are most commonly used for store variables related to production, staging, or development services. They are also sometimes used to defining variables for different users of a single app. Once sub environments exist, they can be activated via the environment dropdown.

{:.alert .alert-primary}
**Note**: Sub environments can be created as Private, meaning they will never be synced or exported.

## Folder Environments
Folder environments are a rarely used feature, but can be invaluable for specific use cases. You can access a folder's environment from the folder dropdown in the sidebar. Any variables defined at the folder-level will be available to all requests within that folder. These will also override any variables defined within a sub environment or base environment.

## Environment Priority
If two variables with the same name are defined in multiple environments, the environment with higher priority will win. Here is the priority of environment, ranging from highest to lowest:

1. Folder Environment (highest priority)
2. Sub Environment
3. Base Environment (lowest priority)

For example, if a variable is defined in a base environment and in a sub environment, the value in the sub environment will overwrite the one in the base environment.

## Recursive Variables
Environments can reference other variables, including variables defined within itself. This is especially useful for composing more complex variables such as the domain name in the following example.

{:.alert .alert-primary}
**Note**: Environment variables can also contain Template Tags. Recursive, or nested, variables only work while the environment is active.

## Conclusion
Environment variables are perhaps the most beneficial feature of Insomnia. They set it apart from more basic tools like Curl, allowing you to save time and organize important values. Take the time to learn to take advantage of environments in your workflow and you will be much more productive!
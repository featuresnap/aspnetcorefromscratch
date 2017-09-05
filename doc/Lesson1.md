# ASP.Net Core From Scratch

## Lesson 1: Creating Solutions with `dotnet new`

This lesson covers the use of the `dotnet new` command to create new solutions.

### Start With a Working Directory

For the examples in this section, create an empty directory and navigate into it:

```bash
mkdir aspnetcorefromscratch && cd aspnetcorefromscratch
```

### What can `dotnet new` create ?

The `dotnet new` command is used to create new items including solutions, projects, and other files, based on templates that are either prepackaged with the .Net Core SDK, or installed as [custom templates](https://docs.microsoft.com/en-us/dotnet/core/tools/custom-templates).

To see all the options for `dotnet new`, as well as all the available templates currently installed, execute `dotnet new --help`.

### Exercises

1. Creating a new solution with default name:

    The `dotnet new sln` command creates a new solution file.

    Try this:
    ```bash
    $ dotnet new sln
    The template "Solution File" was created successfully.
    ```

    What does `dotnet new sln` choose for the name of the solution file?

    ```bash
    $ ls
    aspnetcorefromscratch.sln
    ```

1. Creating a solution with a custom name:

    The `--name` option allows specifying a custom name for the solution file.

    Try this:

    ```bash
    $ dotnet new sln --name MySolution
    The template "Solution File" was created successfully.
    ```

    If you did not remove any files since creating the first solution, you should now have two solution files in the directory.

    ```bash
    $ ls
    aspnetcorefromscratch.sln  MySolution.sln
    ```

1. Creating a solution with a custom name and file extension:

    What happens if you specify the .sln extension when creating a solution file with a custom name?

    Try this:
    ```bash
    $ dotnet new sln --name MyOtherSolution.sln
    The template "Solution File" was created successfully.

    $ ls
    aspnetcorefromscratch.sln  MyOtherSolution.sln.sln  MySolution.sln
# Create File Action (Any Platform)
Github Action to create a new file from environment config (on any platform)

Inspired by finnp/create-file-action

## Text Files
#### Usage
```workflow
- uses: "bartonip/create-file-action-any-platform@master"
      with:
        filename: "your/file/path/file.txt"
        data: "SOME SECRET VALUE"
```

## Binary Files
#### Usage
```workflow
- uses: "bartonip/create-file-action-any-platform@master"
      with:
        filename: "your/file/path/file.gif"
        data: "R0lGODlhAQABAIAAAP///wAAACHBAEAAAAALAAAAAABAAEAAAICRAEAOw=="
        isBase64: "true"
```

#### File Conversion
**Mac/Unix**

```bash
cat ~/your/file/path | base64
```

**Windows (Powershell)**

```powershell
[convert]::ToBase64String((Get-Content -path "C:\Your\File\Path" -Encoding byte))
````

# Create File Action (Any Platform)
Github Action to create a new file from environment config (on any platform)

Inspired by finnp/create-file-action

## Text Files
#### Usage
```workflow
- uses: "bartonip/create-file-action-any-platform@master"
      env:
        FILE_NAME: "dir/fileName.txt"
        FILE_DATA: "file content"
```

## Binary Files
#### Usage
```workflow
- uses: "bartonip/create-file-action-any-platform@master"
      env:
        FILE_NAME: "dir/fileName.txt"
        FILE_BASE64: "ZWFzdGVyZWdnLWxvbAo="
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

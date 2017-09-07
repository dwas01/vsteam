---
external help file: Team-Help.xml
Module Name: 
online version: 
schema: 2.0.0
---

# Add-TeamAccount

## SYNOPSIS
Stores your account name and personal access token for use with the other
functions in this module.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Add-TeamAccount [-Account] <String> -PAT <SecureString> [-Level <String>]
```

### UNNAMED_PARAMETER_SET_2
```
Add-TeamAccount [-PersonalAccessToken] <String> [[-Account] <String>] [-Level <String>]
```

### UNNAMED_PARAMETER_SET_3
```
Add-TeamAccount [[-Account] <String>] [-UseWindowsAuthentication]
```

## DESCRIPTION
On Windows you have to option to store the information at the process, user
or machine (you must be running PowerShell as administrator) level.
On Linux
and Mac you can only store at the process level.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Add-TeamAccount
```

You will be prompted for the account name and personal access token.

### -------------------------- EXAMPLE 2 --------------------------
```
Add-TeamAccount -Account mydemos -PersonalAccessToken 7a8ilh6db4aforlrnrqmdrxdztkjvcc4uhlh5vgbmgap3mziwnga
```

Allows you to provide all the information on the command line.

### -------------------------- EXAMPLE 3 --------------------------
```
Add-TeamAccount -Account http://localtfs:8080/tfs/DefaultCollection -UseWindowsAuthentication
```

On Windows, allows you use to use Windows authentication against a local TFS server.

## PARAMETERS

### -Account
The Visual Studio Team Services (VSTS) account name to use.
DO NOT enter the
entire URL. 
Just the portion before visualstudio.com.
For example in the
following url mydemos is the account name.
https://mydemos.visualstudio.com
or
The full Team Foundation Server (TFS) url including the collection.
http://localhost:8080/tfs/DefaultCollection

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_2, UNNAMED_PARAMETER_SET_3
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PAT
A secured string to capture your personal access token. 
This will allow you
to provide your personal access token without displaying it in plain text.

To use pat simply omit it from the Add-TeamAccount command.

```yaml
Type: SecureString
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Level
On Windows allows you to store your account information at the Process, User or Machine levels. 
When saved at the User or Machine level your account information will be in any future PowerShell processes.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1, UNNAMED_PARAMETER_SET_2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PersonalAccessToken
The personal access token from VSTS/TFS to use to access this account.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseWindowsAuthentication
Allows the use of the current user's Windows credentials to authenticate against a local TFS.

```yaml
Type: SwitchParameter
Parameter Sets: UNNAMED_PARAMETER_SET_3
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-TeamAccount]()

---
external help file: JMu-help.xml
Module Name: JMu
online version:
schema: 2.0.0
---

# New-JMuModule

## SYNOPSIS
Creates a new module based on the JMu module template

## SYNTAX

### notemplate (Default)
```
New-JMuModule [-DestinationPath] <String> [-TemplateParameters <Hashtable>] [-Force] [-NoLogo] [-PassThru]
 [-ProgressAction <ActionPreference>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### template
```
New-JMuModule [-DestinationPath] <String> -Template <PSObject> [-TemplateParameters <Hashtable>] [-Force]
 [-NoLogo] [-PassThru] [-ProgressAction <ActionPreference>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Creates a new module based on the JMu module template

## EXAMPLES

### EXAMPLE 1
```
New-JMuModule -DestinationPath ./MyModule
```

Creates a new module called MyModule in the directory ./MyModule

### EXAMPLE 2
```
$template = Get-JMTestTemplate
$params = @{
    DestinationPath = './MyAwesomeModule'
    Force           = $true
    NoLogo          = $true
    TemplateParameters = @{
        ModuleName   = 'MyAwesomeModule'
        Description  = 'My awesome module'
        Version      = '0.1.0'
        FullName     = 'Community'
        License      = 'MIT'
        CoC          = 'No'
        MkDocs       = 'No'
        Classes      = 'Yes'
        PlatyPS      = 'Yes'
        devcontainer = 'Yes'
        CICD         = 'GitHubActions'
    }
}
$template | New-JMuModule @params
```

Gets the JMTest template, then creates a hashtable containing all
required parameters to create a new module without additional prompts.

## PARAMETERS

### -DestinationPath
Destination path for new module

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Template
Plaster template object

```yaml
Type: PSObject
Parameter Sets: template
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TemplateParameters
Template parameters to pass to Invoke-Plaster

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: @{}
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Overwrite existing files in destination path

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoLogo
Suppress the Plaster logo

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Return a InvokePlasterInfo object representing the created module

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgressAction
{{ Fill ProgressAction Description }}

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: proga

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-JMuTemplate]()


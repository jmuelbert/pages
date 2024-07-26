---
external help file: JMu-help.xml
Module Name: JMu
online version:
schema: 2.0.0
---

# Get-JMuTemplate

## SYNOPSIS
Returns JMu's Plaster template

## SYNTAX

```
Get-JMuTemplate [-ProgressAction <ActionPreference>] [<CommonParameters>]
```

## DESCRIPTION
Returns JMu's Plaster template

## EXAMPLES

### EXAMPLE 1
```
$template = Get-JMuTemplate
$template | New-JMuModule
```

Gets the Plaster template from the JMu module and creates a new module with it

## PARAMETERS

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

### System.Management.Automation.PSObject
## NOTES

## RELATED LINKS

[New-JMuModule]()


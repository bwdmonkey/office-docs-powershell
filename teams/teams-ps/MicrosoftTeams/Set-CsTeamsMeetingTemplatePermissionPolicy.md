---
Module Name: MicrosoftTeams
title: Set-CsTeamsMeetingTemplatePermissionPolicy
author: boboPD
ms.author: pradas
online version: https://learn.microsoft.com/powershell/module/teams/Set-CsTeamsMeetingTemplatePermissionPolicy
schema: 2.0.0
---

# Set-CsTeamsMeetingTemplatePermissionPolicy

## SYNOPSIS

This cmdlet updates an existing TeamsMeetingTemplatePermissionPolicy.

## SYNTAX

```powershell
    Set-CsTeamsMeetingTemplatePermissionPolicy 
        [-Identity] <string> 
        [-HiddenMeetingTemplates <PSListModifier[HiddenMeetingTemplate]>] 
        [-Description <string>]
        [-DefaultMeetingTemplateId <string>]
        [-Force]
        [-WhatIf]
        [-Confirm]
        [<CommonParameters>]
```

## DESCRIPTION

Update any of the properties of an existing instance of the TeamsMeetingTemplatePermissionPolicy.

## EXAMPLES

### Example 1

```powershell
PS> Set-CsTeamsMeetingTemplatePermissionPolicy -Identity Foobar -Description "updated description"
```

Updates the description field of a policy.

### Example 2

```powershell
PS> Set-CsTeamsMeetingTemplatePermissionPolicy -Identity Foobar -HiddenMeetingTemplates @($hiddentemplate_1, $hiddentemplate_2)
```

Updates the hidden meeting templates array.

### Example 3

```powershell
PS> Set-CsTeamsMeetingTemplatePermissionPolicy -Identity Foobar -DefaultMeetingTemplateId "customtemplate_9ab0014a-bba4-4ad6-b816-0b42104b5056"
```

Sets the default meeting template that is automatically applied to ad-hoc or standard meetings created by users assigned this policy.

## PARAMETERS

### -Identity

Name of the policy instance to be updated.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Microsoft Teams
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HiddenMeetingTemplates

The updated list of meeting template IDs to hide.
The HiddenMeetingTemplate objects are created with [New-CsTeamsHiddenMeetingTemplate](New-CsTeamsHiddenMeetingTemplate.md).

```yaml
Type: HiddenMeetingTemplate[]
Parameter Sets: (All)
Aliases:
Applicable: Microsoft Teams
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Pass in a new description if that field needs to be updated.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Microsoft Teams
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultMeetingTemplateId

Specifies the ID of the meeting template to be applied by default to ad-hoc or standard meetings created by the user. Must use the `customtemplate_<GUID>` format. When set to null, no default template is applied.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Microsoft Teams
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS
[Get-CsTeamsMeetingTemplatePermissionPolicy](Get-CsTeamsMeetingTemplatePermissionPolicy.md)

[New-CsTeamsMeetingTemplatePermissionPolicy](New-CsTeamsMeetingTemplatePermissionPolicy.md)

[Remove-CsTeamsMeetingTemplatePermissionPolicy](Remove-CsTeamsMeetingTemplatePermissionPolicy.md)

[Grant-CsTeamsMeetingTemplatePermissionPolicy](Grant-CsTeamsMeetingTemplatePermissionPolicy.md)

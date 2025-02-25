---
Module Name: PnP.PowerShell
title: Get-PnPTenantDeletedSite
schema: 2.0.0
applicable: SharePoint Online
external help file: PnP.PowerShell.dll-Help.xml
online version: https://pnp.github.io/powershell/cmdlets/Get-PnPTenantDeletedSite.html
---
 
# Get-PnPTenantDeletedSite

## SYNOPSIS

> [!TIP]
> We encourage you to make improvements to this documentation. Please navigate to https://github.com/pnp/powershell/blob/dev/documentation/Get-PnPTenantDeletedSite.md to change this file.


**Required Permissions**

* SharePoint: Access to the SharePoint Tenant Administration site

Fetches the site collections from the tenant recycle bin.

## SYNTAX

```powershell
Get-PnPTenantDeletedSite [-Identity] <String> [-Limit] [-IncludePersonalSite] [-IncludeOnlyPersonalSite] [-Connection <PnPConnection>] [<CommonParameters>]
```

## DESCRIPTION
Fetches the site collection's which are listed in your tenant's recycle bin.

## EXAMPLES

### EXAMPLE 1
```powershell
Get-PnPTenantDeletedSite
```

This will fetch the site collections from the recycle bin.

### EXAMPLE 2
```powershell
Get-PnPTenantDeletedSite -Identity "https://tenant.sharepoint.com/sites/contoso"
```

This will fetch the site collection with the url 'https://tenant.sharepoint.com/sites/contoso' from the recycle bin and display its properties.

### EXAMPLE 3
```powershell
Get-PnPTenantDeletedSite -IncludePersonalSite
```

This will fetch the site collections from the recycle bin including the personal sites and display its properties.

### EXAMPLE 4
```powershell
Get-PnPTenantDeletedSite -IncludeOnlyPersonalSite
```

This will fetch the site collections from the recycle bin which are personal sites and display its properties.

## PARAMETERS

### -Connection
Optional connection to be used by the cmdlet. Retrieve the value for this parameter by either specifying -ReturnConnection on Connect-PnPOnline or by executing Get-PnPConnection.

```yaml
Type: PnPConnection
Parameter Sets: (All)

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Limit
Limit of the number of site collections to be retrieved from the recycle bin. Default is 200.

```yaml
Type: SwitchParameter
Parameter Sets: (All)

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludePersonalSite
If specified the task will also retrieve the personal sites from the recycle bin.

```yaml
Type: SwitchParameter
Parameter Sets: (All, ParameterSetAllSites)

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeOnlyPersonalSite
If specified the task will only retrieve the personal sites from the recycle bin.

```yaml
Type: SwitchParameter
Parameter Sets: (All, ParameterSetPersonalSitesOnly)

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
Specifies the full URL of the site collection that needs to be restored.

```yaml
Type: String
Parameter Sets: (All)

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## RELATED LINKS

[Microsoft 365 Patterns and Practices](https://aka.ms/m365pnp)


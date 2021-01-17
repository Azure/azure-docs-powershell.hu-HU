---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 791658e9f4f10fdbb8b1000d6b1bc88d392aaf46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468414"
---
# Set-AzSqlServerDnsAlias

## SYNOPSIS
Módosítja azt a kiszolgálót, amelyre az Azure SQL Server DNS-aliasa mutat

## SZINTAXIS

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
Ez a parancs frissíti azt a kiszolgálót, amelyre az alias mutat. Ezt a parancsot akkor kell kiadni, amikor bejelentkezik az előfizetésbe, ahol az új kiszolgáló, amelyre az alias fog mutasson, megtalálható.

## PÉLDÁK

### 1. példa
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

Ez a parancs frissíti az aliast, amely korábban a régiServerre mutatott, hogy az új kiszolgálóra mutasson

## PARAMETERS

### -AsJob
Parancsmag futtatása a háttérben

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Az Azure Sql Server DNS-alias neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceServerName
Annak az Azure Sql Servernek a neve, amelyre az alias jelenleg mutat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceServerResourceGroupName
A forráskiszolgáló erőforráscsoportjának neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceServerSubscriptionId
A forráskiszolgáló előfizetésazonosítója

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetServerName
Az Azure Sql Server neve, amelyre az aliasnak kell mutasson.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

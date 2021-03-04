---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 87830eb9cb4321bf9af1476d3fa5a0db41796351
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936769"
---
# Remove-AzDataCollectionRuleAssociation

## SYNOPSIS
Adatgyűjtési szabály társításának törlése

## SZINTAXIS

### ByName (alapértelmezett)
```
Remove-AzDataCollectionRuleAssociation
      -TargetResourceId <string> 
      -AssociationName <string> 
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### ByInputObject
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### ByResourceId
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## LEÍRÁS
A **Remove-AzDataCollectionRuleAssociation** parancsmag töröl egy adatgyűjtési szabály társítását (DCRA).

DCR virtuális gépre való alkalmazáshoz társítást kell létrehoznia a virtuális géphez. Előfordulhat, hogy egy virtuális gép több DKR-hez kapcsolódik, és a DCR-hez több virtuális gép is társítva lehet. Ez lehetővé teszi, hogy definiálja a tartományvezérlők készletét, amelyek mindegyikének meg kell egyeztet egy bizonyos követelményt, és csak azokra a virtuális gépekre alkalmazza őket, amelyekre vonatkoznak. Az alábbi "Adatgyűjtés konfigurálása az [Azure Monitor-ügynökhöz"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) a DCRA-cikk alapján olvasható.

## PÉLDÁK

### 1. példa: Az adatgyűjtési szabályok társításának törlése névvel és célerőforrás-azonosítóval (társított virtuális gép) paraméterekkel
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### 2. példa: Adatgyűjtési szabály törlése bemeneti objektummal
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### 3. példa: Adatgyűjtési szabály törlése a társítási erőforrás-azonosító tulajdonsággal
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -TargetResourceId
A társított erőforrás-azonosító.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssociationName
A társítási erőforrás neve.

```yaml
Type: System.String
Parameter Sets: ByName (Default)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
PSDataCollectionRuleResource objektum

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -AssociationId
Az erőforrás azonosítója.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String
###Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource

## KIMENETEK

### System.Boolean

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md)

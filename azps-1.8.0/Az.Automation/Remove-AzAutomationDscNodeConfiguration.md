---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 938fde14fb62ea7f7fd4e04baf5e309615957799
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671531"
---
# Remove-AzAutomationDscNodeConfiguration

## Áttekintés
Eltávolítja a metaadatokat a DSC csomópont-konfigurációból az automatizálásban.

## SZINTAXISA

```
Remove-AzAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzAutomationDscNodeConfiguration** parancsmag eltávolítja a metaadatokat az APS-től származó kívánt állapot-konfiguráció (DSC) csomópont-konfigurációkról az Azure automatizálásban.
Az automatizálás a DSC-csomópontok konfigurációját a Managed Object Format (MOF) konfigurációs dokumentumként tárolja.

## Példák

## PARAMÉTEREK

### -AutomationAccountName
Megadja annak az automatizálási fióknak a nevét, amely tartalmazza azokat a DSC csomópont-konfigurációkat, amelyeknél ez a parancsmag eltávolítja a metaadatokat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -Force
ps_force

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreNodeMappings
Azt jelzi, hogy ez a parancsmag figyelmen kívül hagyja a csomópontok megfeleltetését.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
Annak a DSC-csomópontnak a neve, amelyhez ez a parancsmag eltávolítja a metaadatokat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy erőforráscsoport nevét adja meg.
Ez a parancsmag eltávolítja a DSC csomópont-konfigurációk metaadatait abban az erőforráscsoport-konfigurációban, amelyet ez a paraméter határoz meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### System. Void

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAutomationDscNodeConfiguration](./Get-AzAutomationDscNodeConfiguration.md)

[Importálás – AzAutomationDscNodeConfiguration](./Import-AzAutomationDscNodeConfiguration.md)

[Azure automatizálási parancsmagok](./Az.Automation.md)



---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 25b4adeb2d62f1e66bd30cd990db27eadb41b405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491608"
---
# New-AzureRmDeploymentManagerService

## Áttekintés
Szolgáltatást hoz létre a szolgáltatás topológiájában.

## SZINTAXISA

### Interaktív (alapértelmezett)
```
New-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 -Name <String> -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServiceTopologyObject
```
New-AzureRmDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopology] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServiceTopologyResourceId
```
New-AzureRmDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzureRmDeploymentManagerService** parancsmag egy szolgáltatás topológiája alatt hoz létre egy szolgáltatást, és egy olyan objektumot ad eredményül, amely az adott szolgáltatást jelképezi.
Adja meg a szolgáltatást a nevével, a szolgáltatási topológiával, és az erőforráscsoport nevével. 

A parancsmag egy szolgáltatási objektumot ad eredményül. Ezt az objektumot helyileg is módosíthatja, majd a Set-AzureRmDeploymentManagerService parancsmag használatával alkalmazhatja a módosításokat.

## Példák

### Példa 1
```powershell
PS C:\> New-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Új szolgáltatást hoz létre, amelynek neve ContosoService1 a szolgáltatás topológiája ContosoServiceTopology az erőforráscsoport ContosoResourceGroup, a közép-amerikai helyen. A TargetLocation tulajdonság azt jelzi, hogy a szolgáltatás ContosoService1 az adott előfizetésben a kelet-amerikai régióba kell telepíteni.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
A szolgáltatási erőforrás helye.

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

### -Name (név)
A szolgáltatás neve.

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

### -ResourceGroupName
Az erőforráscsoport.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceTopology
A szolgáltatás topológiájának objektuma, amelyben a szolgáltatást létre kell tenni.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceTopologyId
A szolgáltatás topológiája erőforrás-azonosító, amelyben a szolgáltatást létre kell tenni.

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceTopologyName
Annak a szolgáltatásnak a neve, amelyhez a szolgáltatás tartozik.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Címke
Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetLocation
Annak a helynek a meghatározása, ahol a szolgáltatás alatti erőforrásokat telepítették.

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

### -TargetSubscriptionId
Azt az előfizetést határozza meg, amelyre a szolgáltatás alatti erőforrásokat telepítették.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmDeploymentManagerService](./Get-AzureRmDeploymentManagerService.md)

[Remove-AzureRmDeploymentManagerService](./Remove-AzureRmDeploymentManagerService.md)

[Set-AzureRmDeploymentManagerService](./Set-AzureRmDeploymentManagerService.md)
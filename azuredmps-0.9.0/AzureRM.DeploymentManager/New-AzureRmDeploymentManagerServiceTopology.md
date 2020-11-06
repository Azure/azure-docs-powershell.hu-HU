---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: d7e3055c6443faa2c85d63e6cfdb611cb7d2eb41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491580"
---
# New-AzureRmDeploymentManagerServiceTopology

## Áttekintés
Új szolgáltatási topológiát hoz létre.

## SZINTAXISA

```
New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzureRmDeploymentManagerServiceTopology** parancsmag létrehoz egy szolgáltatási topológiát.

A visszaadott ServiceTopology-objektumot helyileg módosíthatja, majd a Set-AzureRmDeploymentManagerServiceTopology parancsmag használatával is alkalmazhatja a módosításokat.
A visszaadott objektum 

A visszaadott objektumnak van egy ResourceId mezője, amely hivatkozhat a bevezetési erőforrásokra, így jelezve, hogy az ebben a szolgáltatási topológiában bejelentett szolgáltatások üzembe helyezése a kivezetésben történik.

## Példák

### Példa 1
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

Ez a parancsmag új szolgáltatási topológiát hoz létre a ContosoResourceGroup nevű erőforráscsoport-ContosoServiceTopology és a közép-amerikai helyen. Az ereklyék forrása ResourceId azt jelzi, hogy az ebben a topológiában a szolgáltatási egység meghatározásához szükséges leleteknek a megadott tárgyi forrásból kell olvasni.

### 2. példa
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

Ez a parancsmag új szolgáltatási topológiát hoz létre a ContosoResourceGroup nevű erőforráscsoport-ContosoServiceTopology és a közép-amerikai helyen. A lelet-forrás hivatkozás hiánya azt jelzi, hogy az ebben a topológiában a szolgáltatási egység meghatározásához szükséges leletek a szolgáltatási egységben abszolút SAS URI-ként jelennek meg.

## PARAMÉTEREK

### -ArtifactSourceId
Annak a tárgynak az azonosítója, ahol a topológiát alkotó leletek vannak tárolva.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
A topológia helye.

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
A topológia neve.

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
Position: Named
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

### Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmDeploymentManagerServiceTopology](./Get-AzureRmDeploymentManagerServiceTopology.md)

[Remove-AzureRmDeploymentManagerServiceTopology](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[Set-AzureRmDeploymentManagerServiceTopology](./Set-AzureRmDeploymentManagerServiceTopology.md)
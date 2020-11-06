---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: f5e0b1e0b2e85eb3c17a53b0108e853535712db1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491766"
---
# Get-AzureRmDeploymentManagerServiceTopology

## Áttekintés
A szolgáltatás topológiáját kapja.

## SZINTAXISA

### Interaktív (alapértelmezett)
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDeploymentManagerServiceTopology** parancsmag szolgáltatási topológiát kap.

Ezt az objektumot helyileg módosíthatja, majd az Set-AzureRmDeploymentManagerServiceTopology parancsmag használatával alkalmazhatja a módosításokat a topológiára.
Adja meg a szolgáltatás topológiáját a nevével és az erőforrás csoport nevével. Másik lehetőségként megadhatja a ServiceTopology objektumot vagy a ResourceId.

## Példák

### Példa 1
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

Ez a parancs a ContosoServiceTopology nevű szolgáltatási topológiát kapja meg a ContosoResourceGroup.

### 2. példa: a szolgáltatás topológiájának beszerzése az erőforrás-azonosító használatával.
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

Ez a parancs a ContosoServiceTopology nevű szolgáltatási topológiát kapja meg a ContosoResourceGroup.

### 3. példa: a szolgáltatás topológiájának beszerzése a Service topológia objektum használatával.
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

Ez a parancs olyan szolgáltatási topológiát kap, amelynek a neve és a ResourceGroup megegyezik a $serviceTopologyObject neve és ResourceGroupName tulajdonságaival.

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

### -Name (név)
A szolgáltatás topológiájának neve.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Az erőforrás-azonosító.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceTopology
Szolgáltatási topológia erőforrás-objektuma.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

[Új – AzureRmDeploymentManagerServiceTopology](./New-AzureRmDeploymentManagerServiceTopology.md)

[Remove-AzureRmDeploymentManagerServiceTopology](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[Set-AzureRmDeploymentManagerServiceTopology](./Set-AzureRmDeploymentManagerServiceTopology.md)
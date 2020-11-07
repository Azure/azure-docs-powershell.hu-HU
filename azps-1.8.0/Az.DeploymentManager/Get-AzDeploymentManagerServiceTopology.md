---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 54a48a025dff2bba2c1ad620237d0a84aacf7d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671005"
---
# Get-AzDeploymentManagerServiceTopology

## Áttekintés
Megkapja a szolgáltatás topológiáját.

## SZINTAXISA

### Interaktív (alapértelmezett)
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzDeploymentManagerServiceTopology** parancsmag szolgáltatási topológiát kap.

Ezt az objektumot helyileg módosíthatja, majd az Set-AzDeploymentManagerServiceTopology parancsmag használatával alkalmazhatja a módosításokat a topológiára.
Adja meg a szolgáltatás topológiáját a nevével és az erőforrás csoport nevével. Másik lehetőségként megadhatja a ServiceTopology objektumot vagy a ResourceId.

## Példák

### Példa 1
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

Ez a parancs a ContosoServiceTopology nevű szolgáltatási topológiát kapja meg a ContosoResourceGroup.

### 2. példa: a szolgáltatás topológiájának beszerzése az erőforrás-azonosító használatával.
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

Ez a parancs a ContosoServiceTopology nevű szolgáltatási topológiát kapja meg a ContosoResourceGroup.

### 3. példa: a szolgáltatás topológiájának beszerzése a Service topológia objektum használatával.
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

Ez a parancs olyan szolgáltatási topológiát kap, amelynek a neve és a ResourceGroup megegyezik a $serviceTopologyObject neve és ResourceGroupName tulajdonságaival.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -InputObject
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

### -Name (név)
A szolgáltatás topológiájának neve.

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

### -ResourceGroupName
Az erőforráscsoport.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource

## KIMENETEK

### Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: 3dda11ec4fddde67a3ae4300f884290831ac28ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666672"
---
# Get-AzDeploymentManagerService

## Áttekintés
Megkapja a szolgáltatást.

## SZINTAXISA

### Interaktív (alapértelmezett)
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByServiceTopologyObject
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByServiceTopologyResourceId
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzDeploymentManagerService** parancsmag szolgáltatás-topológiában kap egy szolgáltatást, és egy olyan objektumot ad eredményül, amely az adott szolgáltatást jelképezi.
Adja meg a szolgáltatást a nevével, a szolgáltatási topológiával, és az erőforráscsoport nevével. Másik lehetőségként megadhatja a szolgáltatás objektumát vagy a ResourceId.

Ezt az objektumot helyileg is módosíthatja, majd a Set-AzDeploymentManagerService parancsmag használatával alkalmazhatja a módosításokat.

## Példák

### Példa 1
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

Ez a parancs a ContosoService1 nevű szolgáltatást a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában kapja.

### 2. példa: szolgáltatás kérése az erőforrás-azonosítóval
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

Ez a parancs a ContosoService1 nevű szolgáltatást a ContosoResourceGroup ContosoServiceTopology nevű szolgáltatási topológiában kapja.

### 3. példa: szolgáltatás beszerzése a Service objektum használatával.
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

Ez a parancs olyan szolgáltatást kap, amelynek a neve, a szolgáltatás topológiájának neve és a ResourceGroup megegyezik a $serviceObject neve, a ServiceTopologyName és a ResourceGroupName tulajdonságaival.
 

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
Service objektum.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A szolgáltatás neve.

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport.

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
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

### -ServiceTopologyName
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

### -ServiceTopologyObject
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

### -ServiceTopologyResourceId
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource

## KIMENETEK

### Microsoft. Azure. Command. DeploymentManager. models. PSServiceResource

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

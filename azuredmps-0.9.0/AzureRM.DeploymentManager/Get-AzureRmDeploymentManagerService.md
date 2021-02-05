---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4a91c2f8fdda1d2cda7c75f0cf7cfab165701f3d
ms.sourcegitcommit: e57be0da5162efeb0a01f396e2343dd137920063
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/05/2021
ms.locfileid: "99572105"
---
# Get-AzureRmDeploymentManagerService

## SYNOPSIS
Szolgáltatás topológiát kap.

## SZINTAXIS

### Interaktív (alapértelmezett)
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByServiceTopologyObject
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByServiceTopologyResourceId
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzureRmDeploymentManagerService parancsmag** szolgáltatás-topológia alapján kap egy szolgáltatást, és az adott szolgáltatást képviselő objektumot ad vissza.
Adja meg a szolgáltatást a neve, a szolgáltatás topológiája és az erőforráscsoport neve alapján. Másik módon meg is használhatja a Service objektumot vagy az ResourceId objektumot.

Ezt az objektumot helyben módosíthatja, majd a Set-AzureRmDeploymentManagerService alkalmazhatja a szolgáltatásra.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

Ez a parancs egy ContosoService1 nevű szolgáltatást kap a ContosoServiceTopology nevű szolgáltatás topológiában a ContosoResourceGroup csoportban.

### 2. példa: Szolgáltatás lekérte az erőforrás-azonosítót használva.
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

Ez a parancs egy ContosoService1 nevű szolgáltatást kap a ContosoServiceTopology nevű szolgáltatás topológiában a ContosoResourceGroup csoportban.

### 3. példa: Szolgáltatás lekérte a szolgáltatásobjektumot használva.
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

Ez a parancs egy olyan szolgáltatást kap, amelynek a neve, a szolgáltatás topológiája és az Erőforráscsoport neve megegyezik a $serviceObject, ServiceTopologyName és ResourceGroupName tulajdonságaival.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -Name
A szolgáltatás neve.

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Az erőforrás azonosítója.

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

### -Service
Szolgáltatásobjektum.

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

### -ServiceTopology
Az a szolgáltatás topológia objektum, amelyben létre kell hozatni a szolgáltatást.

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

### -ServiceTopologyName
A szolgáltatás-topológia neve.

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

### -ServiceTopologyResourceId
Az a szolgáltatás topológia típusú erőforrás-azonosítója, amelyben létre kell hozatni a szolgáltatást.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzureRmDeploymentManagerService](./New-AzureRmDeploymentManagerService.md)

[Remove-AzureRmDeploymentManagerService](./Remove-AzureRmDeploymentManagerService.md)

[Set-AzureRmDeploymentManagerService](./Set-AzureRmDeploymentManagerService.md)

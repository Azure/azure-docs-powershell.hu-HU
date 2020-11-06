---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 21d0b4f7feec5b32ff732f880924becddd84db73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490696"
---
# Get-AzureRmDeploymentManagerRollout

## Áttekintés
Bevezetést kap.

## SZINTAXISA

### Interaktív (alapértelmezett)
```
Get-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [[-RetryAttempt] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDeploymentManagerRollout** parancsmag bevezetést kap, és egy olyan objektumot ad eredményül, amely a bevezetési folyamat előrehaladásával kapcsolatos részletes információkat tartalmazza.
Adja meg a kiépítést a neve és az erőforráscsoport neve alapján. Felváltva megadhatja a kivezetési objektumot vagy a ResourceId.

## Példák

### Példa 1
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

Ez a parancs beilleszti a ContosoRollout nevű "ContosoResourceGroup" nevű felépítést.

### 2. példa: Bevezetés beszerzése az erőforrás-azonosítóval
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Ez a parancs beilleszti a ContosoRollout nevű "ContosoResourceGroup" nevű felépítést.

### 3. példa: Bevezetés a bevezetési objektum használatával.
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

Ez a parancs olyan kivezetést kap, akinek a neve és a ResourceGroup megegyezik a $rolloutObject neve és ResourceGroupName tulajdonságaival.

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
A bevezetés neve.

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

### -RetryAttempt
A bevezetés kísérlete a bevezetéshez.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bevezetés
Objektum kiépítése

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
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

### Microsoft. Azure. Command. DeploymentManager. models. PSRollout

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Stop-AzureRmDeploymentManagerRollout](./Stop-AzureRmDeploymentManagerRollout.md)

[Újraindítás – AzureRmDeploymentManagerRollout](./Restart-AzureRmDeploymentManagerRollout.md)

[Remove-AzureRmDeploymentManagerRollout](./Remove-AzureRmDeploymentManagerRollout.md)
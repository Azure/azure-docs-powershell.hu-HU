---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 79eeb4e1725adf38b2f1dc70fe181280312fa1e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184227"
---
# Get-AzManagementGroupDeployment

## Áttekintés
Bevezetés beszerzése felügyeleti csoporttal

## SZINTAXISA

### GetByDeploymentName (alapértelmezett)
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzManagementGroupDeployment** parancsmag a központi telepítőket kapja meg a felügyeleti csoportban.
Adja meg a *nevet* vagy az *azonosító* paramétert az eredmények szűréséhez.
A **Get-AzManagementGroupDeployment** alapértelmezés szerint a felügyeleti csoport minden telepített példányát bekapja.

## Példák

### Példa 1: az összes telepített példány beszerzése egy felügyeleti csoportba
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

Ez a parancs a "myMG" felügyeleti csoport minden telepített példányát beilleszti.

### 2. példa: a központi felügyelet beszerzése név alapján
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

Ez a parancs a "Deploy01" bevezetést kapja a "myMG" felügyeleti csoportnál.
A **AzManagementGroupDeployment-** parancsmagok használatával létrehozhatja a kívánt nevet a telepítéshez.
Ha nem rendel nevet, a parancsmagok alapértelmezés szerint a központi telepítéshez használt sablon alapján biztosítják a megfelelő nevet.

### 3. példa: bevezetési azonosító beszerzése
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

Ez a parancs a "Deploy01" bevezetést kapja a "myMG" felügyeleti csoportnál.

## PARAMÉTEREK

### -ApiVersion
Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.
Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
A központi telepítő teljes erőforrás-azonosítója.
Példa:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupId
A kezelési csoport azonosítója.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A központi telepítő neve.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

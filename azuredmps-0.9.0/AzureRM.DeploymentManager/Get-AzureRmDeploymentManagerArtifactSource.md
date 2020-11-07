---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: baf5059d3a952e90422f3e16d83634291aa87614
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671782"
---
# Get-AzureRmDeploymentManagerArtifactSource

## Áttekintés
Egy tárgy forrását kapja.

## SZINTAXISA

### Interaktív (alapértelmezett)
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDeploymentManagerArtifactSource** parancsmag tárgyi forrást kap, és egy olyan objektumot ad eredményül, amely az adott tárgy forrását jelképezi.
Adja meg az tárgy forrását a neve és az erőforrás csoport neve alapján. Másik lehetőségként megadhatja a ArtifactSource objektumot vagy a ResourceId.

Ezt az objektumot helyileg módosíthatja, majd a Set-AzureRmDeploymentManagerArtifactSource parancsmag használatával alkalmazhatja az objektumon végzett módosításokat.

## Példák

### Példa 1: tárgyi forrás beszerzése
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

Ez a parancs a ContosoResourceGroup nevű ContosoArtifactSource nevű tárgyi forrást kapja.

### 2. példa: tárgyi forrás beszerzése az erőforrás-azonosítóval
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

Ez a parancs a ContosoResourceGroup nevű ContosoArtifactSource nevű tárgyi forrást kapja.

### 3. példa: tárgyi forrás beszerzése New-AzureRmDeploymentManagerArtifactSource által visszaadott objektum használatával
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

Ez a parancs olyan tárgyi forrást kap, amelynek a neve és a ResourceGroup megegyezik a $artifactSourceObject neve és ResourceGroupName tulajdonságaival.

## PARAMÉTEREK

### -ArtifactSource
Tárgy forrás objektum.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### -Name (név)
A tárgy forrásának neve.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. DeploymentManager. models. PSArtifactSource

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmDeploymentManagerArtifactSource](./New-AzureRmDeploymentManagerArtifactSource.md)

[Remove-AzureRmDeploymentManagerArtifactSource](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[Set-AzureRmDeploymentManagerArtifactSource](./Set-AzureRmDeploymentManagerArtifactSource.md)
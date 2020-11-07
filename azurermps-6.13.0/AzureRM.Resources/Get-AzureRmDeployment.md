---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeployment.md
ms.openlocfilehash: 6d25bcf98adb740ec695152eb5b27ec9402082c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672584"
---
# Get-AzureRmDeployment

## Áttekintés
A központi telepítő beszerzése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### GetByDeploymentName (alapértelmezett)
```
Get-AzureRmDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzureRmDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRmDeployment** parancsmag a telepített példányokat az aktuális előfizetéses tartományban kapja meg.
Adja meg a *nevet* vagy az *azonosító* paramétert az eredmények szűréséhez.
A **Get-AzureRmDeployment** alapértelmezés szerint az aktuális előfizetési tartomány minden telepített példányát bekapja.

## Példák

### Példa 1: a bevezetések beszerzése az előfizetések hatókörében
```
PS C:\>Get-AzureRmDeployment
```

Ez a parancs a jelenlegi előfizetési tartomány minden telepített példányát beilleszti.

### 2. példa: a központi felügyelet beszerzése név alapján
```
PS C:\>Get-AzureRmDeployment -Name "DeployRoles01"
```

Ez a parancs a DeployRoles01 telepítését az aktuális előfizetési tartományon keresztül kapja meg.
A **AzureRmDeployment-** parancsmagok használatával létrehozhatja a kívánt nevet a telepítéshez.
Ha nem rendel nevet, a parancsmagok alapértelmezés szerint a központi telepítéshez használt sablon alapján biztosítják a megfelelő nevet.

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
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azonosító
A központi telepítő teljes erőforrás-azonosítója.
Példa:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
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
Position: 0
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

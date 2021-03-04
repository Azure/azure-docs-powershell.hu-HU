---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: eb79b6a46f2eaadfc6a42159706c37017cdac8d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937409"
---
# Get-AzResourceGroupDeployment

## SYNOPSIS
Beveszi a telepítéseket egy erőforráscsoportban.

## SZINTAXIS

### GetByResourceGroupDeploymentName (alapértelmezett)
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzResourceGroupDeployment** parancsmag egy Azure-erőforráscsoportban kapja meg a telepítéseket.
Adja meg *a Név* vagy *az Azonosító* paramétert az eredmények szűréséhez.
Alapértelmezés szerint a **Get-AzResourceGroupDeployment** egy adott erőforráscsoport összes telepítését megkapja.
Az Azure-erőforrás egy felhasználó által felügyelt Azure-entitás, például egy adatbázis-kiszolgáló, adatbázis vagy webhely.
Az Azure-erőforráscsoportok egy egységként üzembe helyezett Azure-erőforrások gyűjteményei.
A telepítés az a művelet, amely az erőforráscsoport erőforrásait használatra elérhetővé teszi.
Az Azure-erőforrásokról és az Azure-erőforráscsoportokról a New-AzResourceGroup talál.
Ezt a parancsmagot nyomon követésre használhatja.
Hibakereséshez használja ezt a parancsmagot a Get-AzLog parancsmaggal.

## PÉLDÁK

### 1. példa: Erőforráscsoport összes telepítésének letelepítése
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

Ez a parancs a ContosoLabsRG erőforráscsoport összes központi telepítését beveszi.
A kimenet egy gyűjteménysablont használt WordPress-blog központi telepítését mutatja.

### 2. példa: Telepítés lekérte név szerint
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

Ez a parancs a ContosoLabsRG erőforráscsoport DeployWebsite01 telepítését kapja meg.
A **New-AzResourceGroup** vagy a **New-AzResourceGroupDeployment** parancsmagok használatával nevet rendelhet a telepítéshez.
Ha nem rendel nevet, a parancsmagok az üzembe helyezés létrehozásához használt sablon alapján alapértelmezett nevet biztosítanak.

### 3. példa: Az összes erőforráscsoport telepítésének lekérte
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

Ez a parancs az előfizetés összes erőforráscsoportját begyakorlja a Get-AzResourceGroup parancsmag használatával.
A parancs a folyamat műveleti operátorával átadja az erőforráscsoportokat az aktuális parancsmagnak.
Az aktuális parancsmag begyűszi az előfizetés összes erőforráscsoportját, és átadja az eredményeket a Format-Table-parancsmagnak, hogy megjelenítse a **ResourceGroupName,** **a DeploymentName** és a **ProvisioningState** tulajdonságértékeket.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -Id
A lekért erőforráscsoport-telepítés azonosítója.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
A lekért központi telepítés nevét adja meg.
A helyettesítő karakterek használata nem engedélyezett.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Azt jelzi, hogy ez a parancsmag figyelembe veszi a megjelenés előtt ható API-verziókat, amikor automatikusan meghatározza, hogy melyik verziót kell használni.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Egy erőforráscsoport nevét adja meg.
A parancsmag beállítja a paraméter által megadott erőforráscsoport üzembe helyezését.
A helyettesítő karakterek használata nem engedélyezett.
Ez a paraméter kötelező, és minden parancsban csak egy erőforráscsoport adható meg.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Stop-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Test-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)



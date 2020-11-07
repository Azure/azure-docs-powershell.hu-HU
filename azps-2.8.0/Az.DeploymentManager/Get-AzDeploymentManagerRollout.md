---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: fbcb93ec75dc0e136c1c18743a8686f7642ef02f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666670"
---
# Get-AzDeploymentManagerRollout

## Áttekintés
Megkapja a kiépítést.

## SZINTAXISA

### Interaktív (alapértelmezett)
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzDeploymentManagerRollout** parancsmag bevezetést kap, és egy olyan objektumot ad eredményül, amely a bevezetési folyamat előrehaladásával kapcsolatos részletes információkat tartalmazza.
Adja meg a kiépítést a neve és az erőforráscsoport neve alapján. Felváltva megadhatja a kivezetési objektumot vagy a ResourceId.

A visszaadott bevezetési objektum tartalmazza a telepített szolgáltatásokat, szolgáltatási egységeket és lépéseket, valamint a folyamatban lévőket. Azok, amelyeket még el kell vetni, nem szerepelnek a válaszban.

## Példák

### Példa 1 a kivezetéshez
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

Ez a parancs beilleszti a ContosoRollout nevű "ContosoResourceGroup" nevű felépítést. 

### 2. példa a kivezetési adatok beolvasása és megjelenítése
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

Ez a parancs beilleszti a ContosoRollout nevű "ContosoResourceGroup" nevű felépítést. A-verbose kapcsoló az összes kivezetési részletet hierarchikusan jeleníti meg; a szolgáltatások, a ServiceUnits és az egyes ServiceUnit, valamint a környezetfüggő információk megjelenítése az egyes lépésekhez a bevezetés holisztikus nézete érdekében.

### 3. példa: Bevezetés beszerzése az erőforrás-azonosítóval
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Ez a parancs beilleszti a ContosoRollout nevű "ContosoResourceGroup" nevű felépítést.

### Példa 4: Bevezetés a bevezetési objektum használatával.
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

Ez a parancs olyan kivezetést kap, akinek a neve és a ResourceGroup megegyezik a $rolloutObject neve és ResourceGroupName tulajdonságaival.

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

### -Name (név)
A bevezetés neve.

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

### -RetryAttempt
A bevezetés kísérlete a bevezetéshez.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
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

### System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]

### Microsoft. Azure. Command. DeploymentManager. models. PSRollout

## KIMENETEK

### Microsoft. Azure. Command. DeploymentManager. models. PSRollout

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

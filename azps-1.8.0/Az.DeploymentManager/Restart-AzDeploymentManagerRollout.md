---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: e53f2e72a10befb126bc9cc20dc12bf8990b1553
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670980"
---
# Restart-AzDeploymentManagerRollout

## Áttekintés
Sikertelen bevezetés újraindítása.

## SZINTAXISA

### Interaktív (alapértelmezett)
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az **Újraindítás – AzDeploymentManagerRollout** parancsmag újraindítja a sikertelen bevezetést, és egy olyan objektumot ad eredményül, amely a bevezetési folyamat előrehaladásával kapcsolatos részletes információkat tartalmazza.
Adja meg a kiépítést a neve és az erőforráscsoport neve alapján. Felváltva megadhatja a kivezetési objektumot vagy a ResourceId.
Opcionális paraméter: a SkipSucceeded lehetővé teszi, hogy a bevezetés előző futása során minden követett lépést kiugorjon.

## Példák

### Példa 1
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

Ez a parancs elindítja a ContosoResourceGroup nevű ContosoRollout-bővítményt. A SkipSucceeded jelző azt jelzi, hogy a már sikeresen futtatott összes lépést ki kell hagynia, és a kivezetésnek továbbra is az utolsó sikertelen végrehajtástól kell lépnie.

### 2. példa: a bevezetés újraindítása az erőforrás-azonosítóval
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Ez a parancs elindítja a ContosoResourceGroup nevű ContosoRollout-bővítményt.

### 3. példa: a bevezetés újraindítása a kivezetési objektum használatával.
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

Ez a parancs elindítja a kivezetést, amelynek a neve és a ResourceGroup meg kell egyeznie az $rolloutObject név-és ResourceGroupName tulajdonságaival.

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
Az eltávolítandó erőforrás.

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

### -SkipSucceeded
A bevezetési folyamat előző futásában sikeres lépések elhagyása.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### Microsoft. Azure. Command. DeploymentManager. models. PSRollout

## KIMENETEK

### Microsoft. Azure. Command. DeploymentManager. models. PSRollout

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

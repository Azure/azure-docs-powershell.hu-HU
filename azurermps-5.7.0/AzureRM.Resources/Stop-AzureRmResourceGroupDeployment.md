---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 4cdc70928f2b27ae1e1604c52e5703798a302a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502452"
---
# Stop-AzureRmResourceGroupDeployment

## Áttekintés
Erőforráscsoport-telepítő lemondása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### StopByResourceGroupDeploymentName (alapértelmezett)
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### StopByResourceGroupDeploymentId
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **stop-AzureRmResourceGroupDeployment** parancsmag lemond egy olyan Azure-erőforráscsoport-telepítőt, amely már nem fejeződött be.
Ha meg szeretné szüntetni egy központi üzembe állítást, akkor a bevezetésnek hiányos kitöltési állapottal kell rendelkeznie (például kiépítési vagy sikertelen).

Az Azure-erőforrás egy felhasználó által felügyelt entitás, például webhely, adatbázis vagy adatbázis-kiszolgáló.
Az erőforráscsoport olyan erőforrások gyűjteménye, amelyek egységként települnek.
Erőforráscsoport telepítéséhez használja az New-AzureRmResourceGroupDeployment parancsmagot.

Az New-AzureRmResource parancsmag új erőforrást hoz létre, de nem hoz létre erőforráscsoport-telepítő műveletet, amely a parancsmagot leállíthatja.
Ez a parancsmag csak egy futó központi telepítőt állít le.

Egy adott példány leállításához használja a *Name (név* ) paramétert.
Ha elmulasztja a *Name* paramétert, a **stop-AzureRmResourceGroupDeployment** keres egy futó példányban, és leállítja.
Ha a parancsmag egynél több futó bevezetést talál, a parancs nem hajtható végre.

## Példák

## PARAMÉTEREK

### -ApiVersion
Az erőforrás-szolgáltató által támogatott API-verziót adja meg.
Az alapértelmezett verziótól eltérő verziót is megadhat.

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
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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
A leállításhoz az erőforráscsoport-telepítő AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A leállításhoz az erőforráscsoport-telepítő nevét adja meg.

Ha nem adja meg ezt a paramétert, ez a parancsmag az erőforráscsoport futó példányát keresi, és leállítja.
Ha egynél több futó telepítőt talál, a parancs nem hajtható végre.
A központi telepítő nevének beszerzéséhez használja az Get-AzureRmResourceGroupDeployment parancsmagot.

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.

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

### -ResourceGroupName
Az erőforráscsoport nevét adja meg.
Ez a parancsmag leállítja a paraméter által megadott erőforráscsoport telepítését.

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Logikai

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmResourceGroupDeployment](./Get-AzureRmResourceGroupDeployment.md)

[Új – AzureRmResource](./New-AzureRmResource.md)

[Új – AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Új – AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Remove-AzureRmResourceGroupDeployment](./Remove-AzureRmResourceGroupDeployment.md)

[Teszt-AzureRmResourceGroupDeployment](./Test-AzureRmResourceGroupDeployment.md)



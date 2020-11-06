---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 2282bdef70f6352caa535b4d7a68d5e4046f831e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492186"
---
# Set-AzureRmRoleDefinition

## Áttekintés
Egyéni szerepkör módosítása az Azure RBAC-ban.
A módosított szerepkör definíciójának megadása JSON-fájlként vagy PSRoleDefinition.
Először használja a Get-AzureRmRoleDefinition parancsot a módosítani kívánt egyéni szerepkör beolvasásához.
Ezután módosítsa a módosítani kívánt tulajdonságokat.
Végül mentse a szerepkör-definíciót a parancs segítségével.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### InputFileParameterSet
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A Set-AzureRmRoleDefinition parancsmag egy meglévő egyéni szerepkört frissít az Azure Role-Based Access-vezérlőben.
Adja meg a frissített szerepkör-definíciót a parancshoz JSON-fájlként vagy PSRoleDefinition-objektumként.
A frissített egyéni szerepkör szerepkör-definíciójának tartalmaznia kell a szerepkör azonosítóját és minden egyéb szükséges tulajdonságát, még ha nem is frissítik: DisplayName, leírás, műveletek és AssignableScopes.
A DataActions, a NotDataActions nem kötelező.

Az alábbiakban egy példa frissítve Set-AzureRmRoleDefinition JSON-hoz

{"Azonosító": "52a6cc13-ff92-47a8-a39b-2a8205c3087e"; "név": "frissítve role", "Description": "az összes erőforrás figyelése, és a virtuális gépek indítása és újraindítása", "műveletek": \[ " */READ", "Microsoft. ClassicCompute/virtualmachines/újraindítás/tevékenység", "Microsoft. ClassicCompute/virtualmachines/Start/művelet" \] , "nem tapintatok": \[ "* /Write" \] , "DataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/containers/Blobs/Read", "NotDataActions": \] \[ "Microsoft. Storage/storageAccounts/blobServices/containers/Blobs/Write" \] , \[ \] "AssignableScopes": "/Subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"}

## Példák

### Frissítés a PSRoleDefinitionObject használatával
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### Létrehozás JSON-fájl használatával
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARAMÉTEREK

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

### -InputFile
Annak a fájlnevnek a neve, amely egyetlen JSON szerepkör-definíciót tartalmaz.
Csak a JSON-ban frissítendő tulajdonságokat adja meg.
Szükség van az azonosító tulajdonságra.

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role (szerepkör)
Frissítendő szerepkör-definíciós objektum

```yaml
Type: PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSRoleDefinition
A "role" paraméter értéke az "PSRoleDefinition" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition

## MEGJEGYZI
Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[Új – AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)


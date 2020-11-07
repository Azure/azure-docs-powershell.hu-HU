---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 29be6682c18820a26966cd72997cf54f45db16f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838906"
---
# New-AzRoleDefinition

## Áttekintés
Egyéni szerepkör létrehozása az Azure RBAC-ban.
JSON-Szerepdefiníció vagy PSRoleDefinition-objektum megadása bemenetként.
Első lépésként a Get-AzRoleDefinition parancs segítségével hozzon létre egy eredeti szerepkör-definíciós objektumot.
Ezután szükség szerint módosítsa a tulajdonságait.
Végül ezt a parancsot használva egyéni szerepkört hozhat létre a szerepkör-definícióval.

## SZINTAXISA

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A New-AzRoleDefinition parancsmag egyéni szerepkört hoz létre az Azure Role-Based hozzáférés-vezérlésben.
Adjon meg egy szerepkör-definíciót a parancshoz JSON-fájlként vagy PSRoleDefinition-objektumként.
A beviteli szerepkör definíciójának a következő tulajdonságokat kell tartalmaznia:
1) DisplayName: az egyéni szerepkör neve
2) Leírás: annak a szerepkörnek a rövid leírása, amely összefoglalja a szerepkör által nyújtott hozzáférést.
3) Műveletek: azok a műveletek, amelyekre az egyéni szerepkör hozzáférést biztosít.
Az Azure RBAC-hoz védett Azure Resource Providers műveletek megszerzéséhez használja a Get-AzProviderOperation.
Az alábbiakban néhány érvényes műveleti karakterláncot ismertetünk:
 - a "*/READ" minden Azure Resource Provider olvasási műveletéhez hozzáférést biztosít.
 - A "Microsoft. hálózat/*/Read" a Microsoft. Network Resource szolgáltatója minden erőforrás-típusához hozzáférést biztosít az olvasási műveletekhez.
 - A "Microsoft. számítási/virtualMachines/*" hozzáférést biztosít a virtuális gépek minden műveletéhez és a gyermek erőforrás-típusához.
4) AssignableScopes: azon hatókörök (Azure-előfizetések vagy erőforráscsoportok) halmaza, amelyekben az egyéni szerepkör elérhetővé válik a hozzárendelésekhez.
A AssignableScopes használatával az egyéni szerepkör csak azokat az előfizetéseket és erőforráscsoportokat teszi elérhetővé, amelyeknek szüksége van rá, és nem rendezheti a felhasználói felületet az előfizetések és az erőforráscsoportok többi részében.
A következő érvényes hozzárendelés-hatókörök használhatók:
 - "/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": a szerepkör elérhetővé tétele két előfizetésben.
 - "/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": egyetlen előfizetésben elérhetővé teszi a feladatot.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": a szerepkör elérhetővé tétele csak a hálózati erőforrás csoportban.
A beviteli szerepkör definíciója a következő tulajdonságokat tartalmazhatja:
1) Nem megfelelő: az egyéni szerepkörhöz tartozó hatékony műveletek meghatározására szolgáló műveletek körét.
Ha egy olyan műveletről van szó, amely nem kíván hozzáférést biztosítani egy egyéni szerepkörben, akkor célszerű, ha nem kívánja kizárni a hozzáférést, hanem az összes műveletet nem adja meg, mint az adott műveletet a műveletek során.
2) DataActions: azoknak az adatműveleteknek a halmaza, amelyekhez az egyéni szerepkör hozzáférést ad.
3) NotDataActions: azoknak a műveleteknek a halmazát, amelyeket ki kell zárni a DataActions, és meg kell határozni az egyéni szerepkörhöz tartozó hatékony adatműveleteket.
Ha egy olyan adatműveletről van szó, amely nem kíván hozzáférést adni egy egyéni szerepkörhöz, célszerű a NotDataActions használni, és nem az összes műveletet megadni, mint az adott műveleten kívüli műveletek.
Megjegyzés: Ha egy felhasználóhoz olyan szerepkör van társítva, amely egy olyan szerepkört ad meg, amely egy olyan művelethez van társítva, amelyhez egy másik szerepkör van társítva, akkor a felhasználó a művelet végrehajtását is lehetővé teszi.
A nem megtagadási szabály: egyszerűen célszerű az engedélyezett műveletek halmazát kizárni, ha bizonyos műveleteket ki kell zárni.
A következőkben egy példa JSON szerepkör-definíció ("név") érhető el: "updated role", "Description": "az összes erőforrás figyelése, valamint a virtuális gépek indítása és újraindítása", "műveletek": \[ " */READ", "Microsoft. ClassicCompute/virtualmachines/újraindítás/művelet", "Microsoft. ClassicCompute/virtualmachines/Start/művelet" \] , "nem tapintatok": \[ "* /Write" \] , "DataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/containers/Blobs/Read", "NotDataActions": \] \[ "Microsoft. Storage/storageAccounts/blobServices/containers/Blobs/Write" \] , \[ \] "AssignableScopes": "/Subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"}

## Példák

### Létrehozás a PSRoleDefinitionObject használatával
```
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"
          PS C:\> $role.Id = $null
          PS C:\> $role.Name = "Virtual Machine Operator"
          PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
          PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
          PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
          PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
          PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
          PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
          PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
          PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
          PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
          PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
          PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
          PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
          PS C:\> $role.Actions.Add("Microsoft.Support/*")
          PS C:\> $role.AssignableScopes.Clear()
          PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> New-AzRoleDefinition -Role $role
```

### Létrehozás JSON-fájl használatával
```
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -InputFile
Egyetlen JSON-szerepkört tartalmazó fájlnév

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role (szerepkör)
Szerepkör-definíciós objektum

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleDefinition

## MEGJEGYZI
Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)


---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 73d82366cc0120e057d0c083e7f6da0b3cdebb76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679333"
---
# Set-AzureRmResourceLock

## Áttekintés
Módosítja az erőforrás-zárolást.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### A megadott hatókör zárolása. Alapértelmezett
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Az erőforráscsoport hatókörének zárolása.
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Zárolás az erőforrás-csoport erőforrás-hatókörében.
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Zárolás az előfizetéses hatókörben.
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Zárolás az előfizetés erőforrás-tartományában.
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### A bérlői erőforrás hatókörének zárolása.
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Zárolás, azonosító szerint
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **set-AzureRmResourceLock** parancsmag módosítja az erőforrás-zárolást.

## Példák

### Példa 1: a zárolási megjegyzések frissítése
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

A parancs frissíti a ContosoSiteLock nevű zárolás megjegyzését.

## PARAMÉTEREK

### -ApiVersion
Az erőforrás-szolgáltató API-nak a verziószámát adja meg.
Ha nem ad meg verziót, ez a parancsmag a legújabb elérhető verziót használja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LockId
A parancsmag által módosított zárolás AZONOSÍTÓját adja meg.

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LockLevel
A zárolás szintjét adja meg.
Jelenleg az egyetlen érvényes érték a CanNotDelete.

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LockName
A parancsmag által módosított zárolás nevét adja meg.

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope., A lock at the resource group scope., A lock at the resource group resource scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LockNotes
A zároláshoz kapcsolódó jegyzeteket adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.

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
Annak az erőforráscsoport-csoportnak a neve, amelyhez a zárolás vonatkozik.

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Annak az erőforrásnak a nevét adja meg, amelynek a zárolását alkalmazni kívánja.
Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot: 

Kiszolgálói `/` adatbázis

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
Annak az erőforrásnak a típusa, amelyre a zárolás vonatkozik.

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Scope (hatókör)
Azt a hatókört adja meg, amelyre a zárolás vonatkozik.
Ha például egy adatbázist szeretne megadni, használja az alábbi formátumot: 

`/subscriptions/`előfizetés-azonosító erőforrás-kiszolgálócsoport neve- `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` adatbázis neve

Erőforráscsoport megadásához használja a következő formátumot: 

`/subscriptions/`előfizetés-azonosító `/resourceGroups/` Erőforrás-csoport neve

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantLevel
Jelzi, hogy ez a parancsmag a bérlői szinten működik.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### System. Management. Automation. PSObject

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmResourceLock](./Get-AzureRmResourceLock.md)

[Új – AzureRmResourceLock](./New-AzureRmResourceLock.md)

[Remove-AzureRmResourceLock](./Remove-AzureRmResourceLock.md)



---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 9d65ed2f6bbc2e26c4e91916cc42bf2954c08252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672195"
---
# Set-AzureRmADUser

## Áttekintés
Frissít egy meglévő Active Directory-felhasználót.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
Frissít egy meglévő Active Directory-felhasználó (munkahelyi/iskolai fiók is ismert, mint a szervezeti azonosító).
További információ: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser

## Példák

### Példa 1
```
PS C:\> {{ Add example code here }}
```

{{A példa leírása itt}}

## PARAMÉTEREK

### -DisplayName
A felhasználó címjegyzékében megjelenítendő új név.
Példa – 'Alex Wu '.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableAccount
True a fiók engedélyezéséhez; egyéb esetben false.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceChangePasswordNextLogin
A jelszót csak a jelszó frissítésekor kell megadni.
Egyéb esetben a program figyelmen kívül hagyja.
Meg kell adni, ha a felhasználónak módosítania kell a jelszavát a következő sikeres bejelentkezéskor (igaz).
Az alapértelmezett viselkedés (hamis) a következő sikeres bejelentkezéskor nem módosíthatja a jelszót.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Jelszó
Új jelszó a felhasználó számára.
Meg kell felelnie a bérlő jelszó-bonyolultsági követelményeinek.
Ajánlott egy erős jelszó beállítása.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UPNOrObjectId
A felhasználó egyszerű felhasználóneve (például ' someuser@contoso.com ') vagy annak a felhasználónak a objectId, akinek a tulajdonságokat frissíteni kell.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmADUser](./Get-AzureRmADUser.md)

[Új – AzureRmADUser](./New-AzureRmADUser.md)

[Remove-AzureRmADUser](./Remove-AzureRmADUser.md)


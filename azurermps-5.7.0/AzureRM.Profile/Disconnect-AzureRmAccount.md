---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e72e326fd3251a9b3150b9def06e2fb60afb7d82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679728"
---
# Disconnect-AzureRmAccount

## Áttekintés
Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókkal társított összes hitelesítő adatot és kontextust.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ContextName (alapértelmezett)
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UserId
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipal
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ContextObject
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A Disconnect-AzureRmAccount parancsmag leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókhoz társított összes hitelesítő adatokat és kontextust (előfizetés és bérlői információk).

A parancsmag végrehajtása után ismét be kell jelentkeznie a Connect-AzureRmAccount.

## Példák

### Az aktuális fiók kijelentkezése
```
PS C:\> Disconnect-AzureRmAccount
```

Kijelentkezik az aktuális környezethez társított Azure-fiókból.

### Egy adott környezethez társított fiók kijelentkezése
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

Kinaplózza a megadott környezethez tartozó fiókot ("munka"). Mivel ez a "CurrentUser" hatókört használja, a hitelesítő adatokat és a környezeteket véglegesen törli a rendszer.

### Adott felhasználó kijelentkezése
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

Kiszűri a user1@contoso.org felhasználó összes hitelesítő adatait és a felhasználóhoz tartozó összes kontextust.

## PARAMÉTEREK

### -ApplicationId
ServicePrincipal-azonosító (globálisan egyedi azonosító)

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureContext
Összefüggésben

```yaml
Type: PSAzureContext
Parameter Sets: ContextObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ContextName
A kijelentkezni kívánt környezet neve

```yaml
Type: String
Parameter Sets: ContextName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés

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

### -InputObject
Az eltávolítandó fiók objektuma

```yaml
Type: PSAzureRmAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Scope (hatókör)
Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bérlői azonosító megkeresése
Bérlői azonosító (globálisan egyedi azonosító)

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Felhasználónév
Az űrlap felhasználójának neve user@contoso.org

```yaml
Type: String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem hajtható végre.

```yaml
Type: SwitchParameter
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

### Microsoft. Azure. Command. profil. models. PSAzureRmAccount

### Microsoft. Azure. Command. profil. models. PSAzureContext

## KIMENETEK

### Microsoft. Azure. Command. profil. models. PSAzureRmAccount

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

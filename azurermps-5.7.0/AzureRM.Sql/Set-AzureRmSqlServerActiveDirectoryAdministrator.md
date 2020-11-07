---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 43dbbe6ca4f24e98bcfc45703c387ccb5fb4db03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672508"
---
# Set-AzureRmSqlServerActiveDirectoryAdministrator

## Áttekintés
Az SQL Server Azure AD-rendszergazdája.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureRmSqlServerActiveDirectoryAdministrator** parancsmag a jelenlegi előfizetésben az Azure Active Directoryt (Azure ad) kezelőt, az AzureSQL Servert.

Egyszerre csak egy rendszergazda állíthat elő.

Az Azure AD következő tagjai kioszthatók SQL Server-rendszergazdaként:

- Az Azure AD natív tagjai 
- Az Azure AD szövetséges tagjai 
- Importált tagok más Azure-hirdetésekből, akik natív vagy szövetséges tagok 
- Biztonsági csoportként létrehozott Azure AD-csoportok

A Microsoft-fiókok, például a Outlook.com, a Hotmail.com vagy a Live.com tartományok nem támogatottak rendszergazdáknak.
A többi vendégfiók, például a Gmail.com vagy a Yahoo.com tartománya nem támogatott rendszergazdáknak.

Azt javasoljuk, hogy rendszergazdaként hozza létre a dedikált Azure AD-csoportot.

## Példák

### 1. példa: rendszergazdai csoport létesítése a kiszolgálón
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

Ez a parancs a Server01 nevű DBA nevű Azure AD Administrator nevű csoportra vonatkozó szabályokat AD meg.
Ez a kiszolgáló az erőforráscsoport ResourceGroup01 van társítva.

### 2. példa: rendszergazdai felhasználó létesítése a kiszolgálón
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

Ez a parancs az Azure AD-felhasználót rendszergazdaként használja a Server01 nevű kiszolgálón.

### 3. példa: rendszergazdai csoport létesítése az azonosító megadásával
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

Ez a parancs a Server01 nevű DBA nevű Azure AD Administrator nevű csoportra vonatkozó szabályokat AD meg.
A parancs a *ObjectId* paraméter azonosítóját adja meg.
Ez gondoskodik arról, hogy a parancs akkor is sikeres legyen, ha a csoport megjelenítendő neve nem egyedi.

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

### -DisplayName
Annak az Azure AD administratornak a megjelenítendő nevét adja meg, amely a parancsmag rendelkezésére áll.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Annak az Azure AD Administrator-nek az egyedi AZONOSÍTÓját adja meg, amely a parancsmag rendelkezésére áll.
Ha a megjelenítendő név nem egyedi, akkor ehhez a paraméterhez meg kell adnia egy értéket.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kiszolgálónév
Annak az SQL-kiszolgálónak a neve, amelyhez a parancsmag a rendszergazda rendelkezésére áll.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. Command. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmSqlServerActiveDirectoryAdministrator](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[Remove-AzureRmSqlServerActiveDirectoryAdministrator](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)



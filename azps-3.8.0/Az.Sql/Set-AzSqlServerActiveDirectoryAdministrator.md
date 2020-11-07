---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: fddefaf27d1e5b481bd90058739d472d7c793a88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846562"
---
# Set-AzSqlServerActiveDirectoryAdministrator

## Áttekintés
Az SQL Server Azure AD-rendszergazdája.

## SZINTAXISA

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [[-IsAzureADOnlyAuthentication] <Boolean>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzSqlServerActiveDirectoryAdministrator** parancsmag a jelenlegi előfizetésben az Azure Active Directoryt (Azure ad) kezelőt, az AzureSQL Servert.
Egyszerre csak egy rendszergazda állíthat elő.
Az Azure AD következő tagjai kioszthatók SQL Server-rendszergazdaként:
- Az Azure AD natív tagjai 
- Az Azure AD szövetséges tagjai 
- Importált tagok más Azure-hirdetésekből, akik natív vagy szövetséges tagok 
- A biztonsági csoportokba létrehozott Azure-HIRDETÉSCSOPORTOK Microsoft-fiókjai (például az Outlook.com, a Hotmail.com vagy a Live.com tartományban) nem használhatók rendszergazdáknak.
A többi vendégfiók, például a Gmail.com vagy a Yahoo.com tartománya nem támogatott rendszergazdáknak.
Azt javasoljuk, hogy rendszergazdaként hozza létre a dedikált Azure AD-csoportot.

## Példák

### 1. példa: rendszergazdai csoport létesítése a kiszolgálón
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

Ez a parancs a Server01 nevű DBA nevű Azure AD Administrator nevű csoportra vonatkozó szabályokat AD meg.
Ez a kiszolgáló az erőforráscsoport ResourceGroup01 van társítva.

### 2. példa: rendszergazdai felhasználó létesítése a kiszolgálón
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

Ez a parancs az Azure AD-felhasználót rendszergazdaként használja a Server01 nevű kiszolgálón.

### 3. példa: rendszergazdai csoport létesítése az azonosító megadásával
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

Ez a parancs a Server01 nevű DBA nevű Azure AD Administrator nevű csoportra vonatkozó szabályokat AD meg.
A parancs a *ObjectId* paraméter azonosítóját adja meg.
Ez gondoskodik arról, hogy a parancs akkor is sikeres legyen, ha a csoport megjelenítendő neve nem egyedi.

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

### -DisplayName
Annak az Azure AD administratornak a megjelenítendő nevét adja meg, amely a parancsmag rendelkezésére áll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IsAzureADOnlyAuthentication
Annak megadása, hogy engedélyezve van-e csak az Azure Active Directory-hitelesítés.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Annak az Azure AD Administrator-nek az egyedi AZONOSÍTÓját adja meg, amely a parancsmag rendelkezésére áll.
Ha a megjelenítendő név nem egyedi, akkor ehhez a paraméterhez meg kell adnia egy értéket.

```yaml
Type: System.Guid
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
Type: System.String
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
Type: System.String
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

### System. GUID

## KIMENETEK

### Microsoft. Azure. Command. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzSqlServerActiveDirectoryAdministrator](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[Remove-AzSqlServerActiveDirectoryAdministrator](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[Disable-AzSqlServerActiveDirectoryOnlyAuthentication](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: d450fa7795a530106a72180210d9cb133c7d3047
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209183"
---
# Set-AzSqlServerActiveDirectoryAdministrator

## SYNOPSIS
Azure AD-rendszergazdát hoz létre az SQL Serverhez.

## SZINTAXIS

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzSqlServerActiveDirectoryAdministrator** parancsmag az AzureSQL Server Azure Active Directory -rendszergazdáját használja a jelenlegi előfizetésben.
Egyszerre csak egy rendszergazda létesíthet.
Az Azure AD következő tagjait lehet SQL Server-rendszergazdaként kiépítni:
- Az Azure AD natív tagjai 
- Az Azure AD összevont tagjai 
- Importált tagok más Azure AD-ről, akik natív vagy összevont tagok 
- A Microsoft-fiókokként létrehozott Azure AD-csoportok , például a Outlook.com-, Hotmail.com- Live.com- vagy Live.com-fiókok, nem támogatottak rendszergazdákként.
Más vendégfiókok, például a Gmail.com vagy Yahoo.com tartományában található fiókok, nem támogatottak rendszergazdaként.
Azt javasoljuk, hogy rendszergazdaként kiépítsen egy dedikált Azure AD-csoportot.

## PÉLDÁK

### 1. példa: Rendszergazdai csoport kiépítése egy kiszolgálóhoz
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

Ez a parancs egy DBAs nevű Azure AD-rendszergazdai csoportot hoz létre a Server01 nevű kiszolgálóhoz.
Ez a kiszolgáló az ResourceGroup01 erőforráscsoporthoz van társítva.

### 2. példa: Rendszergazdai felhasználó kiépítése egy kiszolgálóhoz
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

Ez a parancs az Azure AD-felhasználót a Server01 nevű kiszolgáló rendszergazdájának nevezi el.

### 3. példa: Rendszergazdai csoport kiépítése az azonosító megadásával
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

Ez a parancs egy DBAs nevű Azure AD-rendszergazdai csoportot hoz létre a Server01 nevű kiszolgálóhoz.
A parancs megadja az *ObjectId paraméter azonosítóját.*
Ez akkor is sikeres lesz, ha a csoport megjelenítendő neve nem egyedi.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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
Annak az Azure AD-rendszergazdának a megjelenítendő nevét adja meg, amelyről ez a parancsmag el van ásva.

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

### -ObjectId
Az Azure AD-rendszergazda egyedi azonosítóját adja meg, amely szerint ez a parancsmag ki van ásva.
Ha a megjelenítendő név nem egyedi, meg kell adnia egy értéket ehhez a paraméterhez.

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
Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.

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

### -ServerName
Annak az SQL Servernek a nevét adja meg, amelyhez a parancsmag rendszergazdai jogosultságot ad.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Guid

## KIMENETEK

### Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzSqlServerActiveDirectoryAdministrator](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[Remove-AzSqlServerActiveDirectoryAdministrator](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[Disable-AzSqlServerActiveDirectoryOnlyAuthentication](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)



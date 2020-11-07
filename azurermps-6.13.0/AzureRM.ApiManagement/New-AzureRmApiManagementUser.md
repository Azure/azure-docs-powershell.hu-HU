---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 1c8b7f8069c63d18f69285f7e40ac4d652f0bf73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672497"
---
# New-AzureRmApiManagementUser

## Áttekintés
Új felhasználó regisztrálása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmApiManagementUser** parancsmag új felhasználót regisztrál.

## Példák

### 1. példa: új felhasználó regisztrálása
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

Ez a parancs egy új, Patti Fuller nevű felhasználót regisztrál.

## PARAMÉTEREK

### -Környezet
Egy **PsApiManagementContext** -objektumot ad meg.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### – E-mail
A felhasználó e-mail-címét adja meg.

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

### -Vezetéknév
A felhasználó vezetéknevét adja meg.
A paraméternek 1 – 100 karakter hosszúnak kell lennie.

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

### -Vezetéknév
A felhasználó vezetéknevét adja meg.
A paraméternek 1 – 100 karakter hosszúnak kell lennie.

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

### -Megjegyzés
A felhasználó megjegyzését adja meg.
Ez a paraméter nem kötelező.
Az alapértelmezett érték $Null.

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

### -Jelszó
Megadja a felhasználó jelszavát.
Ehhez a paraméterhez szükség van.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State (állami)
A felhasználói állapotot adja meg.
Ez a paraméter nem kötelező.
A paraméter alapértelmezett értéke $Null.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserId
A felhasználói azonosítót adja meg.
Ez a paraméter nem kötelező.
Ha ez a paraméter nincs megadva, a parancsmag létrehoz egy felhasználói azonosítót.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext

### System. String

### System. Security. SecureString

### System. null ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementUserState, Microsoft. Azure. commands. ApiManagement. ServiceManagement, Version = 6.1.0.0

## KIMENETEK

### Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmApiManagementUser](./Get-AzureRmApiManagementUser.md)

[Set-AzureRmApiManagementUser](./Set-AzureRmApiManagementUser.md)



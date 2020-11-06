---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d0efe107f15cf3e2bcb0d25c283fee306eeb404b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493242"
---
# Get-AzureRmEnrollmentAccount

## Áttekintés
Tanúsítványigénylési fiókok beszerzése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Egyetlen
```
Get-AzureRmEnrollmentAccount -ObjectId <System.String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmEnrollmentAccount** parancsmag tanúsítványigénylési fiókokat kap.

## Példák

### Példa 1
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

Az összes rendelkezésre álló tanúsítványigénylő fiók beszerzése.

### 2. példa
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

A megadott objektumazonosító beszerzése az igénylési fiókból

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

### -ObjectId
ObjectId egy adott tanúsítványigénylési fiókból.

```yaml
Type: System.String
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. számlázás. models. PSEnrollmentAccount, Microsoft. Azure. commands. számlázás, verzió = 0.14.0.0, Culture = semleges, PublicKeyToken = null]]
Microsoft. Azure. commands. számlázás. modellek. PSEnrollmentAccount

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK


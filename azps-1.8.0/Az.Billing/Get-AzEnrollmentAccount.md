---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d76797f82a14c8efa2f9a3d6a77436fa2f8a1b68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671443"
---
# Get-AzEnrollmentAccount

## Áttekintés
Tanúsítványigénylési fiókok beszerzése

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Egyetlen
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzEnrollmentAccount** parancsmag tanúsítványigénylési fiókokat kap.

## Példák

### Példa 1
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

Az összes rendelkezésre álló tanúsítványigénylő fiók beszerzése.

### 2. példa
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

A megadott objektumazonosító beszerzése az igénylési fiókból

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

### -ObjectId
ObjectId egy adott tanúsítványigénylési fiókból.

```yaml
Type: System.String
Parameter Sets: Single
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

### Microsoft. Azure. commands. számlázás. modellek. PSBillingPeriod

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: d075c6792134536be84643d51f37b2379b63d5e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836298"
---
# Get-AzDataLakeStoreTrustedIdProvider

## Áttekintés
A megadott adattárolóban kapja meg a megadott megbízható identitás-szolgáltatót.
Ha nem ad meg szolgáltatót, akkor a fiók összes szolgáltatóját listázhatja.

## SZINTAXISA

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzDataLakeStoreTrustedIdProvider** parancsmag a megadott adattó-tárolóban kapja meg a megadott megbízható identitás-szolgáltatót.
Ha nem ad meg szolgáltatót, akkor a fiók összes szolgáltatóját listázhatja.

## Példák

### 1. példa: konkrét megbízható identitás-szolgáltató beszerzése
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

A "MyProvider" nevű szolgáltatót számítja ki a "ContosoADL" fiókból.

### 2. példa: a fiók összes szolgáltatójának listázása
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

A "ContosoADL" fiók alatti összes szolgáltató felsorolása

## PARAMÉTEREK

### -Fiók
Az adattó-tároló fiók a megbízható identitás-szolgáltató beolvasásához

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Name (név)
A lekérdezni kívánt megbízható identitás-szolgáltató neve

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnek a neve, amely alatt a megadott fiók megadott megbízható identitás-szolgáltatóját be szeretné olvasni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreTrustedIdProvider

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

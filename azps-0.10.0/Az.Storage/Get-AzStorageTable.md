---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: 1d06b0934306779d0f8266c24c81810de77b3389
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843046"
---
# Get-AzStorageTable

## Áttekintés
A tárolási táblák listája.

## SZINTAXISA

### Táblanév (alapértelmezett)
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzStorageTable** parancsmag az Azure-beli tárterület-fiókkal társított tárolási táblákat sorolja fel.

## Példák

### 1. példa: az összes Azure Storage Table listázása
```
PS C:\>Get-AzStorageTable
```

Ez a parancs a tárterület-fiókok minden tárolási tábláját beilleszti.

### 2. példa: az Azure Storage Tables listázása helyettesítő karakterrel
```
PS C:\>Get-AzStorageTable -Name table*
```

Ez a parancs egy helyettesítő karaktert használ az olyan tárolási táblák beszerzéséhez, amelyek neve táblázattal kezdődik.

### 3. példa: az Azure Storage Tables listázása táblanév előtaggal
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

Ez a parancs az *előtag* paraméterrel olyan tárolási táblákat kap, amelyeknek a neve táblázattal kezdődik.

## PARAMÉTEREK

### -Környezet
A tárolási környezetet adja meg.
A létrehozáshoz használhatja az New-AzStorageContext parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Name (név)
A táblázat nevét adja meg.
Ha a táblázat neve üres, a parancsmag felsorolja az összes táblázatot.
Ellenkező esetben az összes olyan táblát felsorolja, amely megfelel a megadott névnek vagy a normál név mintának.

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
A bekapni kívánt tábla vagy táblák nevében használt előtagot adja meg.
Ezzel az eszközzel megkeresheti az összes olyan táblát, amely ugyanazzal a karakterlánccal kezdődik, mint amilyen például a táblázat.

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext

## KIMENETEK

### Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageTable

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzStorageTable](./New-AzStorageTable.md)

[Remove-AzStorageTable](./Remove-AzStorageTable.md)



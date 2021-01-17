---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: b056504786d641d137d5188ed529eecb0ede690f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324795"
---
# New-AzStorageContainer

## SYNOPSIS
Létrehoz egy Azure-tárolót.

## SZINTAXIS

```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzStorageContainer** parancsmag létrehoz egy Azure-tárolót.

## PÉLDÁK

### 1. példa: Azure-tároló létrehozása
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

Ez a parancs egy tárolótárolót hoz létre.

### 2. példa: Több Azure-tároló létrehozása
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

Ez a példa több tárolót hoz létre.
A  **.NET-karakterláncosztály Felosztás** metódusát használja, majd átadja a neveket a folyamatnak.

## PARAMETERS

### -ClientTimeoutPerRequest
Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.
Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.
Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Megadja a maximális párhuzamos hálózati hívásokat.
Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.
A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.
Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.
Az alapértelmezett érték 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Környezet
Megadja az új tároló környezetét.

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
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Az új tároló nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Engedély
A tárolóhoz való nyilvános hozzáférés szintjét határozza meg.
Alapértelmezés szerint a tároló és a benne lévő blobok csak a tárfiók tulajdonosa által érhetők el.
Ha névtelen felhasználóknak szeretné olvasási engedélyeket beállítani egy tárolóhoz és blobjaikhoz, a tároló engedélyeinek beállításával engedélyezheti a nyilvános hozzáférést.
A névtelen felhasználók a kérés hitelesítése nélkül olvashatják a blobokat egy nyilvánosan elérhető tárolóban.
A paraméter elfogadható értékei a következőek:
- Tároló.
Teljes olvasási hozzáférést biztosít a tárolókhoz és a blobjaikhoz.
Az ügyfelek névtelen kérésen keresztül számba tudják venni a tárolóban lévő blobokat, de a tárfiókban lévő tárolókat nem. 
- Blob.
Olvasási hozzáférést biztosít a blobadatokhoz a teljes tárolóban névtelen kérésen keresztül, de nem biztosít hozzáférést a tárolóadatokhoz.
Az ügyfelek névtelen kérésekkel nem tudnak blobokat számozni a tárolóban. 
- Kikapcsolva.
Ez csak a tárfiók tulajdonosára korlátozza a hozzáférést.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
A szolgáltatás időkorrekta-intervallumát adja meg másodpercben egy kéréshez.
Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext

## KIMENETEK

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStorageContainer](./Get-AzStorageContainer.md)

[Remove-AzStorageContainer](./Remove-AzStorageContainer.md)

[Set-AzStorageContainerAcl](./Set-AzStorageContainerAcl.md)



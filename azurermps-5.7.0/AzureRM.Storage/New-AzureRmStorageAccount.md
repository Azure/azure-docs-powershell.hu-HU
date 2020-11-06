---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 1b00930332d9f3f5a78e4cfe8ab7478a5dc5fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502320"
---
# New-AzureRmStorageAccount

## Áttekintés
Tároló fiókot hoz létre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmStorageAccount** parancsmag egy Azure Storage-fiókot hoz létre.

## Példák

### Példa 1: tárterület-fiók létrehozása
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS"
```

Ez a parancs létrehoz egy tárolási fiókot az erőforráscsoport neve MyResourceGroup.

### 2. példa: a tárterület-titkosítást használó blob-tárolási fiók létrehozása
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

A parancs létrehoz egy blob-tároló fiókot, amely a forró hozzáférési típust használja.
A fiók engedélyezte a tárterület-titkosítást a blob-szolgáltatásban.

### 3. példa: hozzon létre egy olyan tárolási fiókot, amely lehetővé teszi a tárterület-titkosítást a blob-és Fájlszolgáltatások számára, valamint létrehozhatja és hozzárendelheti az identitást az Azure-rendszerhez.
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

Ez a parancs létrehoz egy olyan tárolási fiókot, amely lehetővé tette a tárterület-titkosítást a blob és a Fájlszolgáltatások számára.  Egy identitást hoz létre, és hozzárendel egy olyan identitást, amellyel az Azure-kulccsal kezelheti a fiókok kulcsait.

## PARAMÉTEREK

### -AccessTier
A parancsmag által létrehozott tárolási fiók hozzáférési rétegét adja meg.
A paraméter elfogadható értékei a következők: meleg és hűvös.

Ha a BlobStorage értékét adja meg a *Kind* paraméterhez, meg kell adnia a *AccessTier* paraméter értékét.

Ha *a tárterület* értékére vonatkozó értéket ad meg, ne adja meg a *AccessTier* paramétert.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignIdentity
Új tárolási fiók identitásának létrehozása és hozzárendelése ehhez a tárterülethez a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használathoz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDomainName
A tárolási fiók egyéni tartományának nevét adja meg.
Az alapértelmezett érték a tárterület.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableEncryptionService
Azt jelzi, hogy ez a parancsmag engedélyezi-e a tárterület-titkosítási szolgáltatást a tárterületen.
Az Azure Blob és az Azure file Services támogatott.

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Azt jelzi, hogy a tárolási fiók csak HTTPS-forgalmat engedélyez-e.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kind
A parancsmag által létrehozott tárolási fiók típusát adja meg.
A paraméter elfogadható értékei a következők:

- Tárterület.
Általános célú tárolási fiók, amely támogatja a Blobs, a táblázatok, a várólisták, a fájlok és a lemezek tárolását.

- BlobStorage.
BLOB-tároló fiók, amely támogatja a BLOB-tárolót.


Az alapértelmezett érték a tárterület.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
A létrehozandó tárterület-fiók helyét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A létrehozandó tárterület-fiók nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforrás-csoportnak a nevét adja meg, amelybe a tárolási fiókot hozzá szeretné adni.

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

### -SkuName
Megadja annak a tárolási fióknak az SKU-nevét, amelyet a parancsmag hoz létre.
A paraméter elfogadható értékei a következők:

- Standard_LRS.
Helyileg redundáns tárterület.
- Standard_ZRS.
Zóna – redundáns tárterület.
- Standard_GRS.
Geo-redundáns tárterület.
- Standard_RAGRS.
Olvassa el az Access geo-redundáns tárterülete című témakört.
- Premium_LRS.
Prémium lokálisan redundáns tárterület.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
Ha a BlobStorage értékét adja meg a *Kind* paraméterhez, meg kell adnia a *AccessTier* paraméter értékét.

Ha *a tárterület* értékére vonatkozó értéket ad meg, ne adja meg a *AccessTier* paramétert.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseSubDomain
Azt jelzi, hogy engedélyezi-e a közvetlen CName érvényesítést.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmStorageAccount](./Get-AzureRmStorageAccount.md)

[Remove-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)

[Set-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)

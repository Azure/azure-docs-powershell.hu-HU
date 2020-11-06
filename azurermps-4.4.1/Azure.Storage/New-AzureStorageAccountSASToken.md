---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 8b280a13e7eb7a2e6ea3f52b4a121f313504b2ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492643"
---
# New-AzureStorageAccountSASToken

## Áttekintés
Ügyfél szintű SAS-tokent hoz létre.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Leírás
A **New-AzureStorageSASToken** parancsmag létrehoz egy ügyfél szintű megosztott hozzáférés-aláírási (SAS) jogkivonatot egy Azure-tárterülethez.

A SAS-tokent használhatja több szolgáltatás engedélyeinek meghatalmazására, illetve a szolgáltatások engedélyeinek meghatalmazására, ha az objektum szintű SAS-tokent használja.

## Példák

### Példa 1: egy fiók szintű SAS-token létrehozása teljes hozzáféréssel
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

A parancs teljes hozzáféréssel létrehoz egy fiók szintű SAS-jogkivonatot.

### 2. példa: fiók szintű SAS-token létrehozása IP-címekhez
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

Ez a parancs egy fiók szintű SAS-jogkivonatot hoz létre a HTTPS-only kérelmekhez a megadott IP-címtartományból.

## PARAMÉTEREK

### -Környezet
Az Azure tárolási környezetét adja meg.
A New-AzureStorageContext parancsmaggal **AzureStorageContext** -objektumokat lehet kikeresni.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExpiryTime
Azt az időpontot adja meg, amikor a megosztott elérési aláírás érvénytelenné válik.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressOrRange
Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.
A tartomány bezárólag.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Engedély
A tárolási fiók engedélyei.
Az engedélyek csak akkor érvényesek, ha megfelelnek a megadott erőforrás-típusnak.
Az elfogadható jogosultsági értékekről további információt a fiók-SAS létrehozása című témakörben talál.https://go.microsoft.com/fwlink/?LinkId=799514

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Annak a protokollnak a használatát adja meg, amely a biztonsági fiókkezelő fiókkal végzett kéréshez engedélyezve van.
A paraméter elfogadható értékei a következők:

- HttpsOnly
- HttpsOrHttp

Az alapértelmezett érték a HttpsOrHttp.

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
A SAS-tokenhez elérhető erőforrás-típusokat adja meg.
A paraméter elfogadható értékei a következők:

- Nincs
- Szolgáltatás
- Konténer
- Objektum

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Szolgáltatás
A szolgáltatást adja meg.
A paraméter elfogadható értékei a következők:

- Nincs
- BLOB
- Fájl
- Várólista
- Táblázat

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kezdő időpont
Itt adhatja meg **datetime** -objektumként az időt, amelyen a biztonsági társítás érvényes lesz.
A **datetime** objektum beszerzéséhez használja az Get-Date parancsmagot.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### IStorageContext

A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről

## KIMENETEK

### System. String

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorageBlobSASToken](./New-AzureStorageBlobSASToken.md)

[Új – AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)

[Új – AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)

[Új – AzureStorageQueueSASToken](./New-AzureStorageQueueSASToken.md)

[Új – AzureStorageShareSASToken](./New-AzureStorageShareSASToken.md)

[Új – AzureStorageTableSASToken](./New-AzureStorageTableSASToken.md)



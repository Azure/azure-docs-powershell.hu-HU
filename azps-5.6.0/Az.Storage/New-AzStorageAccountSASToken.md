---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 6d399c7ed7c074cd5adaf0579097c0706f46192d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002613"
---
# New-AzStorageAccountSASToken

## SYNOPSIS
Létrehoz egy fiókszintű SAS-jogkivonatot.

## SZINTAXIS

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzStorageSASToken** parancsmag létrehoz egy fiókszintű megosztott hozzáférés-aláírást (SAS) egy Azure Storage-fiókhoz.
Az SAS-jogkivonattal delegálhatja több szolgáltatás engedélyét, illetve delegálhatja az objektumszintű SAS-jogkivonattal nem elérhető szolgáltatások engedélyét.

## PÉLDÁK

### 1. példa: Fiókszintű SAS-jogkivonat létrehozása teljes engedéllyel
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

Ez a parancs létrehoz egy fiókszintű SAS-jogkivonatot teljes engedéllyel.

### 2. példa: Fiókszintű SAS-jogkivonat létrehozása IP-címek tartományhoz
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

Ez a parancs létrehoz egy fiókszintű SAS-jogkivonatot a https-only kérések számára a megadott IP-címtartományból.

## PARAMETERS

### -Környezet
Az Azure-tárterület környezetét határozza meg.
A New-AzStorageContext segítségével **azureStorageContext objektumot** is be tud szerezni.

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

### -ExpiryTime
Azt az időt adja meg, amikor a megosztott hozzáférés aláírása érvénytelenné válik.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressOrRange
Megadja azt az IP-címet vagy IP-címtartományt, amelyből a kérelmeket el kell fogadni( például 168.1.5.65 vagy 168.1.5.60-168.1.5.70.
A tartomány magában foglalja a teljes tartományt is.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Engedély
A Tárfiók engedélyeinek megadása.
Az engedélyek csak akkor érvényesek, ha megfelelnek a megadott erőforrástípusnak.
Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).
Az elfogadható engedélyértékekkel kapcsolatos további információkért lásd: Account SAS létrehozása http://go.microsoft.com/fwlink/?LinkId=799514

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
A fiók SAS-hez való kérése esetén engedélyezett protokollt adja meg.
A paraméter elfogadható értékei a következőek:
- HttpsOnly
- HttpsOrHttp Az alapértelmezett érték a httpsOrHttp.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
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
Megadja az SAS-jogkivonattal elérhető erőforrástípusokat.
A paraméter elfogadható értékei a következőek:
- Nincs
- Szolgáltatás
- Tároló
- Objektum

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Service
A szolgáltatást határozza meg.
A paraméter elfogadható értékei a következőek:
- Nincs
- Blob
- Fájl
- Várólistán
- Táblázat

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Azt az időpontot adja meg **DateTime-objektumként,** amikorra az SAS érvényes lesz.
**DateTime-objektum** betöltéshez használja a Get-Date parancsmagot.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext

## KIMENETEK

### System.String

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzStorageBlobSASToken](./New-AzStorageBlobSASToken.md)

[New-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)

[New-AzStorageFileSASToken](./New-AzStorageFileSASToken.md)

[New-AzStorageQueueSASToken](./New-AzStorageQueueSASToken.md)

[New-AzstorageSharesASToken](./New-AzStorageShareSASToken.md)

[New-AzstorageTableSASToken](./New-AzStorageTableSASToken.md)



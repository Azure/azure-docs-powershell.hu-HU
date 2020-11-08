---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015515"
---
# New-AzureStorSimpleNetworkConfig

## Áttekintés
Hálózati konfigurációs objektum előkészítése

## SZINTAXISA

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorSimpleNetworkConfig** parancsmag hálózati konfigurációs objektumra készíti át a **set-AzureStorSimpleDevice** parancsmagot.
Állítsa a *Controller0IPAddress* paramétert és a *Controller1IPAddress* paramétert csak a Data0 felületen.
A Data0 csak három beállítást támogat: *Controller0IPAddress* , *Controller1IPAdress* és *EnableIscsi*.

## Példák

### 1. példa: Data0-felület beállítása
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

Ez a parancs hálózati konfigurációt hoz létre a Data0 felületéhez.
Ez a parancs a *Controller0IPv4Address* , az *Controller1IPv4Address* és a *EnableIscsi* paramétert adja meg.
Ez a parancsmag csak a következő három paraméterhez tudja konfigurálni a Data0.

### 2. példa: Configuren az Data0 eltérő felületet
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

Ez a parancs a Data1-felületet adja meg.

### 3. példa: eszköz konfigurációjának módosítása
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

Az első parancs létrehozza az Data0 felület hálózati konfigurációját.
Ez a parancs a *Controller0IPv4Address* , az *Controller1IPv4Address* és a *EnableIscsi* paramétert adja meg.
A parancs az eredményt az $NetworkConfigData 0 változóban tárolja.

A második parancs a **Get-AzureStorSimpleDevice** parancsmagot és a **Where-Object** Core parancsmagot használja online StorSimple-eszköz beszerzéséhez, majd a $OnlineDevice változóban tárolja.

A végleges parancs a **set-AzureStorSimpleDevice** parancsmaggal módosítja a megadott eszköz-azonosítót tartalmazó eszköz konfigurációját.
A parancs az első parancsban létrehozott Configuration objektummal használja az aktuális parancsmagot.

## PARAMÉTEREK

### -Controller0IPv4Address
A 0 vezérlő IPv4-címét adja meg.
Ezt a paramétert csak a Data0 felületéhez adja meg.

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

### -Controller1IPv4Address
Az 1-es vezérlő IPv4-címét adja meg.
Ezt a paramétert csak a Data0 felületéhez adja meg.

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

### -EnableCloud
Azt jelzi, hogy engedélyezve van-e a felhőalapú beállítás.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableIscsi
Azt jelzi, hogy engedélyezve van-e az internetes SCSI (ISCSI) az illesztőfelületen.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InterfaceAlias
Annak a kapcsolatnak az illesztőfelület-aliasát adja meg, amelyhez ez a parancsmag a beállításokat szolgáltatja.
Az érvényes értékek a Data0-től a Data5-ig kerülnek.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv4Address
Az összeköttetés IPv4-címét adja meg.

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

### -IPv4Gateway
Az átjáró IPv4-címét adja meg.

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

### -IPv4Netmask
Az összeköttetéshez tartozó IPv4-hálózati maszkot adja meg.

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

### -IPv6Gateway
Az összeköttetés IPv6-átjáróját adja meg.

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

### -IPv6Prefix
A felület IPv6-előtagját adja meg.

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

### -Profil
Egy Azure-profilt ad meg.

```yaml
Type: AzureSMProfile
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

### Nincs

## KIMENETEK

### NetworkConfig
Ez a parancsmag egy NetworkConfig objektumot ad eredményül, amely a következő tulajdonságokat tartalmazza: 

- **IsIscsiEnabled** ( **logikai** ) 
- **IsCloudEnabled** ( **logikai** )
- **Controller0IPv4Address** ( **IP_cím** ) 
- **Controller1IPv4Address** ( **IP_cím** ) 
- **IPv6Gateway** ( **IP_cím** ) 
- **IPv4Gateway** ( **IP_cím** ) 
- **IPv4Address** ( **IP_cím** ) 
- **IPv6Prefix** ( **karakterlánc** )
- **IPv4Netmask** ( **IP_cím** ) 
- **InterfaceAlias** ( **NetInterfaceId** )

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureStorSimpleDevice](./Set-AzureStorSimpleDevice.md)

[Get-AzureStorSimpleDevice](./Get-AzureStorSimpleDevice.md)



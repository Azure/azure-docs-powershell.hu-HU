---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c6479f9358322ae76eeb2fdf3cb9f2bb922e462
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848850"
---
# Set-AzureRmDnsRecordSet

## Áttekintés
Frissíti a DNS-rekord halmazát.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureRmDnsRecordSet** parancsmag egy helyi **Recordset** objektumról frissíti az Azure DNS szolgáltatásban lévő rekordot.

A **rekordhalmaz** -objektum paraméterként vagy a pipeline operátor segítségével átadható.

A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.

A Record set nem frissül, ha az Azure DNS-ben módosította a helyi **Recordset** objektum beolvasását.
Ez védelmet nyújt az egyidejű módosítások számára.
Ezt a működést a *felülírás* paraméterrel szüntetheti meg, amely az egyidejű módosításoktól függetlenül frissíti a rekordot.

## Példák

### Példa 1: rekordazonosító frissítése
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

Az első parancs az Get-AzureRmDnsRecordSet parancsmagot használja a megadott rekordtípus beolvasásához, majd a $RecordSet változóban tárolja.

A második és a harmadik parancs az off-line műveletekkel két rekordot hozhat létre a rekordhoz.

A végleges parancs a **set-AzureRmDnsRecordSet** parancsmagot használja a frissítés véglegesítéséhez.

### 2. példa: SOA rekord frissítése
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

Az első parancs a **Get-AzureRmDnsRecordset** parancsmagot használja a megadott rekordtípus beolvasásához, majd a $Recordset változóban tárolja.

A második parancs frissíti a megadott SOA-rekordot a $RecordSet.

A végleges parancs a **set-AzureRmDnsRecordSet** parancsmagot használja a frissítés $Recordset propagálásához.

## PARAMÉTEREK

### -Átír
Azt jelzi, hogy a rekordot az egyidejű módosításoktól függetlenül frissíteni kell.

Ha a rendszer az Azure DNS-ben módosította a helyi **Recordset** objektum beolvasását, a program nem frissíti a rekordot.
Ez védelmet nyújt az egyidejű módosítások számára.
Ha el szeretné tiltani ezt a problémát, használhatja a *felülírás* paramétert, amely a rekord egyidejű módosítástól függetlenül frissül.

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

### -RecordSet
A frissítendő **rekordhalmazt** adja meg.

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. DNS. DnsRecordSet
A **Recordset** objektum átadható a parancsmagnak.

## KIMENETEK

### Microsoft. Azure. Command. DNS. DnsRecordSet
Ez a parancsmag egy olyan objektumot ad eredményül, amely a frissített **Recordset** objektumot jelképezi.

## MEGJEGYZI
A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.
A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.

Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.
Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést. 

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[Új – AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)

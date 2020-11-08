---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194429"
---
# Set-AzDnsRecordSet

## Áttekintés
Frissíti a DNS-rekord halmazát.

## SZINTAXISA

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzDnsRecordSet** parancsmag egy helyi **Recordset** objektumról frissíti az Azure DNS szolgáltatásban lévő rekordot.
A **rekordhalmaz** -objektum paraméterként vagy a pipeline operátor segítségével átadható.
A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.
A Record set nem frissül, ha az Azure DNS-ben módosította a helyi **Recordset** objektum beolvasását.
Ez védelmet nyújt az egyidejű módosítások számára.
Ezt a működést a *felülírás* paraméterrel szüntetheti meg, amely az egyidejű módosításoktól függetlenül frissíti a rekordot.

## Példák

### Példa 1: rekordazonosító frissítése
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

Az első parancs az Get-AzDnsRecordSet parancsmagot használja a megadott rekordtípus beolvasásához, majd a $RecordSet változóban tárolja.
A második és a harmadik parancs az off-line műveletekkel két rekordot hozhat létre a rekordhoz.
A végleges parancs a **set-AzDnsRecordSet** parancsmagot használja a frissítés véglegesítéséhez.

### 2. példa: SOA rekord frissítése
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

Az első parancs a **Get-AzDnsRecordset** parancsmagot használja a megadott rekordtípus beolvasásához, majd a $Recordset változóban tárolja.
A második parancs frissíti a megadott SOA-rekordot a $RecordSet.
A végleges parancs a **set-AzDnsRecordSet** parancsmagot használja a frissítés $Recordset propagálásához.

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

### -Átír
Azt jelzi, hogy a rekordot az egyidejű módosításoktól függetlenül frissíteni kell.
Ha a rendszer az Azure DNS-ben módosította a helyi **Recordset** objektum beolvasását, a program nem frissíti a rekordot.
Ez védelmet nyújt az egyidejű módosítások számára.
Ha el szeretné tiltani ezt a problémát, használhatja a *felülírás* paramétert, amely a rekord egyidejű módosítástól függetlenül frissül.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. DNS. DnsRecordSet

## KIMENETEK

### Microsoft. Azure. Command. DNS. DnsRecordSet

## MEGJEGYZI
A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.
A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.
Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.
Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést. 

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[Új – AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147971"
---
# Set-AzDnsRecordSet

## SYNOPSIS
Frissíti a DNS-rekordkészletet.

## SZINTAXIS

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzDnsRecordSet** parancsmag egy helyi **RecordSet-objektumból** frissíti az Azure DNS-szolgáltatás egyik rekordkészletét.
A **RecordSet-objektumokat** paraméterként vagy a folyamat műveleti jelének használatával is át lehet adni.
A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.
A rekordkészlet nem frissül, ha módosult az Azure DNS-ben a helyi **RecordSet** objektum lekérése óta.
Ez védelmet nyújt az egyidejű módosítások számára.
Ezt a viselkedést  letilthatja a Felülírás paraméter használatával, amely a rekordkészletet frissíti, függetlenül a párhuzamos módosításoktól.

## PÉLDÁK

### 1. példa: Rekordkészlet frissítése
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

Az első parancs a Get-AzDnsRecordSet parancsmag használatával begyűjte a megadott rekordkészletet, majd a $RecordSet tárolja.
A második és a harmadik parancs off-line művelet, amely két A rekordot ad a rekordkészlethez.
Az utolsó parancs a **Set-AzDnsRecordSet** parancsmagot használja a frissítés véglegesítéséhez.

### 2. példa: SOA rekord frissítése
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

Az első parancs **a Get-AzDnsRecordset** parancsmag használatával begyűjte a megadott rekordkészletet, majd tárolja azt a $RecordSet változóban.
A második parancs frissíti a megadott SOA rekordot a $RecordSet.
Az utolsó parancs a **Set-AzDnsRecordSet** parancsmag segítségével propagálja a $RecordSet.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -Felülírás
Azt jelzi, hogy frissíteni kell a rekordkészletet az egyidejű módosításoktól függetlenül.
A rekordkészlet nem frissül, ha módosult az Azure DNS-ben a helyi **RecordSet** objektum lekérése óta.
Ez védelmet nyújt az egyidejű módosítások számára.
Ennek a viselkedésnek a  letiltásához használhatja a Felülírás paramétert, így a rekordkészlet frissül, függetlenül az egyidejű módosításoktól.

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
A **frissítenie kell rekordkészletet** adja meg.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## KIMENETEK

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## MEGJEGYZÉSEK
A Confirm *paraméterrel* szabályozhatja, hogy a parancsmag megerősítést kér-e.
A parancsmag alapértelmezés szerint megerősítést kér, $ConfirmPreference Windows PowerShell változó értéke Közepes vagy kisebb.
Ha a *Confirm* vagy *a Confirm:$True értéket adja* meg, ez a parancsmag megerősítést kér a futtatása előtt.
Ha a *Confirm:$False értéket* adja meg, a parancsmag nem kér megerősítést. 

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

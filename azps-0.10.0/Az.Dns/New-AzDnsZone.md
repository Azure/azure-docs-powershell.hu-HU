---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 0b41ff25823e44b31c7ff7677678a332782e7615
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843997"
---
# New-AzDnsZone

## Áttekintés
Új DNS-zóna létrehozása

## SZINTAXISA

```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **New-AzDnsZone** parancsmag egy új DNS-zónát hoz létre a megadott erőforráscsoport-szolgáltatónál. Adjon meg egy egyedi DNS-zóna nevét a *Name* paraméterhez, vagy a parancsmag hibát ad vissza. A zóna létrehozása után a New-AzDnsRecordSet parancsmagot használva hozhat létre rekordokat a zónában.

A *Confirm* paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.

## Példák

### Példa 1: DNS-zóna létrehozása
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Ez a parancs létrehoz egy új DNS-zónát a megadott erőforráscsoport myzone.com, majd a $Zone változóban tárolja.

## PARAMÉTEREK

### -Name (név)
A létrehozandó DNS-zóna nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azt az erőforráscsoportot adja meg, amelybe a zónát létre szeretné hozni.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
A kulcs-érték párok a hash-táblázatok formájában. Példa:

@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

Ebben a parancsmagban nem lehet beírni a bemenetet.

## KIMENETEK

### Microsoft. Azure. Command. DNS. DnsZone

Ez a parancsmag az új DNS-zónát képviselő Microsoft. Azure. Command. DNS. DnsZone objektumot ad eredményül.

## MEGJEGYZI
A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.
A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.

Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.
Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDnsZone](./Get-AzDnsZone.md)

[Új – AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)
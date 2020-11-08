---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183606"
---
# Remove-AzDnsRecordSet

## Áttekintés
Rekord törlése

## SZINTAXISA

### Mezők
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Vegyes
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objektum
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzDnsRecordSet** parancsmag törli a megadott rekordot a megadott zónából.
Nem törölhet olyan SOA-vagy névkiszolgálói (NS) rekordokat, amelyek automatikusan létrejönnek a zóna APEX-ben.
A **rekordhalmaz** -objektumot átadhatja erre a parancsmagra a pipeline operátorral vagy paraméterként.
Ha a rekordokat név és típus szerint szeretné megadni a **rekordhalmaz** -objektum használata nélkül, a zónát **dnsZone** objektumként kell átadnia ehhez a parancsmaghoz a pipeline operátorral vagy paraméterként, illetve a *ZoneName* és a *ResourceGroupName* paramétert is megadhatja.
A Confirm paramétert és $ConfirmPreference Windows PowerShell-változót használva beállíthatja, hogy a parancsmag kér-e megerősítést.
Ha a **rekordhalmazt Recordset** objektummal adja meg, akkor a program nem törli a rekordot, ha az Azure DNS megváltozott, mert a helyi **Recordset** objektum beolvasva lett.
Ez védelmet nyújt az egyidejű módosítások számára.
Ezt úgy teheti meg, hogy a *felülírási* paramétert használja, amely a rekordokat az egyidejű módosításoktól függetlenül törli.

## Példák

### 1. példa: a rekordtípus eltávolítása
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

Az első parancs a megadott rekordot kapja meg, majd a $RecordSet változóban tárolja. A második parancs eltávolítja a rekordot a $RecordSet.

### 2. példa: a rekordtípus eltávolítása és az összes megerősítés letiltása
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

Az első parancs a megadott rekordot kapja meg.
A második parancs törli a rekordot, még akkor is, ha időközben megváltozott.
A megerősítési utasításokat a rendszer letiltja.

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

### -Name (név)
Az eltávolítandó **rekordhalmaz** nevét adja meg.
Ha a rekordot név szerint adja meg, a DNS-zónát a *Zone* paraméterrel vagy a *ZoneName* és a *ResourceGroupName* paraméterrel kell megadni.
Másik lehetőségként a rekordhalmazt egy **Recordset** objektum segítségével is megadhatja, amelyet a *rekordhalmaz* paraméterrel adhat meg.

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Átír
Ha a **rekordhalmazt Recordset** objektummal adja meg, akkor a program nem törli a rekordot, ha az Azure DNS megváltozott, mert a helyi **Recordset** objektum beolvasva lett.
Ez védelmet nyújt az egyidejű módosítások számára.
Ezt a *felülírási* paraméter használatával lehet letiltani, amely a rekordokat az egyidejű módosításoktól függetlenül törli.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
passthru

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
Az eltávolítandó **Recordset** objektumot adja meg.
Azt is megteheti, hogy a rekord a *név* és a *zóna* paraméter segítségével, illetve a *név* , a *ZoneName* és a *ResourceGroupName* paraméter segítségével is megadható.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecordType
A DNS-rekord típusát adja meg.
Az érvényes értékek a következők:
- Egy
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- A TXT SOA rekordokat a rendszer automatikusan törli a zóna törlésekor.
Nem lehet manuálisan törölni a SOA-rekordokat.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azt a erőforráscsoportot adja meg, amely a törölni kívánt **rekordhalmazt** tartalmazó DNS-zónát tartalmazza.
Ez a paraméter csak akkor érvényes, ha a Record set és a DNS Zone argumentumot a *Name* és a *ZoneName* paraméterrel adja meg.
Azt is megteheti, hogy a *rekordhalmaz* paraméterrel vagy a *név* és a *zóna* paraméterrel megadhatja a rekordot.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone (zóna)
A törlendő **rekordhalmazt** tartalmazó DNS-zónát adja meg.
Ez a paraméter csak akkor érvényes, ha a rekordot a *Name* paraméterrel adja meg.
Azt is megteheti, hogy a *rekordhalmaz* paraméterrel, illetve a *név* , a *ZoneName* és a *ResourceGroupName* paraméterrel megadhatja a rekordot.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
A törlendő **rekordhalmazt** tartalmazó zóna nevét adja meg.
A *név* -és *ResourceGroupName* paramétereket is meg kell adnia.
Másik lehetőségként a *rekordhalmazt a Recordset* paraméterrel vagy a *név* és a *zóna* paraméterrel is megadhatja.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

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

### Microsoft. Azure. Management. DNS. models. RecordType

### System. String

### Microsoft. Azure. Command. DNS. DnsZone

### Microsoft. Azure. Command. DNS. DnsRecordSet

## KIMENETEK

### System. Boolean

## MEGJEGYZI
A *Confirm* paraméterrel beállíthatja, hogy a parancsmag kéri-e a megerősítést.
A parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, ha a $ConfirmPreference Windows PowerShell-változóban közepes vagy alacsonyabb érték szerepel.
Ha a *megerősítés* vagy a *megerősítés gombot adja meg: $true* , ez a parancsmag a Futtatás előtt kéri a megerősítést.
Ha a *megerősítés: $Falset* adja meg, a parancsmag nem kér megerősítést.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[Új – AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)

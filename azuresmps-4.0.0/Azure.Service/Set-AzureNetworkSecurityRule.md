---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015800"
---
# Set-AzureNetworkSecurityRule

## Áttekintés
Hálózatbiztonsági szabály hozzáadása vagy módosítása egy hálózati biztonsági csoportban

## SZINTAXISA

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **set-AzureNetworkSecurityRule** parancsmag az Azure Network biztonsági szabályait hozzáadja vagy módosítja egy hálózati biztonsági csoportban.

## Példák

## PARAMÉTEREK

### -Műveletek
A hálózati biztonsági szabályokra vonatkozó műveleteket adja meg.
Az érvényes értékek: Allow és deny.

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

### -DestinationAddressPrefix
A hálózati biztonsági szabálynak a cél IP-tartományának osztály nélküli tartományok közötti útválasztási (CIDR) címét adja meg.
A csillag (*) az IP-címet adja meg.

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

### -DestinationPortRange
A hálózat biztonsági szabályának célport-hatókörét adja meg.
Az érvényes értékek 0 és 65535 közötti egész számok.
Megadhat egy egyedi értéket, vagy megadhat egy LowerNumber-HigherNumber.
Egy kötőjel választja el a két értéket.

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

### -Name (név)
A parancsmag által hozzáadott vagy módosított hálózati biztonsági szabály nevét adja meg.

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

### -NetworkSecurityGroup
Azt a hálózati biztonsági csoportot adja meg, amelyre a parancsmag módosított.
**INetworkSecurityGroup** objektum beolvasásához használja az Get-AzureNetworkSecurityGroup parancsmagot.

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### – Prioritás
A hálózati biztonsági szabály prioritását adja meg.
Az érvényes értékek a következők: 100-től 4096-ig terjedő egész számok.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható. Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

### -Protocol
A hálózati biztonsági szabály protokollját adja meg.
Az érvényes értékek a következők: 

- TCP 
- UDP 
- *

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

### -SourceAddressPrefix
A hálózati biztonsági szabály forrás IP-CIDR címét adja meg.
A csillag (*) az IP-címet adja meg.

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

### -SourcePortRange
Megadja a hálózati biztonsági szabály forrásport-hatókörét.
Az érvényes értékek 0 és 65535 közötti egész számok.
Megadhat egy egyedi értéket, vagy megadhat egy LowerNumber-HigherNumber.
Egy kötőjel választja el a két értéket.

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

### -Type (típus)
A hálózati biztonsági szabályhoz tartozó kapcsolat típusát adja meg.
Érvényes értékek: bejövő és kimenő.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzureNetworkSecurityRule](./Remove-AzureNetworkSecurityRule.md)



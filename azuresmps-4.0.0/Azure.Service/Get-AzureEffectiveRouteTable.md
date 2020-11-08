---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016353"
---
# Get-AzureEffectiveRouteTable

## Áttekintés
A virtuális gép által alkalmazott útvonal beolvasása.

## SZINTAXISA

### IaaSGetEffectiveRouteTableParamSet
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### SlotGetEffectiveRouteTableParamSet
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureEffectiveRouteTable** parancsmag a virtuális gépeken alkalmazott útvonalat kapja meg.
Ez a művelet néhány másodpercig eltarthat.

## Példák

### Példa 1: a tényleges útvonal beszerzése virtuális gépet alkalmazva
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

Ez a parancs egy ContosoVM06 nevű virtuális gépet kap a ContosoService nevű szolgáltatáshoz, és átadja a virtuális gép objektumát az aktuális parancsmagnak.
Az aktuális parancsmag a virtuális gépre alkalmazott útvonalat kapja meg.

## PARAMÉTEREK

### -NetworkInterfaceName
Annak a hálózati adapternek a nevét adja meg, amelyhez ez a parancsmag hatékony útvonalakat kap.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -RoleInstanceName
Annak a Pásti-szerepnek a nevét adja meg, amelynek a parancsmagja hatékony útvonalakat kap.

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szolgáltatásnév
Egy felhőalapú szolgáltatás nevét adja meg.
A Péter szerepkör, amelyhez ez a parancsmag érvényes útvonalú, a paraméter által megadott szolgáltatáshoz tartozik.

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

### -Slot
A Péter-bővítőhelyet adja meg.
Az a Péter-szerep, amelynek a parancsmagja hatékony útvonalon van, a paraméter által megadott bővítőhely van megadható.
Az érvényes értékek a következők: 

- Production
- Átmeneti tárolásra szolgáló 

Az alapértelmezett érték a termelés.

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Annak a virtuális gépnek az objektumát adja meg, amelyhez ez a parancsmag hatékony útvonalakat kap.

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### System. Collections. Generic. IEnumerable<Microsoft. WindowsAzure. Management. Network. models. EffectiveRouteTable, Microsoft. WindowsAzure. Management. Network>

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRouteTable](./Get-AzureRouteTable.md)

[Új – AzureRouteTable](./New-AzureRouteTable.md)

[Remove-AzureRouteTable](./Remove-AzureRouteTable.md)

[Remove-AzureSubnetRouteTable](./Remove-AzureSubnetRouteTable.md)

[Set-AzureSubnetRouteTable](./Set-AzureSubnetRouteTable.md)



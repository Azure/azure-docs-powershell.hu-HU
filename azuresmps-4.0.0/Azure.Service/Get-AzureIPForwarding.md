---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BE661AC7-BA39-4D6A-8083-16CE9327DC08
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4c84155484435a9601af005393593040c9cfe4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016348"
---
# Get-AzureIPForwarding

## Áttekintés
Megkapja az IP-továbbítás állapotát.

## SZINTAXISA

### IaaSIPForwardingParamSet
```
Get-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### SlotIPForwardingParamSet
```
Get-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureIPForwarding** parancsmag az IP-továbbítás állapotát kapja meg.

## Példák

### Példa 1: IP-továbbítási állapot beszerzése virtuális géphez
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureIPForwarding
Disabled
```

Ez a parancs egy ContosoVM06 nevű virtuális gépet kap a ContosoService nevű szolgáltatáshoz, és átadja a virtuális gép objektumát az aktuális parancsmagnak.
Az aktuális parancsmag a virtuális gép IP-továbbítási állapotát kapja meg.

## PARAMÉTEREK

### -NetworkInterfaceName
Annak a hálózati adapternek a neve, amelyhez a parancsmag IP-továbbítási állapotot kap.

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

### -RoleName
Itt adhatja meg annak a Pásti-szerepnek a nevét, amelynek a parancsmagja IP-továbbítási állapotot kap.

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szolgáltatásnév
Egy felhőalapú szolgáltatás nevét adja meg.
A Péter-szerep a paraméter által megadott szolgáltatáshoz tartozik.

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
Az a Péter-szerep, amelyre a parancsmag átirányítást kap, a paraméter által megadott bővítőhelyet adja meg.
Az érvényes értékek a következők: 

- Production
- Átmeneti tárolásra szolgáló 

Az alapértelmezett érték a termelés.

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Annak a virtuálisgép-objektumnak a megadása, amelyhez ez a parancsmag IP-továbbítási állapotot kap.

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSIPForwardingParamSet
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

### System. String

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureIPForwarding](./Set-AzureIPForwarding.md)



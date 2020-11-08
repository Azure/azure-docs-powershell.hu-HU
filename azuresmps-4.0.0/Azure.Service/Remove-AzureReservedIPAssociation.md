---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A6964C80-1991-46FC-84C8-5B00616386BE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e43f841fea77626c18edbda541fa011e95faceb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016136"
---
# Remove-AzureReservedIPAssociation

## Áttekintés
Eltávolítja a társítást a fenntartott IP-címről a VM vagy a felhő szolgáltatásba.

## SZINTAXISA

```
Remove-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureReservedIPAssociation** parancsmag nem társítja a lefoglalt IP-címet egy virtuális GÉPRŐL (VM) vagy Felhőbeli szolgáltatásból.
Amikor a művelet befejeződött, a lefoglalt IP-cím ingyenes, és a VM/VIP megkapja a dinamikus nyilvános IP-címet az Azure Inventory rendszerből.

## Példák

### 1. példa: fenntartott IP-társítás eltávolítása
```
PS C:\> Remove-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

Ez a parancs nem társítja a ResIp14 nevű fenntartott IP-címet a PipTestWestEurope nevű szolgáltatásból.
A PipTestWestEurope egy új dinamikus VIP-felhasználó lesz társítva.

## PARAMÉTEREK

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

Ezzel a jelzéssel figyelmen kívül hagyhatja az e-maileket a fenntartott IP-társítás eltávolításakor.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

### -ReservedIPName
A foglalt IP-cím nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szolgáltatásnév
A szolgáltatás nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
A központi telepítő környezetet adja meg.
A paraméter elfogadható értékei a következők: termelés, megállóhelyek.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualIPName
Azt a virtuális IP-címet adja meg, amelyből el szeretné távolítani a társítást egy szolgáltatással vagy VM-tel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. WindowsAzure. commands. Utilities. Common. ManagementOperationContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureReservedIPAssociation](./Set-AzureReservedIPAssociation.md)



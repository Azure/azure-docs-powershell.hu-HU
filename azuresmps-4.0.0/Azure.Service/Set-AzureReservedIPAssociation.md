---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015825"
---
# Set-AzureReservedIPAssociation

## Áttekintés
Fenntartott IP-címet társít egy meglévő virtuális géphez vagy felhőalapú szolgáltatáshoz.

## SZINTAXISA

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **set-AzureReservedIPAssociation** parancsmag FENNTARTott IP-címet társít egy futó virtuális gép vagy felhőalapú szolgáltatás virtuális IP-címével (VIP).
A fenntartott IP-cím nem használható az e parancsmag használatakor, és ugyanazon a helyen kell lennie, mint a virtuális gépet vagy a Felhőbeli szolgáltatást.

A művelet körülbelül 30 másodperc elteltével lép életbe, ami után a virtuális gép vagy szolgáltatás elérhető a lefoglalt IP-cím használatával.

## Példák

### 1. példa: fenntartott IP-társítás beállítása
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

Ez a parancs hozzárendeli a ResIp14 nevű fenntartott IP-címet a szolgáltatás PipTestWestEurope.
A ResIp14 egy fenntartott IP a Nyugat-európai régióban.

## PARAMÉTEREK

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
Annak a fenntartott IP-címnek a nevét adja meg, amelyet egy virtuális géphez vagy szolgáltatáshoz szeretne társítani.

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
Annak a szolgáltatásnak a nevét adja meg, amelybe a lefoglalt IP-címet társítani szeretné.

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
A telepítő bővítőhelyet adja meg.
A paraméter elfogadható értékei a következők:

- Átmeneti tárolásra szolgáló
- Production

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
Annak a meglévő VIP-névnek a nevét adja meg, amely társítva van egy fenntartott IP-vel.
Lásd: Add-AzureVirtualIP a VIP-szolgáltatások hozzáadásához

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

[Remove-AzureReservedIPAssociation](./Remove-AzureReservedIPAssociation.md)



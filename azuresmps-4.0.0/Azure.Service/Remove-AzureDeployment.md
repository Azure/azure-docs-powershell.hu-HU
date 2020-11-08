---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016165"
---
# Remove-AzureDeployment

## Áttekintés
Törli a Felhőbeli szolgáltatások üzembe helyezését.

## SZINTAXISA

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzureDeployment** parancsmag törli az Azure Cloud-szolgáltatás telepítését.
Ha törölni szeretne egy központi telepítőt, először függessze fel.

## Példák

### 1. példa: a központi telepítő eltávolítása
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

Ez a parancs eltávolítja a ContosoService nevű Azure szolgáltatás telepítését.
Mivel a parancs nem ad meg tárolóhelyet, eltávolítja a szolgáltatást a termelési környezetből.

### 2. példa: a központi telepítések és a virtuális merevlemezek eltávolítása
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

Ez a parancs eltávolítja a ContosoService nevű szolgáltatás telepítését a termelési környezetből.
A parancs a mögöttes virtuális merevlemezeket is eltávolítja.

## PARAMÉTEREK

### -DeleteVHD
Megadja, hogy a parancsmag eltávolítja a telepítőt és a virtuális merevlemezeket (VHD-ket) a blob-tárolóból.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
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

### -Szolgáltatásnév
Annak a szolgáltatásnak a nevét adja meg, amelyre ez a parancsmag törli a telepített példányát.

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

### -Slot
Azt a központi telepítő környezetet adja meg, amelyből a parancsmag törli a központi telepítőt.
Érvényes értékek: staging és termelés.
Az alapértelmezett érték a termelés.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### ManagementOperationContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[Move-AzureDeployment](./Move-AzureDeployment.md)

[Új – AzureDeployment](./New-AzureDeployment.md)

[Set-AzureDeployment](./Set-AzureDeployment.md)



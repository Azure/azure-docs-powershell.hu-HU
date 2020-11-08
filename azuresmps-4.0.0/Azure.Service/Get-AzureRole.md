---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016314"
---
# Get-AzureRole

## Áttekintés
A Microsoft Azure-szolgáltatás szerepköreinek listáját adja eredményül.

## SZINTAXISA

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureRole** parancsmag egy lista-objektumot ad eredményül, amely a Microsoft Azure-szolgáltatás szerepköreinek részleteit tartalmazza.
Ha a *RoleName* paramétert adja meg, a **Get-AzureRole** csak az adott szerepkör adatait adja eredményül.
Ha a *InstanceDetails* paramétert adja meg, a függvény további, példány-specifikus részleteket ad vissza.

## Példák

### Példa 1: a szolgáltatások szerepkörének beszerzése
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

Ez a parancs egy olyan objektumot ad eredményül, amely részletesen ismerteti az MySvc01 szolgáltatásban futó összes termelési szerepkört.

### 2. példa: adatok beszerzése a szolgáltatáson futó szerepkörökről
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

Ez a parancs egy olyan objektumot ad eredményül, amely a MyTestVM3 szerepkör részleteit jeleníti meg a MySvc01 szolgáltatás átmeneti környezetében.

### 3. példa: a szolgáltatásban futó szerepkör példányaira vonatkozó információk beszerzése
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

Ez a parancs egy olyan objektumot ad eredményül, amely részletesen ismerteti az MyTestVM02 szerepkör példányait a MySvc01 szolgáltatás üzemi környezetében.

### Példa 4: a szolgáltatáshoz társított szerepkör-példányok táblázatának beszerzése
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

Ez a parancs visszaadja az MySvc01 szolgáltatás üzemi környezetében futó minden szerepkör-példány példányának nevét, méretét és állapotát.

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

### -InstanceDetails
Azt adja meg, hogy a parancsmag az egyes szerepkörök példányairól adja meg az adatokat.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -RoleName
A beolvasott szerepkör nevét adja meg.

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

### -Szolgáltatásnév
Az Azure-szolgáltatás nevét adja meg.

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
Az Azure-telepítő környezetét adja meg.
A paraméter elfogadható értékei a következők: termelés vagy megállóhely.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureRole](./Set-AzureRole.md)



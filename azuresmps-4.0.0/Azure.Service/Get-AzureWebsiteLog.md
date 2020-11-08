---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016506"
---
# Get-AzureWebsiteLog

## Áttekintés
A megadott webhelyhez naplók jelentkeznek.

## SZINTAXISA

### Farok
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ListPath
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A megadott webhely naplózása.

## Példák

### Példa 1: a napló folyamatos indítása
```
PS C:\> Get-AzureWebsiteLog -Tail
```

Ez a példa elindítja a naplózást az összes alkalmazás-naplóban.

### 2. példa: naplók indítása a http-naplókból
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

Ez a példa elindítja a http-naplók naplózását.

### 3. példa: naplók indítása a hibanapló továbbításához
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

Ez a példa elindítja a naplózási adatfolyamot, és csak a hibák naplózását jeleníti meg.

### 4. példa: avaiable naplók megjelenítése
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

Ez a példa felsorolja a webhely összes elérhető naplózási útvonalát.

## PARAMÉTEREK

### -ListPath
Azt jelzi, hogy a napló elérési útvonalait szeretné-e listázni

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Üzenet
Itt adhatja meg azt a karakterláncot, amelyet a rendszer a napló üzenetének szűréséhez fog használni.
Csak a karakterláncot tartalmazó naplók lesznek beolvasva.

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A webhely neve.

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

### -Path (elérési út)
Az az útvonal, amelyből a naplót vissza kívánja olvasni.
Alapértelmezés szerint ez a root, ami azt jelenti, hogy az összes elérési utat tartalmazza.

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
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

### -Slot
A bővítőhely nevét adja meg.

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

### -Farok
Itt adhatja meg, hogy a naplókat szeretné-e továbbítani.

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
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

[Get-AzureWebsite](./Get-AzureWebsite.md)

[Új – AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Start-AzureWebsite](./Start-AzureWebsite.md)



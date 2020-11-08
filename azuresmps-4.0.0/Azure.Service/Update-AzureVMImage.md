---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5544F2E2-27EF-4079-8E13-6B85DF2018A2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a71ad8b25a17c1c2933cdcf305ba0b53f67bf0f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016583"
---
# Update-AzureVMImage

## Áttekintés
A képtárházban frissíti az operációs rendszer képének címkéjét.

## SZINTAXISA

```
Update-AzureVMImage [-ImageName] <String> [-Label] <String> [[-Eula] <String>] [[-Description] <String>]
 [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>]
 [[-DiskConfig] <VirtualMachineImageDiskConfigSet>] [[-Language] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-DontShowInGui] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
Az **Update-AzureVMImage** parancsmag a képtárházban lévő operációs rendszer képére frissíti a címkét.
Egy képobjektumot ad eredményül, amely a frissített képpel kapcsolatos információkat jeleníti meg.

## Példák

### Példa 1: kép frissítése a képfelirat módosításával
```
PS C:\> Update-AzureVMImage -ImageName "Windows-Server-2008-SP2" -Label "DoNotUse"
```

Ez a parancs frissíti a Windows-Server-2008-SP2 lemezképfájlt, ha módosítja a képfeliratot a DoNotUse-ra.

### 2. példa: az összes operációs rendszer beszerzése címke szerint, majd a címke frissítése
```
PS C:\> Get-AzureVMImage | Where-Object {$_.Label -eq "DoNotUse" } | Update-AzureVMImage -Label "Updated"
```

Ez a parancs beolvassa az összes operációs rendszer DoNotUse, és a címkét módosította.

## PARAMÉTEREK

### -Leírás
Az operációs rendszer képének leírását adja meg.

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

### -DiskConfig
A **AzureVMImageDiskConfigSet** , a **set-AzureVMImageOSDiskConfig** és a **set-AzureVMImageDataDiskConfig** parancsmagok használatával létrehozott virtuális gép lemezképfájljának operációs rendszerének és adatlemezének konfigurációját adja meg.

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DontShowInGui
Jelzi, hogy ez a parancsmag nem jeleníti meg a képet a GUI-ban.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EULA
A végfelhasználói licencszerződést adja meg.
Azt javasoljuk, hogy az érték egy URL-cím.

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

### -IconName
Az operációs rendszer vagy a virtuális gép képének normál ikonjának nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: IconUri

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageFamily
Egy olyan értéket ad meg, amely az operációs rendszer vagy a virtuális gép képeinek csoportosítására használható.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageName
A képtárházban frissítendő kép nevét adja meg.

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

### -Label (címke)
A kép új feliratát adja meg.

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

### -Nyelv
Az operációs rendszer nyelvét adja meg a virtuális gép vagy az operációs rendszer képen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivacyUri
Meghatározza az operációs rendszer képhez kapcsolódó adatvédelmi szabályokat tartalmazó dokumentumra mutató URI-azonosítót.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
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

### -PublishedDate
Azt a dátumot adja meg, amikor az operációs rendszer képet felvette a képtárházba.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecommendedVMSize
A virtuális gép méretét adja meg.

A paraméter elfogadható értékei a következők:

- Közepes
- Nagy
- ExtraLarge
- A5
- A6
- A7

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SmallIconName
Megadja az operációs rendszer vagy a virtuálisgép-kép kis ikonjának nevét.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmallIconUri

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### OSImageContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Remove-AzureVMImage](./Remove-AzureVMImage.md)

[Mentés-AzureVMImage](./Save-AzureVMImage.md)

[Új – AzureVMImageDiskConfigSet](./New-AzureVMImageDiskConfigSet.md)

[Set-AzureVMImageOSDiskConfig](./Set-AzureVMImageOSDiskConfig.md)

[Set-AzureVMImageDataDiskConfig](./Set-AzureVMImageDataDiskConfig.md)



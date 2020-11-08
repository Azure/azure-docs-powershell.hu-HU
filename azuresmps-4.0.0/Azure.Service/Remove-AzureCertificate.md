---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016167"
---
# Remove-AzureCertificate

## Áttekintés
Tanúsítvány eltávolítása Azure-szolgáltatásból.

## SZINTAXISA

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzureCertificate** parancsmag az Azure-szolgáltatások tanúsítványait távolítja el.

## Példák

### 1. példa: tanúsítvány eltávolítása egy szolgáltatásból
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

Ez a parancs eltávolítja azt a tanúsítvány-objektumot, amely a Felhőbeli szolgáltatás megadott ujjlenyomatával rendelkezik.

### 2. példa: az összes tanúsítvány eltávolítása egy szolgáltatásból
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

Ez a parancs a **Get-AzureCertificate** parancsmag használatával kapja meg a ContosoService nevű szolgáltatás összes tanúsítványát.
A parancs a csővezeték-kezelő segítségével átadja az egyes tanúsítványokat az aktuális parancsmagnak.
Ez a parancsmag eltávolítja az egyes tanúsítványokat a felhőalapú szolgáltatásból.

### 3. példa: egy adott ujjlenyomat-algoritmust használó szolgáltatás összes tanúsítványának eltávolítása
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

Ez a parancs a ContosoService nevű szolgáltatás összes olyan tanúsítványát beolvassa, amely az SHA1 ujjlenyomat-algoritmust használja.
A parancs átadja az egyes tanúsítványokat az aktuális parancsmagnak, amely az egyes tanúsítványokat eltávolítja.

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

### -Szolgáltatásnév
Annak az Azure-szolgáltatásnak a neve, amelyből a parancsmag eltávolítja a tanúsítványt.

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

### -Ujjlenyomat
A parancsmag által eltávolított tanúsítvány ujjlenyomatát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ThumbprintAlgorithm
A tanúsítvány ujjlenyomatának létrehozásához használt algoritmust adja meg.

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

[Add-AzureCertificate](./Add-AzureCertificate.md)

[Get-AzureCertificate](./Get-AzureCertificate.md)

[Új – AzureCertificateSetting](./New-AzureCertificateSetting.md)



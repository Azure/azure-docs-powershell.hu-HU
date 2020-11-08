---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A6D5C40-2532-4FD1-A74F-16725CAD8EDD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29d049dbdce93102411a875cfaef8e5fb9c719b6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016395"
---
# Add-AzureCertificate

## Áttekintés
Tanúsítvány feltöltése Azure Cloud-szolgáltatásba.

## SZINTAXISA

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
A **Add-AzureCertificate** parancsmag az Azure-szolgáltatások tanúsítványát tölti fel.

## Példák

### 1. példa: tanúsítvány és jelszó feltöltése
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

A parancs feltölti a ContosoCertificate. pfx fájlt egy felhőalapú szolgáltatásba.
A parancs a tanúsítvány jelszavát adja meg.

### 2. példa: tanúsítványfájl feltöltése
```
PS C:\> Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

A parancs feltölti a ContosoCertificate. cer fájlt egy felhőalapú szolgáltatásba.
A parancs a tanúsítvány jelszavát adja meg.

### 3. példa: a bizonyítvány-objektum feltöltése
```
PS C:\> $Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

Az első parancs a Windows PowerShell Core **Get-Item** parancsmag segítségével kap tanúsítványt a felhasználó saját tárolójában.
A parancs a $Certificate változóban tárolja a tanúsítványt.

A második parancs a $certificate egy felhőalapú szolgáltatásba feltölti a tanúsítványt.

## PARAMÉTEREK

### -CertToDeploy
A telepítendő tanúsítványt adja meg.
Megadhatja a tanúsítványfájl teljes elérési útját, például egy *. cer vagy *.
pfx-fájlnév-kiterjesztés vagy X. 509 tanúsítvány objektum.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### -Jelszó
A tanúsítvány jelszavát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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
Annak az Azure-szolgáltatásnak a nevét adja meg, amelyre a parancsmag hozzáadja a tanúsítványt.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### ManagementOperationContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureCertificate](./Get-AzureCertificate.md)

[Új – AzureCertificateSetting](./New-AzureCertificateSetting.md)

[Remove-AzureCertificate](./Remove-AzureCertificate.md)



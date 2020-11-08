---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015932"
---
# New-AzureCertificateSetting

## Áttekintés
Tanúsítvány-beállítási objektum létrehozása egy szolgáltatásban.

## SZINTAXISA

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **New-AzureCertificateSetting** parancsmag létrehoz egy tanúsítvány-beállítási objektumot egy Azure-szolgáltatásban található tanúsítványhoz.

Az **Add-AzureProvisioningConfig** parancsmaggal egy tanúsítvány-beállítási objektum segítségével hozhat létre konfigurációs objektumokat.
A **New-AzureVM** parancsmaggal virtuális gépet hozhat létre a konfigurációs objektumokkal.
A tanúsítvány-beállítási objektum segítségével virtuális gépet hozhat létre a **New-AzureQuickVM** parancsmag használatával.

## Példák

### Példa 1: tanúsítvány-beállítási objektum létrehozása
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

Ezzel a paranccsal létrehoz egy tanúsítvány-beállítási objektumot egy meglévő tanúsítványhoz.

### 2. példa: konfigurációs beállítási objektumot használó virtuális gép létrehozása
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

Az első parancs az **Add-AzureCertificate** parancsmag segítségével hozzáadja a ContosoCert. cer nevű tanúsítványt a ContosoService nevű szolgáltatáshoz.

A második parancs létrehozza a tanúsítvány-beállítási objektumot, majd a $CertificateSetting változóban tárolja.

A harmadik parancs a **Get-AzureVMImage** parancsmag segítségével kap képet a képtárházból.
Ez a parancs a képet a $Image változóban tárolja.

A végleges parancs a virtuális gép konfigurációs objektumát a **New-AzureVMConfig** parancsmag segítségével hozza létre a $image kép alapján.
A parancs a csővezeték-kezelő használatával továbbítja az objektumot az **Add-AzureProvisioningConfig** parancsmaghoz.
Ebben a parancsmagban kiépítési adatok adhatók hozzá a konfigurációhoz.
A parancs átadja az objektumot a **New-AzureVM** parancsmagnak, amely a virtuális gépet hozza létre.

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

### -StoreName mezőt
Azt a tanúsítványtárolót adja meg, amelybe a tanúsítványt be szeretné helyezni.
Az érvényes értékek a következők: 

- AddressBook
- AuthRoot
- CertificateAuthority
- Fájltípusa nem engedélyezett
- A
- Legfelső szintű
- TrustedPeople
- TrustedPublisher

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ujjlenyomat
A tanúsítvány ujjlenyomatát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureCertificate](./Add-AzureCertificate.md)

[Add-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Get-AzureCertificate](./Get-AzureCertificate.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Új – AzureQuickVM](./New-AzureQuickVM.md)

[Új – AzureVM](./New-AzureVM.md)

[Remove-AzureCertificate](./Remove-AzureCertificate.md)



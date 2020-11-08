---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015982"
---
# New-AzureSSHKey

## Áttekintés
A meglévő tanúsítvány új, Linux-alapú Azure virtuális gépre való beszúrására szolgáló SSH-kulcs objektum létrehozása.

## SZINTAXISA

### kulcspár
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### PUBLICKEY
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **New-AzureSSHKey** parancsmag létrehoz egy SSH-kulcsú objektumot egy olyan tanúsítványhoz, amely már hozzá lett adva az Azure-hoz.
Ezt az SSH billentyűt ezt követően az új **AzureProvisioningConfig** is használhatja, ha új virtuális gépet hoz létre a konfigurációs objektumhoz új **AzureVM** , vagy ha új virtuális gépet hoz létre a **New-AzureQuickVM** használatával.
Ha a virtuálisgép-készítő parancsfájlok részeként része, akkor a megadott SSH nyilvános kulcsot vagy kulcspárt adja hozzá az új virtuális géphez.

## Példák

### Példa 1: tanúsítvány-beállítási objektum létrehozása
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

Ez a parancs létrehoz egy tanúsítvány-beállítási objektumot egy meglévő tanúsítványhoz, majd egy változóban tárolja az objektumot későbbi használatra.

### 2. példa: tanúsítvány felvétele szolgáltatásba
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

Ez a parancs tanúsítványokat ad egy Azure-szolgáltatáshoz, majd létrehoz egy új, a tanúsítványt használó virtuális virtuális gépet.

## PARAMÉTEREK

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

### -Kulcspár
Itt adhatja meg, hogy ez a parancsmag létrehoz egy olyan objektumot, amely egy SSH kulcspár beszúrását az új virtuálisgép-konfigurációba illeszti be.

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path (elérési út)
Az SSH-beli nyilvános kulcs vagy kulcspár tárolásának elérési útját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicKey
Itt adhatja meg, hogy a parancsmag létrehoz egy olyan objektumot, amely egy SSH nyilvános kulcs beszúrását az új virtuálisgép-konfigurációba illeszti be.

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
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

[Add-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Új – AzureVMConfig](./New-AzureVMConfig.md)

[Új – AzureVM](./New-AzureVM.md)

[Új – AzureQuickVM](./New-AzureQuickVM.md)



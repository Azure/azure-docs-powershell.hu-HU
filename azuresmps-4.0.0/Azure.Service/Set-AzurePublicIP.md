---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015955"
---
# Set-AzurePublicIP

## Áttekintés
Nyilvános IP-címet ad az Azure Virtual Machine-nek.

## SZINTAXISA

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **set-AzurePublicIP** parancsmag nyilvános IP-címet ad egy Azure Virtual Machine-nek.
Ha egy meglévő virtuális géphez futtatja ezt a parancsmagot, frissítse a virtuális gépet a módosítások végrehajtásához.
Megadhat egy tartománynév-címkét, amely a nyilvános IP-hez megfelelő DNS-bejegyzést hoz létre.

## Példák

### 1. példa: nyilvános IP-cím hozzáadása meglévő virtuális géphez
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a FTPInstance nevű virtuális gépet a FTPInAzure nevű szolgáltatásban.
A parancs a virtuális gépet az aktuális parancsmagra átadja a pipeline operátor használatával.
Az aktuális parancsmag hozzáadja a nyilvános IP-név ftpip.
A parancs átadja a virtuális gépet az **Update-AzureVM** parancsmagnak, amely végrehajtja a módosításokat.

### 2. példa: nyilvános IP hozzáadása egy új virtuális géphez
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Ez a parancs a virtuális gép konfigurációs objektumát a **New-AzureVMConfig** parancsmag használatával hozza létre.
A parancs átadja az objektumot az **Add-AzureProvisioningConfig** parancsmagnak, ami további konfigurációt biztosít.
Az aktuális parancsmag hozzáadja a nyilvános IP-név ftpip.
A parancs átadja a konfigurációt a **New-AzureVM** parancsmagnak, amely a virtuális gépet hozza létre.

### 3. példa: nyilvános IP-cím és címke hozzáadása meglévő virtuális géphez
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a FTPInstance nevű virtuális gépet a FTPInAzure nevű szolgáltatásban.
A parancs a virtuális gépet az aktuális parancsmagra átadja a pipeline operátor használatával.
Az aktuális parancsmag hozzáadja a nyilvános IP-név ftpip és a címke ipname.
A parancs frissíti a virtuális gépet, amely végrehajtja a módosításokat.

### 4. példa: nyilvános IP-cím és címke hozzáadása egy új virtuális géphez
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

Ez a parancs létrehoz egy virtuális gép konfigurációs objektumát, majd átadja az objektumot a **AzureProvisioningConfig** , amely további konfigurációt biztosít.
Az aktuális parancsmag hozzáadja a nyilvános IP-név ftpip és a címke ipname.
A parancs a virtuális gépet hozza létre.

## PARAMÉTEREK

### -DomainNameLabel
Adja meg a nyilvános IP-címhez tartozó DNS-bejegyzéshez használni kívánt nevet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
A TCP üresjárati időtúllépési időszakát adja meg percben.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

### -PublicIPName
Adja meg a nyilvános IP-nevet.

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

### -VM
Azt a virtuális gépet adja meg, amelyre a parancsmag hozzáadja a nyilvános IP-címet.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. WindowsAzure. Command. ServiceManagement. Model. IPersistentVM

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzurePublicIP](./Get-AzurePublicIP.md)

[Get-AzureVM](./Get-AzureVM.md)

[Új – AzureVM](./New-AzureVM.md)

[Új – AzureVMConfig](./New-AzureVMConfig.md)

[Remove-AzurePublicIP](./Remove-AzurePublicIP.md)

[Update-AzureVM](./Update-AzureVM.md)



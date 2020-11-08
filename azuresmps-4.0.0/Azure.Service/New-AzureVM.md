---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1999C880-F8F9-4CED-91A9-33E9BBDFE27D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09a3d7be7bf71e73443dcbb31464ee6f7f19b43a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016200"
---
# New-AzureVM

## Áttekintés
Azure virtuális gépet hoz létre.

## SZINTAXISA

### ExistingService (alapértelmezett)
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### CreateService
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **New-AzureVM** parancsmag új virtuális gépet ad egy meglévő Azure-szolgáltatáshoz, vagy virtuális gépet és szolgáltatást hoz létre a jelenlegi előfizetésben, ha a *helyet* vagy a *AffinityGroup* adja meg.

## Példák

### Példa 1: virtuális gép létrehozása Windows-konfigurációhoz
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

Ez a parancs létrehoz egy kiépítési konfigurációt a Windows operációs rendszer virtuálisgép-konfigurációja alapján, és egy virtuális gépet hoz létre a megadott affinitási csoportban.

### 2. példa: virtuális gép létrehozása Linux-konfigurációhoz
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

Ez a parancs létrehoz egy kiépítési konfigurációt a Linux virtuális gép konfigurációja alapján, és egy virtuális gépet hoz létre a megadott affinitási csoportban.

### 3. példa: virtuális gép létrehozása és adatlemez hozzáadása
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

Az első két parancs a **Get-AzureVMImage** parancsmag használatával érheti el a képeket, és az $Image változóban tárolja az egyiket.

Ez a parancs létrehoz egy kiépítési konfigurációt a Windows operációs rendszer virtuálisgép-konfigurációja alapján, és egy virtuális gépet hoz létre Azure-adatlemezzel.

### Példa 4: fenntartott IP-címmel rendelkező virtuális gép létrehozása
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

Ez a parancs létrehoz egy kiépítési konfigurációt a Windows operációs rendszer virtuálisgép-konfigurációja alapján, és egy fenntartott IP-címet használó virtuális gépet hoz létre.

## PARAMÉTEREK

### -AffinityGroup
Annak az Azure affinitásnak a csoportját adja meg, amelyben a Felhőbeli szolgáltatás található.
Ehhez a paraméterhez csak akkor van szükség, ha a parancsmag felhőalapú szolgáltatást hoz létre.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeploymentLabel
A központi telepítő címkéjét adja meg.

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

### -DeploymentName
A telepítő nevét adja meg.
Ha nem adja meg, akkor ez a parancsmag a szolgáltatás nevét használja a központi telepítő nevében.

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

### -DnsSettings
Megadja azt a DNS-kiszolgáló objektumot, amely meghatározza az új központi telepítő DNS-beállításait.

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -InternalLoadBalancerConfig
Belső terheléselosztót ad meg.
Ezt a paramétert a program nem használja.

```yaml
Type: InternalLoadBalancerConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Hely
Az új szolgáltatást működtető helyet adja meg.
Ha már létezik a szolgáltatás, ne adja meg ezt a paramétert.

```yaml
Type: String
Parameter Sets: CreateService
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

### -ReservedIPName
A foglalt IP-cím nevét adja meg.

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

### -ReverseDnsFqdn
A DNS-név teljesen minősített tartománynevét adja meg.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceDescription
Az új szolgáltatás leírását adja meg.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceLabel
Az új szolgáltatás feliratát adja meg.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szolgáltatásnév
Az új vagy meglévő szolgáltatás nevét adja meg.

Ha a szolgáltatás nem létezik, akkor ez a parancsmag hozza létre Önnek a megfelelőt.
A *hely* vagy a *AffinityGroup* paraméterrel megadhatja, hogy hová hozza létre a szolgáltatást.

Ha a szolgáltatás létezik, a *hely* -vagy *AffinityGroup* paraméter nem szükséges.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMs
A létrehozandó virtuális számítógép-objektumok listáját adja meg.

```yaml
Type: PersistentVM[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -VNetName
Annak a virtuális hálózatnak a nevét adja meg, ahol ez a parancsmag telepíti a virtuális gépet.

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

### -WaitForBoot
Itt adhatja meg, hogy ez a parancsmag várja a virtuális gépet a **ReadyRole** állapot eléréséhez.
Ez a parancsmag nem hajtható végre, ha a virtuális gép az alábbi állapotok egyikére esik a várakozás közben: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

[Add-AzureDataDisk](./Add-AzureDataDisk.md)

[Add-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Új – AzureVMConfig](./New-AzureVMConfig.md)



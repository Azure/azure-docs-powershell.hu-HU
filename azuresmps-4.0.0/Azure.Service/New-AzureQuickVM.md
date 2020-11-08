---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015909"
---
# New-AzureQuickVM

## Áttekintés
Azure virtuális gépet konfigurál és hoz létre.

## SZINTAXISA

### Windows (alapértelmezett)
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **New-AzureQuickVM** parancsmag egy Azure virtuális gépet állít be és hoz létre.
Ez a parancsmag a virtuális gépet egy meglévő Azure-szolgáltatásba telepítheti.
Ez a parancsmag egy olyan Azure-szolgáltatást is létrehozhat, amely az új virtuális gépet tárolja.

## Példák

### Példa 1: virtuális gép létrehozása
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

Ez a parancs létrehoz egy virtuális gépet, amely futtatja a Windows operációs rendszert egy meglévő szolgáltatásban.
A parancsmag a megadott képen a virtuális gépet alapozza.
A parancs a *WaitForBoot* paramétert adja meg.
Ezért a parancsmag megvárja a virtuális gép indítását.

### 2. példa: a tanúsítványok használatával létrehozott virtuális gép létrehozása
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

Az első parancs az áruházból kapja a tanúsítványokat, és a $certs változóban tárolja őket.

A második parancs létrehoz egy virtuális gépet, amely a Windows operációs rendszert futtatja egy meglévő szolgáltatásból egy képről.
A WinRM HTTPS Listener alapértelmezés szerint engedélyezve van a virtuális gépen.
A parancs a *WaitForBoot* paramétert adja meg.
Ezért a parancsmag megvárja a virtuális gép indítását.
A parancs feltölti a WinRM tanúsítványát, és X509Certificates a szolgáltatott szolgáltatáshoz.

### 3. példa: a Linux operációs rendszert futtató virtuális gép létrehozása
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

A parancs létrehoz egy virtuális gépet, amely a Linux operációs rendszert egy képből futtatja.
Ezzel a paranccsal létrehoz egy szolgáltatást az új virtuális gép üzemeltetéséhez.
A parancs a szolgáltatás helyét adja meg.

### Példa 4: virtuális gép létrehozása és szolgáltatás létrehozása az új virtuális gép üzemeltetéséhez
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

Az első parancs a **Get-AzureLocation** parancsmag segítségével kapja meg a helyeket, majd a $Locations Array változóban tárolja őket.

A második parancs a **Get-AzureVMImage** parancsmag használatával érheti el a képeket, majd a $images Array változóban tárolja őket.

A végleges parancs létrehoz egy VirtualMachine25 nevű nagy virtuális gépet.
A virtuális gép futtatja a Windows operációs rendszert.
A $Images-ban található képek egyikén alapul.
A parancs létrehozza az új virtuális gép ContosoService03 nevű szolgáltatását.
A szolgáltatás $Locationsben található.

### Példa 5: a fenntartott IP-nevet tartalmazó virtuális gép létrehozása
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

Az első parancs a helyek elemre kerül, majd a $Locations Array változóban tárolja őket.

A második parancs elérhetővé válik a képek, majd a $Images Array változóban tárolja őket.

A végleges parancs egy VirtualMachine27 nevű virtuális gépet hoz létre a $Images egyik képének alapján.
A parancs létrehoz egy szolgáltatást a $Locationsban.
A virtuális gép rendelkezik egy fenntartott IP-névvel, amelyet korábban a $ipName változóban tároltak.

## PARAMÉTEREK

### -AdminUsername
Annak a rendszergazdai fióknak a felhasználónevét adja meg, amelyet a parancsmag a virtuális gépen hoz létre.

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AffinityGroup
A virtuális gép affinitása csoportját adja meg.
Ezt a paramétert vagy a *hely* paramétert csak akkor adja meg, ha a parancsmag Azure-szolgáltatást hoz létre a virtuális géphez.

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

### -AvailabilitySetName
Annak az elérhetőségi készletnek a nevét adja meg, amelyben ez a parancsmag létrehozta a virtuális gépet.

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

### -Tanúsítványok
A parancsmag által a szolgáltatás létrehozásához használt tanúsítványok listáját adja meg.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDataFile
A virtuális gép adatfájlját adja meg.
Ez a parancsmag Base64-ként kódolja a fájl tartalmát.
A fájlnak a 64 kilobyte-nál kisebbnek kell lennie.

Ha a vendég operációs rendszer a Windows operációs rendszer, ez a parancsmag a%SYSTEMDRIVE%\AzureData\CustomData.bin. nevű bináris fájlként menti ezeket az adatokat.

Ha a vendég operációs rendszer a Linuxot használja, a parancsmag a ovf-env.xml fájllal továbbítja az adatforrást.
A telepítés a fájlt a/var/lib/waagent könyvtárba másolja.
Az ügynök a Base64 kódolású adatot is tárolja a/var/lib/waagent/CustomData.-ban.

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

### -DisableGuestAgent
Jelzi, hogy ez a parancsmag kikapcsolja az infrastruktúrát szolgáltatásként (IaaS).

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

### -DisableWinRMHttps
Jelzi, hogy ez a parancsmag letiltja a Windows Remote Management (WinRM) szolgáltatást a HTTPS rendszeren.
A WinRM alapértelmezés szerint engedélyezve van a HTTPS felett.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSettings
Itt adhatja meg az új központi telepítő DNS-beállításait meghatározó DNS-kiszolgálói objektumok tömbjét.
**DnsServer** -objektum létrehozásához használja a **New-AzureDns** parancsmagot.

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Jelzi, hogy ez a parancsmag engedélyezi a WinRM HTTP-t.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Az operációs rendszer merevlemezének állomás-gyorsítótárazási módját adja meg.
Az érvényes értékek a következők: 

- ReadOnly
- ReadWrite

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

### -ImageName
Annak a lemeznek a neve, amelyet a parancsmag az operációs rendszer lemezének létrehozásához használ.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

### -InstanceSize
A példány méretének meghatározása.
Az érvényes értékek a következők: 

- ExtraSmall
- Kisvállalati
- Közepes
- Nagy
- ExtraLarge
- A5
- A6
- A7
- A8
- A9
- Basic_A0
- Basic_A1
- Basic_A2
- Basic_A3
- Basic_A4
- Standard_D1
- Standard_D2
- Standard_D3
- Standard_D4
- Standard_D11
- Standard_D12
- Standard_D13
- Standard_D14

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

### -Linux
Jelzi, hogy ez a parancsmag egy Linux-beli virtuális gépet hoz létre.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxUser
Annak a linuxos rendszergazdai fióknak a felhasználónevét adja meg, amelyet a parancsmag a virtuális gépen hoz létre.

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
A virtuális gépet működtető Azure-adatközpontot adja meg.
Ha ezt a paramétert adja meg, a parancsmag egy Azure-szolgáltatást hoz létre a megadott helyen.
Ezt a paramétert vagy a *AffinityGroup* paramétert csak akkor adja meg, ha a parancsmag Azure-szolgáltatást hoz létre a virtuális géphez.

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

### -MediaLocation
Annak az Azure-tárterületnek a helye, ahol a parancsmag létrehozza a virtuális gépek lemezeit.

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

### -Name (név)
Annak a virtuális gépnek a nevét adja meg, amelyre a parancsmag létrehozta.

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

### -NoExportPrivateKey
Azt jelzi, hogy ez a konfiguráció nem tölti fel a titkos kulcsot.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Azt jelzi, hogy ez a parancsmag nem hoz létre WinRM-végpontot a virtuális géphez.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Jelszó
A felügyeleti fiók jelszavát adja meg.

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

### -ReservedIPName
A fenntartott IP-nevet adja meg.

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
A DNS-névlekérdezéshez a teljesen minősített tartománynevet adja meg.

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

### -Szolgáltatásnév
Annak az új vagy meglévő Azure-szolgáltatásnak a nevét adja meg, amelyre a parancsmag hozzáadja az új virtuális gépet.

Ha új szolgáltatást ad meg, a parancsmagok létrehozzák.
Új szolgáltatás létrehozásához meg kell adnia a *helyet* vagy a *AffinityGroup* paramétert.

Ha meglévő szolgáltatást ad meg, ne adjon meg *helyet* vagy *AffinityGroup*.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHKeyPairs
Az SSH-kulcsok párjait adja meg.

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHPublicKeys
Az SSH-beli nyilvános kulcsokat adja meg.

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetNames
A virtuális gép alhálózatának neveinek egy tömbjét adja meg.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
A virtuális gép virtuális hálózatának nevét adja meg.

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
Jelzi, hogy ez a parancsmag várja, hogy a virtuális gép elérje az állam ReadyRole.
Ha a virtuális gép eléri az alábbi állapotok egyikét, a parancsmag nem működik: FailedStartingVM, ProvisioningFailed vagy ProvisioningTimeout.

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

### -Windows
Jelzi, hogy ez a parancsmag létrehoz egy Windows Virtual Machine-t.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
Azt a tanúsítványt adja meg, amelyet a parancsmag a WinRM-végpontokhoz társít.

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificates
A hosztolt szolgáltatásba telepített X509-tanúsítványok tömbjét adja meg.

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
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

[Get-AzureLocation](./Get-AzureLocation.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Új – AzureDns](./New-AzureDns.md)



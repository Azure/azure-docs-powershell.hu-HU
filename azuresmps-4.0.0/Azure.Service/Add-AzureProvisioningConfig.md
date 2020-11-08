---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016382"
---
# Add-AzureProvisioningConfig

## Áttekintés
Kiépítési konfigurációt ad az Azure Virtual Machine-nek.

## SZINTAXISA

### Windows (alapértelmezett)
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### WindowsDomain
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
Az **Add-AzureProvisioningConfig** parancsmag kiépítési konfigurációs adatokat hoz létre egy Azure Virtual Machine-konfigurációhoz.
A konfigurációs objektum segítségével virtuális gépet hozhat létre.

Ez a parancsmag különféle kiépítési konfigurációkat támogat, például különálló Windows-kiszolgálókat, a Windows-kiszolgálókat, amelyek az Active Directory-tartományhoz és a Linux-alapú kiszolgálókhoz csatlakoznak.

Ha Active Directory-tartományhoz csatlakoztatott kiszolgálót szeretne létrehozni, adja meg az Active Directory-tartomány teljes tartománynevét, valamint annak a tartománynak a hitelesítő adatait, akinek van engedélye a virtuális gépre a tartományhoz való csatlakozáshoz.

## Példák

### Példa 1: különálló virtuális gép létrehozása
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

Ez a parancs a virtuális gép konfigurációs objektumát a **New-AzureVMConfig** parancsmag használatával hozza létre.
A parancs a csővezeték-kezelő használatával továbbítja az objektumot az aktuális parancsmaghoz.
Az aktuális parancsmag a Windows operációs rendszert futtató virtuális gép kiépítési konfigurációját egészíti ki.
A konfiguráció a rendszergazda felhasználónevét és jelszavát tartalmazza.
A parancs átadja a konfigurációt a **New-AzureVM** parancsmagnak, amely a virtuális gépet hozza létre.

### 2. példa: tartomány létrehozása virtuális géphez
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

Ez a parancs létrehoz egy virtuális gép konfigurációs objektumát, majd átadja az aktuális parancsmagnak.
Az aktuális parancsmag egy virtuális gép kiépítési konfigurációjának hozzáadása a contoso-tartományhoz való csatlakozáshoz.
A parancs a virtuális géphez a tartományhoz való csatlakozáshoz szükséges felhasználónevet és jelszót tartalmazza.
A konfiguráció használatához a felhasználónak módosítania kell a felhasználó jelszavát az első bejelentkezéskor.
A parancs létrehozza a virtuális gépet a kiépítési objektum alapján.

### 3. példa: Linux-alapú virtuális gép létrehozása
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

Ez a parancs létrehoz egy virtuális gép konfigurációs objektumát, majd átadja az aktuális parancsmagnak.
A jelenlegi parancsmag a Linux operációs rendszert futtató virtuális gép kiépítési konfigurációját egészíti ki.
A konfiguráció a root felhasználónevét és jelszavát tartalmazza.
A parancs létrehozza a virtuális gépet a kiépítési objektum alapján.

### Példa 4: a WinRM tanúsítványait tartalmazó virtuális gép létrehozása
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Az első parancs tanúsítványokat kap egy tanúsítványtárolóból, majd a $certs Array változóban tárolja őket.

A második parancs létrehozza a virtuális gép konfigurációs objektumát, majd átadja az aktuális parancsmagnak.
Az aktuális parancsmag a Rendszerfelügyeleti webszolgáltatások tanúsítványait tartalmazó kiépítési konfigurációt ad hozzá.
A parancs létrehozza a virtuális gépet a kiépítési objektum alapján.

### Példa 5: virtuális gép létrehozása, amelyen a WinRM engedélyezve van a HTTP-ben
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Ez a parancs létrehoz egy virtuális gép konfigurációs objektumát, majd átadja az aktuális parancsmagnak.
Az aktuális parancsmag olyan kiépítési konfigurációt hoz létre, amelynek a WinRM engedélyezve van a HTTP-ben.
A parancs létrehozza a virtuális gépet a kiépítési objektum alapján.

### Példa 6: virtuális gép létrehozása, amelyen a WinRM szolgáltatás le van tiltva HTTPS felett
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Ez a parancs létrehoz egy virtuális gép konfigurációs objektumát, majd átadja az aktuális parancsmagnak.
Az aktuális parancsmag olyan kiépítési konfigurációt ad hozzá, amely letiltja a WinRM-t HTTPS-kapcsolaton keresztül.
A parancs létrehozza a virtuális gépet a kiépítési objektum alapján.

### 7. példa: virtuális gép létrehozása kulcs exportálása nélkül
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

Az első parancs tanúsítványokat kap egy tanúsítványtárolóból, majd a $certs Array változóban tárolja őket.

A második parancs létrehozza a virtuális gép konfigurációs objektumát, majd átadja az aktuális parancsmagnak.
Az aktuális parancsmag kiépíti a tanúsítványokat tartalmazó virtuális gépek kiépítési konfigurációját, és nem exportál személyes kulcsokat.
A parancs létrehozza a virtuális gépet a kiépítési objektum alapján.

## PARAMÉTEREK

### -AdminUsername
Annak a rendszergazdai fióknak a felhasználónevét adja meg, amelyet a konfiguráció a virtuális gépen hoz létre.

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

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tanúsítványok
Azon tanúsítványok halmazát adja meg, amelyeket a konfiguráció a virtuális gépre telepített.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
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

Ha a vendég operációs rendszer a Windows operációs rendszer, ez a konfiguráció a%SYSTEMDRIVE%\AzureData\CustomData.bin. nevű bináris fájlként menti ezeket az adatokat.

Ha a vendég operációs rendszer a Linuxot használja, ez a konfiguráció a ovf-env.xml fájllal továbbítja az adatokat.
A konfiguráció a fájlt a/var/lib/waagent könyvtárba másolja.
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

### -DisableAutomaticUpdates
Jelzi, hogy ez a konfiguráció letiltja az automatikus frissítéseket.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableGuestAgent
Azt jelzi, hogy ez a konfiguráció letiltja az infrastruktúrát a szolgáltatás (IaaS) Guest agentben.

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

### -DisableSSH
Jelzi, hogy ez a konfiguráció letiltja az SSH-t.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWinRMHttps
Jelzi, hogy ez a konfiguráció letiltja a Windows Remote Management (WinRM) szolgáltatást a HTTPS rendszeren.
A WinRM alapértelmezés szerint engedélyezve van a HTTPS felett.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tartomány
Annak a fióknak a nevét adja meg, amely rendelkezik engedéllyel a számítógép tartományba való felvételéhez.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainPassword
Annak a felhasználói fióknak a jelszava, amely engedéllyel rendelkezik a számítógép tartományba való felvételéhez.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainUserName
Annak a felhasználói fióknak a neve, amely engedéllyel rendelkezik a számítógép tartományba való felvételéhez.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Jelzi, hogy ez a beállítás engedélyezi a WinRM HTTP-t.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
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

### -JoinDomain
Annak a tartománynak a teljes tartományneve (FQDN), amelyhez csatlakozni szeretne.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
Azt jelzi, hogy ez a konfiguráció Linux-konfigurációt hoz létre.

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
Annak a linuxos rendszergazdai fióknak a felhasználónevét adja meg, amelyet a konfiguráció a virtuális gépen hoz létre.

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

### -MachineObjectOU
Annak a szervezeti egységnek (OU) a teljes tartománynevét adja meg, amelyben a konfiguráció létrehozta a számítógép fiókját.

```yaml
Type: String
Parameter Sets: WindowsDomain
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
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoRDPEndpoint
Azt jelzi, hogy ez a konfiguráció egy virtuális gépet hoz létre távoli asztali végpont nélkül.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHEndpoint
Azt jelzi, hogy ez a konfiguráció az SSH végpont nélküli virtuális gépet hoz létre.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHPassword
Azt jelzi, hogy ez a konfiguráció egy virtuális gépet hoz létre SSH-jelszó nélkül.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Jelzi, hogy ez a konfiguráció nem hoz létre WinRM-végpontot a virtuális géphez.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Jelszó
A rendszergazdai fiók jelszavát adja meg.

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

### -ResetPasswordOnFirstLogon
Azt jelzi, hogy a virtuális gépnek az első bejelentkezéskor módosítania kell a jelszót.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
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

### -Időzóna
A virtuális gép időzónáját adja meg, például Pacific standard Time vagy Kanada Central standard Time.

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Egy virtuálisgép-objektumot ad meg.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
Azt jelzi, hogy ez a konfiguráció egy különálló virtuális gépet hoz létre, amely a Windows operációs rendszert futtatja.

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

### -WindowsDomain
Jelzi, hogy ez a konfiguráció létrehoz egy Active Directory-tartományhoz csatlakozó Windows Servert.

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
Azt a tanúsítványt adja meg, amelyet ez a konfiguráció egy WinRM-végponthoz társít.

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
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
Parameter Sets: Windows, WindowsDomain
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

[Új – AzureVM](./New-AzureVM.md)

[Új – AzureVMConfig](./New-AzureVMConfig.md)



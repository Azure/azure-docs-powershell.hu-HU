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
# <span data-ttu-id="b5018-101">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="b5018-101">Add-AzureProvisioningConfig</span></span>

## <span data-ttu-id="b5018-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5018-102">SYNOPSIS</span></span>
<span data-ttu-id="b5018-103">Kiépítési konfigurációt ad az Azure Virtual Machine-nek.</span><span class="sxs-lookup"><span data-stu-id="b5018-103">Adds provisioning configuration for an Azure virtual machine.</span></span>

## <span data-ttu-id="b5018-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5018-104">SYNTAX</span></span>

### <span data-ttu-id="b5018-105">Windows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5018-105">Windows (Default)</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b5018-106">Linux</span><span class="sxs-lookup"><span data-stu-id="b5018-106">Linux</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b5018-107">WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="b5018-107">WindowsDomain</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b5018-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5018-108">DESCRIPTION</span></span>
<span data-ttu-id="b5018-109">Az **Add-AzureProvisioningConfig** parancsmag kiépítési konfigurációs adatokat hoz létre egy Azure Virtual Machine-konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="b5018-109">The **Add-AzureProvisioningConfig** cmdlet adds provisioning configuration information to an Azure virtual machine configuration.</span></span>
<span data-ttu-id="b5018-110">A konfigurációs objektum segítségével virtuális gépet hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="b5018-110">You can use the configuration object to create a virtual machine.</span></span>

<span data-ttu-id="b5018-111">Ez a parancsmag különféle kiépítési konfigurációkat támogat, például különálló Windows-kiszolgálókat, a Windows-kiszolgálókat, amelyek az Active Directory-tartományhoz és a Linux-alapú kiszolgálókhoz csatlakoznak.</span><span class="sxs-lookup"><span data-stu-id="b5018-111">This cmdlet supports different provisioning configurations, including standalone Windows servers, Windows servers joined to an Active Directory domain, and Linux-based servers.</span></span>

<span data-ttu-id="b5018-112">Ha Active Directory-tartományhoz csatlakoztatott kiszolgálót szeretne létrehozni, adja meg az Active Directory-tartomány teljes tartománynevét, valamint annak a tartománynak a hitelesítő adatait, akinek van engedélye a virtuális gépre a tartományhoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="b5018-112">To create an Active Directory domain joined server, specify the fully qualified domain name of the Active Directory domain and the domain credentials of a user who has permission to join the virtual machine to the domain.</span></span>

## <span data-ttu-id="b5018-113">Példák</span><span class="sxs-lookup"><span data-stu-id="b5018-113">EXAMPLES</span></span>

### <span data-ttu-id="b5018-114">Példa 1: különálló virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="b5018-114">Example 1: Create a standalone virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="b5018-115">Ez a parancs a virtuális gép konfigurációs objektumát a **New-AzureVMConfig** parancsmag használatával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="b5018-115">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="b5018-116">A parancs a csővezeték-kezelő használatával továbbítja az objektumot az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="b5018-116">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b5018-117">Az aktuális parancsmag a Windows operációs rendszert futtató virtuális gép kiépítési konfigurációját egészíti ki.</span><span class="sxs-lookup"><span data-stu-id="b5018-117">The current cmdlet adds provisioning configuration for a virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="b5018-118">A konfiguráció a rendszergazda felhasználónevét és jelszavát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b5018-118">The configuration includes the administrator user name and password.</span></span>
<span data-ttu-id="b5018-119">A parancs átadja a konfigurációt a **New-AzureVM** parancsmagnak, amely a virtuális gépet hozza létre.</span><span class="sxs-lookup"><span data-stu-id="b5018-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="b5018-120">2. példa: tartomány létrehozása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="b5018-120">Example 2: Create a domain joined virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="b5018-121">Ez a parancs létrehoz egy virtuális gép konfigurációs objektumát, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b5018-121">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b5018-122">Az aktuális parancsmag egy virtuális gép kiépítési konfigurációjának hozzáadása a contoso-tartományhoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="b5018-122">The current cmdlet adds provisioning configuration for a virtual machine to be joined with the contoso domain.</span></span>
<span data-ttu-id="b5018-123">A parancs a virtuális géphez a tartományhoz való csatlakozáshoz szükséges felhasználónevet és jelszót tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b5018-123">The command includes user name and password necessary to join the virtual machine to the domain.</span></span>
<span data-ttu-id="b5018-124">A konfiguráció használatához a felhasználónak módosítania kell a felhasználó jelszavát az első bejelentkezéskor.</span><span class="sxs-lookup"><span data-stu-id="b5018-124">The configuration requires the user to change the user password at the first logon.</span></span>
<span data-ttu-id="b5018-125">A parancs létrehozza a virtuális gépet a kiépítési objektum alapján.</span><span class="sxs-lookup"><span data-stu-id="b5018-125">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="b5018-126">3. példa: Linux-alapú virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="b5018-126">Example 3: Create a Linux-based virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="b5018-127">Ez a parancs létrehoz egy virtuális gép konfigurációs objektumát, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b5018-127">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b5018-128">A jelenlegi parancsmag a Linux operációs rendszert futtató virtuális gép kiépítési konfigurációját egészíti ki.</span><span class="sxs-lookup"><span data-stu-id="b5018-128">The current cmdlet adds provisioning configuration for a virtual machine that runs the Linux operating system.</span></span>
<span data-ttu-id="b5018-129">A konfiguráció a root felhasználónevét és jelszavát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b5018-129">The configuration includes the root user name and password.</span></span>
<span data-ttu-id="b5018-130">A parancs létrehozza a virtuális gépet a kiépítési objektum alapján.</span><span class="sxs-lookup"><span data-stu-id="b5018-130">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="b5018-131">Példa 4: a WinRM tanúsítványait tartalmazó virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="b5018-131">Example 4: Create a virtual machine that includes certificates for WinRM</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="b5018-132">Az első parancs tanúsítványokat kap egy tanúsítványtárolóból, majd a $certs Array változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="b5018-132">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="b5018-133">A második parancs létrehozza a virtuális gép konfigurációs objektumát, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b5018-133">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b5018-134">Az aktuális parancsmag a Rendszerfelügyeleti webszolgáltatások tanúsítványait tartalmazó kiépítési konfigurációt ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="b5018-134">The current cmdlet adds provisioning configuration that includes certificates for WinRM.</span></span>
<span data-ttu-id="b5018-135">A parancs létrehozza a virtuális gépet a kiépítési objektum alapján.</span><span class="sxs-lookup"><span data-stu-id="b5018-135">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="b5018-136">Példa 5: virtuális gép létrehozása, amelyen a WinRM engedélyezve van a HTTP-ben</span><span class="sxs-lookup"><span data-stu-id="b5018-136">Example 5: Create a virtual machine that has WinRM enabled over HTTP</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="b5018-137">Ez a parancs létrehoz egy virtuális gép konfigurációs objektumát, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b5018-137">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b5018-138">Az aktuális parancsmag olyan kiépítési konfigurációt hoz létre, amelynek a WinRM engedélyezve van a HTTP-ben.</span><span class="sxs-lookup"><span data-stu-id="b5018-138">The current cmdlet adds provisioning configuration that has WinRM enabled over HTTP.</span></span>
<span data-ttu-id="b5018-139">A parancs létrehozza a virtuális gépet a kiépítési objektum alapján.</span><span class="sxs-lookup"><span data-stu-id="b5018-139">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="b5018-140">Példa 6: virtuális gép létrehozása, amelyen a WinRM szolgáltatás le van tiltva HTTPS felett</span><span class="sxs-lookup"><span data-stu-id="b5018-140">Example 6: Create a virtual machine that has WinRM disabled over HTTPS</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="b5018-141">Ez a parancs létrehoz egy virtuális gép konfigurációs objektumát, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b5018-141">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b5018-142">Az aktuális parancsmag olyan kiépítési konfigurációt ad hozzá, amely letiltja a WinRM-t HTTPS-kapcsolaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="b5018-142">The current cmdlet adds provisioning configuration that disables WinRM over HTTPS.</span></span>
<span data-ttu-id="b5018-143">A parancs létrehozza a virtuális gépet a kiépítési objektum alapján.</span><span class="sxs-lookup"><span data-stu-id="b5018-143">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="b5018-144">7. példa: virtuális gép létrehozása kulcs exportálása nélkül</span><span class="sxs-lookup"><span data-stu-id="b5018-144">Example 7: Create a virtual machine with no key export</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="b5018-145">Az első parancs tanúsítványokat kap egy tanúsítványtárolóból, majd a $certs Array változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="b5018-145">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="b5018-146">A második parancs létrehozza a virtuális gép konfigurációs objektumát, majd átadja az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b5018-146">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b5018-147">Az aktuális parancsmag kiépíti a tanúsítványokat tartalmazó virtuális gépek kiépítési konfigurációját, és nem exportál személyes kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="b5018-147">The current cmdlet adds provisioning configuration for a virtual machine that includes certificates and does not export private keys.</span></span>
<span data-ttu-id="b5018-148">A parancs létrehozza a virtuális gépet a kiépítési objektum alapján.</span><span class="sxs-lookup"><span data-stu-id="b5018-148">The command creates the virtual machine based on the provisioning object.</span></span>

## <span data-ttu-id="b5018-149">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5018-149">PARAMETERS</span></span>

### <span data-ttu-id="b5018-150">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="b5018-150">-AdminUsername</span></span>
<span data-ttu-id="b5018-151">Annak a rendszergazdai fióknak a felhasználónevét adja meg, amelyet a konfiguráció a virtuális gépen hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5018-151">Specifies the user name of the Administrator account that this configuration creates on the virtual machine.</span></span>

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

### <span data-ttu-id="b5018-152">-Tanúsítványok</span><span class="sxs-lookup"><span data-stu-id="b5018-152">-Certificates</span></span>
<span data-ttu-id="b5018-153">Azon tanúsítványok halmazát adja meg, amelyeket a konfiguráció a virtuális gépre telepített.</span><span class="sxs-lookup"><span data-stu-id="b5018-153">Specifies a set of certificates that this configuration installs on the virtual machine.</span></span>

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

### <span data-ttu-id="b5018-154">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="b5018-154">-CustomDataFile</span></span>
<span data-ttu-id="b5018-155">A virtuális gép adatfájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5018-155">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="b5018-156">Ez a parancsmag Base64-ként kódolja a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="b5018-156">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="b5018-157">A fájlnak a 64 kilobyte-nál kisebbnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="b5018-157">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="b5018-158">Ha a vendég operációs rendszer a Windows operációs rendszer, ez a konfiguráció a%SYSTEMDRIVE%\AzureData\CustomData.bin. nevű bináris fájlként menti ezeket az adatokat.</span><span class="sxs-lookup"><span data-stu-id="b5018-158">If the guest operating system is the Windows operating system, this configuration saves this data as a binary file named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="b5018-159">Ha a vendég operációs rendszer a Linuxot használja, ez a konfiguráció a ovf-env.xml fájllal továbbítja az adatokat.</span><span class="sxs-lookup"><span data-stu-id="b5018-159">If the guest operating system is Linux, this configuration passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="b5018-160">A konfiguráció a fájlt a/var/lib/waagent könyvtárba másolja.</span><span class="sxs-lookup"><span data-stu-id="b5018-160">Configuration copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="b5018-161">Az ügynök a Base64 kódolású adatot is tárolja a/var/lib/waagent/CustomData.-ban.</span><span class="sxs-lookup"><span data-stu-id="b5018-161">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="b5018-162">-DisableAutomaticUpdates</span><span class="sxs-lookup"><span data-stu-id="b5018-162">-DisableAutomaticUpdates</span></span>
<span data-ttu-id="b5018-163">Jelzi, hogy ez a konfiguráció letiltja az automatikus frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="b5018-163">Indicates that this configuration disables automatic updates.</span></span>

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

### <span data-ttu-id="b5018-164">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="b5018-164">-DisableGuestAgent</span></span>
<span data-ttu-id="b5018-165">Azt jelzi, hogy ez a konfiguráció letiltja az infrastruktúrát a szolgáltatás (IaaS) Guest agentben.</span><span class="sxs-lookup"><span data-stu-id="b5018-165">Indicates that this configuration disables the infrastructure as a service (IaaS) guest agent.</span></span>

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

### <span data-ttu-id="b5018-166">-DisableSSH</span><span class="sxs-lookup"><span data-stu-id="b5018-166">-DisableSSH</span></span>
<span data-ttu-id="b5018-167">Jelzi, hogy ez a konfiguráció letiltja az SSH-t.</span><span class="sxs-lookup"><span data-stu-id="b5018-167">Indicates that this configuration disables SSH.</span></span>

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

### <span data-ttu-id="b5018-168">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="b5018-168">-DisableWinRMHttps</span></span>
<span data-ttu-id="b5018-169">Jelzi, hogy ez a konfiguráció letiltja a Windows Remote Management (WinRM) szolgáltatást a HTTPS rendszeren.</span><span class="sxs-lookup"><span data-stu-id="b5018-169">Indicates that this configuration disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="b5018-170">A WinRM alapértelmezés szerint engedélyezve van a HTTPS felett.</span><span class="sxs-lookup"><span data-stu-id="b5018-170">By default, WinRM is enabled over HTTPS.</span></span>

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

### <span data-ttu-id="b5018-171">-Tartomány</span><span class="sxs-lookup"><span data-stu-id="b5018-171">-Domain</span></span>
<span data-ttu-id="b5018-172">Annak a fióknak a nevét adja meg, amely rendelkezik engedéllyel a számítógép tartományba való felvételéhez.</span><span class="sxs-lookup"><span data-stu-id="b5018-172">Specifies the name of the domain of the account that has permission to add the computer to a domain.</span></span>

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

### <span data-ttu-id="b5018-173">-DomainPassword</span><span class="sxs-lookup"><span data-stu-id="b5018-173">-DomainPassword</span></span>
<span data-ttu-id="b5018-174">Annak a felhasználói fióknak a jelszava, amely engedéllyel rendelkezik a számítógép tartományba való felvételéhez.</span><span class="sxs-lookup"><span data-stu-id="b5018-174">Specifies the password of the user account that has permission to add the computer to a domain.</span></span>

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

### <span data-ttu-id="b5018-175">-DomainUserName</span><span class="sxs-lookup"><span data-stu-id="b5018-175">-DomainUserName</span></span>
<span data-ttu-id="b5018-176">Annak a felhasználói fióknak a neve, amely engedéllyel rendelkezik a számítógép tartományba való felvételéhez.</span><span class="sxs-lookup"><span data-stu-id="b5018-176">Specifies the name of the user account that has permission to add the computer to a domain.</span></span>

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

### <span data-ttu-id="b5018-177">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="b5018-177">-EnableWinRMHttp</span></span>
<span data-ttu-id="b5018-178">Jelzi, hogy ez a beállítás engedélyezi a WinRM HTTP-t.</span><span class="sxs-lookup"><span data-stu-id="b5018-178">Indicates that this configuration enables WinRM over HTTP.</span></span>

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

### <span data-ttu-id="b5018-179">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b5018-179">-InformationAction</span></span>
<span data-ttu-id="b5018-180">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="b5018-180">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b5018-181">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b5018-181">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5018-182">Folytassa</span><span class="sxs-lookup"><span data-stu-id="b5018-182">Continue</span></span>
- <span data-ttu-id="b5018-183">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="b5018-183">Ignore</span></span>
- <span data-ttu-id="b5018-184">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="b5018-184">Inquire</span></span>
- <span data-ttu-id="b5018-185">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b5018-185">SilentlyContinue</span></span>
- <span data-ttu-id="b5018-186">állj</span><span class="sxs-lookup"><span data-stu-id="b5018-186">Stop</span></span>
- <span data-ttu-id="b5018-187">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="b5018-187">Suspend</span></span>

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

### <span data-ttu-id="b5018-188">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b5018-188">-InformationVariable</span></span>
<span data-ttu-id="b5018-189">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b5018-189">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b5018-190">-JoinDomain</span><span class="sxs-lookup"><span data-stu-id="b5018-190">-JoinDomain</span></span>
<span data-ttu-id="b5018-191">Annak a tartománynak a teljes tartományneve (FQDN), amelyhez csatlakozni szeretne.</span><span class="sxs-lookup"><span data-stu-id="b5018-191">Specifies the fully qualified domain name (FQDN) of the domain to join.</span></span>

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

### <span data-ttu-id="b5018-192">-Linux</span><span class="sxs-lookup"><span data-stu-id="b5018-192">-Linux</span></span>
<span data-ttu-id="b5018-193">Azt jelzi, hogy ez a konfiguráció Linux-konfigurációt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5018-193">Indicates that this configuration creates a Linux configuration.</span></span>

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

### <span data-ttu-id="b5018-194">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="b5018-194">-LinuxUser</span></span>
<span data-ttu-id="b5018-195">Annak a linuxos rendszergazdai fióknak a felhasználónevét adja meg, amelyet a konfiguráció a virtuális gépen hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5018-195">Specifies the user name of the Linux administrative account that this configuration creates on the virtual machine.</span></span>

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

### <span data-ttu-id="b5018-196">-MachineObjectOU</span><span class="sxs-lookup"><span data-stu-id="b5018-196">-MachineObjectOU</span></span>
<span data-ttu-id="b5018-197">Annak a szervezeti egységnek (OU) a teljes tartománynevét adja meg, amelyben a konfiguráció létrehozta a számítógép fiókját.</span><span class="sxs-lookup"><span data-stu-id="b5018-197">Specifies the fully qualified name of the organizational unit (OU) in which the configuration creates the computer account.</span></span>

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

### <span data-ttu-id="b5018-198">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="b5018-198">-NoExportPrivateKey</span></span>
<span data-ttu-id="b5018-199">Azt jelzi, hogy ez a konfiguráció nem tölti fel a titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="b5018-199">Indicates that this configuration does not upload the private key.</span></span>

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

### <span data-ttu-id="b5018-200">-NoRDPEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5018-200">-NoRDPEndpoint</span></span>
<span data-ttu-id="b5018-201">Azt jelzi, hogy ez a konfiguráció egy virtuális gépet hoz létre távoli asztali végpont nélkül.</span><span class="sxs-lookup"><span data-stu-id="b5018-201">Indicates that this configuration creates a virtual machine without a remote desktop endpoint.</span></span>

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

### <span data-ttu-id="b5018-202">-NoSSHEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5018-202">-NoSSHEndpoint</span></span>
<span data-ttu-id="b5018-203">Azt jelzi, hogy ez a konfiguráció az SSH végpont nélküli virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5018-203">Indicates that this configuration creates a virtual machine without an SSH endpoint.</span></span>

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

### <span data-ttu-id="b5018-204">-NoSSHPassword</span><span class="sxs-lookup"><span data-stu-id="b5018-204">-NoSSHPassword</span></span>
<span data-ttu-id="b5018-205">Azt jelzi, hogy ez a konfiguráció egy virtuális gépet hoz létre SSH-jelszó nélkül.</span><span class="sxs-lookup"><span data-stu-id="b5018-205">Indicates that this configuration creates a virtual machine without an SSH password.</span></span>

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

### <span data-ttu-id="b5018-206">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5018-206">-NoWinRMEndpoint</span></span>
<span data-ttu-id="b5018-207">Jelzi, hogy ez a konfiguráció nem hoz létre WinRM-végpontot a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="b5018-207">Indicates that this configuration does not add a WinRM endpoint for the virtual machine.</span></span>

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

### <span data-ttu-id="b5018-208">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="b5018-208">-Password</span></span>
<span data-ttu-id="b5018-209">A rendszergazdai fiók jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5018-209">Specifies the password of the administrator account.</span></span>

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

### <span data-ttu-id="b5018-210">-Profil</span><span class="sxs-lookup"><span data-stu-id="b5018-210">-Profile</span></span>
<span data-ttu-id="b5018-211">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b5018-211">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5018-212">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b5018-212">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5018-213">-ResetPasswordOnFirstLogon</span><span class="sxs-lookup"><span data-stu-id="b5018-213">-ResetPasswordOnFirstLogon</span></span>
<span data-ttu-id="b5018-214">Azt jelzi, hogy a virtuális gépnek az első bejelentkezéskor módosítania kell a jelszót.</span><span class="sxs-lookup"><span data-stu-id="b5018-214">Indicates that the virtual machine requires the user to change the password at the first logon.</span></span>

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

### <span data-ttu-id="b5018-215">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="b5018-215">-SSHKeyPairs</span></span>
<span data-ttu-id="b5018-216">Az SSH-kulcsok párjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5018-216">Specifies SSH key pairs.</span></span>

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

### <span data-ttu-id="b5018-217">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="b5018-217">-SSHPublicKeys</span></span>
<span data-ttu-id="b5018-218">Az SSH-beli nyilvános kulcsokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5018-218">Specifies SSH public keys.</span></span>

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

### <span data-ttu-id="b5018-219">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="b5018-219">-TimeZone</span></span>
<span data-ttu-id="b5018-220">A virtuális gép időzónáját adja meg, például Pacific standard Time vagy Kanada Central standard Time.</span><span class="sxs-lookup"><span data-stu-id="b5018-220">Specifies the time zone for the virtual machine, for example, Pacific Standard Time or Canada Central Standard Time.</span></span>

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

### <span data-ttu-id="b5018-221">-VM</span><span class="sxs-lookup"><span data-stu-id="b5018-221">-VM</span></span>
<span data-ttu-id="b5018-222">Egy virtuálisgép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b5018-222">Specifies a virtual machine object.</span></span>

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

### <span data-ttu-id="b5018-223">-Windows</span><span class="sxs-lookup"><span data-stu-id="b5018-223">-Windows</span></span>
<span data-ttu-id="b5018-224">Azt jelzi, hogy ez a konfiguráció egy különálló virtuális gépet hoz létre, amely a Windows operációs rendszert futtatja.</span><span class="sxs-lookup"><span data-stu-id="b5018-224">Indicates that this configuration creates a standalone virtual machine that runs the Windows operating system.</span></span>

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

### <span data-ttu-id="b5018-225">-WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="b5018-225">-WindowsDomain</span></span>
<span data-ttu-id="b5018-226">Jelzi, hogy ez a konfiguráció létrehoz egy Active Directory-tartományhoz csatlakozó Windows Servert.</span><span class="sxs-lookup"><span data-stu-id="b5018-226">Indicates that this configuration creates Windows server that is joined to an Active Directory domain.</span></span>

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

### <span data-ttu-id="b5018-227">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="b5018-227">-WinRMCertificate</span></span>
<span data-ttu-id="b5018-228">Azt a tanúsítványt adja meg, amelyet ez a konfiguráció egy WinRM-végponthoz társít.</span><span class="sxs-lookup"><span data-stu-id="b5018-228">Specifies a certificate that this configuration associates to a WinRM endpoint.</span></span>

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

### <span data-ttu-id="b5018-229">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="b5018-229">-X509Certificates</span></span>
<span data-ttu-id="b5018-230">A hosztolt szolgáltatásba telepített X509-tanúsítványok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5018-230">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

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

### <span data-ttu-id="b5018-231">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5018-231">CommonParameters</span></span>
<span data-ttu-id="b5018-232">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5018-232">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5018-233">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5018-233">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5018-234">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5018-234">INPUTS</span></span>

## <span data-ttu-id="b5018-235">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5018-235">OUTPUTS</span></span>

## <span data-ttu-id="b5018-236">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5018-236">NOTES</span></span>

## <span data-ttu-id="b5018-237">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5018-237">RELATED LINKS</span></span>

[<span data-ttu-id="b5018-238">Új – AzureVM</span><span class="sxs-lookup"><span data-stu-id="b5018-238">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="b5018-239">Új – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="b5018-239">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)



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
# <span data-ttu-id="8cc9c-101">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="8cc9c-101">New-AzureQuickVM</span></span>

## <span data-ttu-id="8cc9c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8cc9c-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc9c-103">Azure virtuális gépet konfigurál és hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-103">Configures and creates an Azure virtual machine.</span></span>

## <span data-ttu-id="8cc9c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8cc9c-104">SYNTAX</span></span>

### <span data-ttu-id="8cc9c-105">Windows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8cc9c-105">Windows (Default)</span></span>
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

### <span data-ttu-id="8cc9c-106">Linux</span><span class="sxs-lookup"><span data-stu-id="8cc9c-106">Linux</span></span>
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8cc9c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8cc9c-107">DESCRIPTION</span></span>
<span data-ttu-id="8cc9c-108">A **New-AzureQuickVM** parancsmag egy Azure virtuális gépet állít be és hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-108">The **New-AzureQuickVM** cmdlet configures and creates an Azure virtual machine.</span></span>
<span data-ttu-id="8cc9c-109">Ez a parancsmag a virtuális gépet egy meglévő Azure-szolgáltatásba telepítheti.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-109">This cmdlet can deploy a virtual machine into an existing Azure service.</span></span>
<span data-ttu-id="8cc9c-110">Ez a parancsmag egy olyan Azure-szolgáltatást is létrehozhat, amely az új virtuális gépet tárolja.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-110">This cmdlet can alternatively create an Azure service that hosts the new virtual machine.</span></span>

## <span data-ttu-id="8cc9c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8cc9c-111">EXAMPLES</span></span>

### <span data-ttu-id="8cc9c-112">Példa 1: virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="8cc9c-112">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

<span data-ttu-id="8cc9c-113">Ez a parancs létrehoz egy virtuális gépet, amely futtatja a Windows operációs rendszert egy meglévő szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-113">This command creates a virtual machine that runs the Windows operating system in an existing service.</span></span>
<span data-ttu-id="8cc9c-114">A parancsmag a megadott képen a virtuális gépet alapozza.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-114">The cmdlet bases the virtual machine on the specified image.</span></span>
<span data-ttu-id="8cc9c-115">A parancs a *WaitForBoot* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-115">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="8cc9c-116">Ezért a parancsmag megvárja a virtuális gép indítását.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-116">Therefore, the cmdlet waits for the virtual machine to start.</span></span>

### <span data-ttu-id="8cc9c-117">2. példa: a tanúsítványok használatával létrehozott virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="8cc9c-117">Example 2: Create a virtual machine that by using certificates</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

<span data-ttu-id="8cc9c-118">Az első parancs az áruházból kapja a tanúsítványokat, és a $certs változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-118">The first command gets certificates from a store, and stores them in the $certs variable.</span></span>

<span data-ttu-id="8cc9c-119">A második parancs létrehoz egy virtuális gépet, amely a Windows operációs rendszert futtatja egy meglévő szolgáltatásból egy képről.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-119">The second command creates a virtual machine that runs the Windows operating system in an existing service from an image.</span></span>
<span data-ttu-id="8cc9c-120">A WinRM HTTPS Listener alapértelmezés szerint engedélyezve van a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-120">By default, WinRM Https listener is enabled on the virtual machine.</span></span>
<span data-ttu-id="8cc9c-121">A parancs a *WaitForBoot* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-121">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="8cc9c-122">Ezért a parancsmag megvárja a virtuális gép indítását.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-122">Therefore, the cmdlet waits for the virtual machine to start.</span></span>
<span data-ttu-id="8cc9c-123">A parancs feltölti a WinRM tanúsítványát, és X509Certificates a szolgáltatott szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-123">The command uploads a WinRM Certificate and X509Certificates to the hosted service.</span></span>

### <span data-ttu-id="8cc9c-124">3. példa: a Linux operációs rendszert futtató virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="8cc9c-124">Example 3: Create a virtual machine that runs the Linux operating system</span></span>
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

<span data-ttu-id="8cc9c-125">A parancs létrehoz egy virtuális gépet, amely a Linux operációs rendszert egy képből futtatja.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-125">This command creates a virtual machine that runs the Linux operating system from an image.</span></span>
<span data-ttu-id="8cc9c-126">Ezzel a paranccsal létrehoz egy szolgáltatást az új virtuális gép üzemeltetéséhez.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-126">This command creates a service to host the new virtual machine.</span></span>
<span data-ttu-id="8cc9c-127">A parancs a szolgáltatás helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-127">The command specifies a location for the service.</span></span>

### <span data-ttu-id="8cc9c-128">Példa 4: virtuális gép létrehozása és szolgáltatás létrehozása az új virtuális gép üzemeltetéséhez</span><span class="sxs-lookup"><span data-stu-id="8cc9c-128">Example 4: Create a virtual machine and create a service to host the new virtual machine</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

<span data-ttu-id="8cc9c-129">Az első parancs a **Get-AzureLocation** parancsmag segítségével kapja meg a helyeket, majd a $Locations Array változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-129">The first command gets locations by using the **Get-AzureLocation** cmdlet, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="8cc9c-130">A második parancs a **Get-AzureVMImage** parancsmag használatával érheti el a képeket, majd a $images Array változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-130">The second command gets available images by using the **Get-AzureVMImage** cmdlet, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="8cc9c-131">A végleges parancs létrehoz egy VirtualMachine25 nevű nagy virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-131">The final command creates a large virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="8cc9c-132">A virtuális gép futtatja a Windows operációs rendszert.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-132">The virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="8cc9c-133">A $Images-ban található képek egyikén alapul.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-133">It is based on one of the images in $Images.</span></span>
<span data-ttu-id="8cc9c-134">A parancs létrehozza az új virtuális gép ContosoService03 nevű szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-134">The command creates a service named ContosoService03 for the new virtual machine.</span></span>
<span data-ttu-id="8cc9c-135">A szolgáltatás $Locationsben található.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-135">The service is in a location in $Locations.</span></span>

### <span data-ttu-id="8cc9c-136">Példa 5: a fenntartott IP-nevet tartalmazó virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="8cc9c-136">Example 5: Create a virtual machine that has a reserved IP name</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

<span data-ttu-id="8cc9c-137">Az első parancs a helyek elemre kerül, majd a $Locations Array változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-137">The first command gets locations, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="8cc9c-138">A második parancs elérhetővé válik a képek, majd a $Images Array változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-138">The second command gets available images, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="8cc9c-139">A végleges parancs egy VirtualMachine27 nevű virtuális gépet hoz létre a $Images egyik képének alapján.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-139">The final command creates a virtual machine named VirtualMachine27 based on one of the images in $Images.</span></span>
<span data-ttu-id="8cc9c-140">A parancs létrehoz egy szolgáltatást a $Locationsban.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-140">The command creates a service in a location in $Locations.</span></span>
<span data-ttu-id="8cc9c-141">A virtuális gép rendelkezik egy fenntartott IP-névvel, amelyet korábban a $ipName változóban tároltak.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-141">The virtual machine has a reserved IP name, previously stored in the $ipName variable.</span></span>

## <span data-ttu-id="8cc9c-142">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8cc9c-142">PARAMETERS</span></span>

### <span data-ttu-id="8cc9c-143">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="8cc9c-143">-AdminUsername</span></span>
<span data-ttu-id="8cc9c-144">Annak a rendszergazdai fióknak a felhasználónevét adja meg, amelyet a parancsmag a virtuális gépen hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-144">Specifies the user name of the Administrator account that this cmdlet creates on the virtual machine.</span></span>

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

### <span data-ttu-id="8cc9c-145">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="8cc9c-145">-AffinityGroup</span></span>
<span data-ttu-id="8cc9c-146">A virtuális gép affinitása csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-146">Specifies the affinity group for the virtual machine.</span></span>
<span data-ttu-id="8cc9c-147">Ezt a paramétert vagy a *hely* paramétert csak akkor adja meg, ha a parancsmag Azure-szolgáltatást hoz létre a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-147">Specify this parameter or the *Location* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="8cc9c-148">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="8cc9c-148">-AvailabilitySetName</span></span>
<span data-ttu-id="8cc9c-149">Annak az elérhetőségi készletnek a nevét adja meg, amelyben ez a parancsmag létrehozta a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-149">Specifies the name of the availability set in which this cmdlet creates the virtual machine.</span></span>

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

### <span data-ttu-id="8cc9c-150">-Tanúsítványok</span><span class="sxs-lookup"><span data-stu-id="8cc9c-150">-Certificates</span></span>
<span data-ttu-id="8cc9c-151">A parancsmag által a szolgáltatás létrehozásához használt tanúsítványok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-151">Specifies a list of certificates that this cmdlet uses to create the service.</span></span>

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

### <span data-ttu-id="8cc9c-152">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="8cc9c-152">-CustomDataFile</span></span>
<span data-ttu-id="8cc9c-153">A virtuális gép adatfájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-153">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="8cc9c-154">Ez a parancsmag Base64-ként kódolja a fájl tartalmát.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-154">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="8cc9c-155">A fájlnak a 64 kilobyte-nál kisebbnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-155">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="8cc9c-156">Ha a vendég operációs rendszer a Windows operációs rendszer, ez a parancsmag a%SYSTEMDRIVE%\AzureData\CustomData.bin. nevű bináris fájlként menti ezeket az adatokat.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-156">If the guest operating system is the Windows operating system, this cmdlet saves this data as a binary file that is named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="8cc9c-157">Ha a vendég operációs rendszer a Linuxot használja, a parancsmag a ovf-env.xml fájllal továbbítja az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-157">If the guest operating system is Linux, this cmdlet passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="8cc9c-158">A telepítés a fájlt a/var/lib/waagent könyvtárba másolja.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-158">Installation copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="8cc9c-159">Az ügynök a Base64 kódolású adatot is tárolja a/var/lib/waagent/CustomData.-ban.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-159">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="8cc9c-160">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="8cc9c-160">-DisableGuestAgent</span></span>
<span data-ttu-id="8cc9c-161">Jelzi, hogy ez a parancsmag kikapcsolja az infrastruktúrát szolgáltatásként (IaaS).</span><span class="sxs-lookup"><span data-stu-id="8cc9c-161">Indicates that this cmdlet disables the infrastructure as a service (IaaS) provision guest agent.</span></span>

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

### <span data-ttu-id="8cc9c-162">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="8cc9c-162">-DisableWinRMHttps</span></span>
<span data-ttu-id="8cc9c-163">Jelzi, hogy ez a parancsmag letiltja a Windows Remote Management (WinRM) szolgáltatást a HTTPS rendszeren.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-163">Indicates that this cmdlet disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="8cc9c-164">A WinRM alapértelmezés szerint engedélyezve van a HTTPS felett.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-164">By default, WinRM is enabled over HTTPS.</span></span>

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

### <span data-ttu-id="8cc9c-165">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="8cc9c-165">-DnsSettings</span></span>
<span data-ttu-id="8cc9c-166">Itt adhatja meg az új központi telepítő DNS-beállításait meghatározó DNS-kiszolgálói objektumok tömbjét.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-166">Specifies an array of DNS server objects that defines the DNS settings for the new deployment.</span></span>
<span data-ttu-id="8cc9c-167">**DnsServer** -objektum létrehozásához használja a **New-AzureDns** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-167">To create a **DnsServer** object, use the **New-AzureDns** cmdlet.</span></span>

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

### <span data-ttu-id="8cc9c-168">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="8cc9c-168">-EnableWinRMHttp</span></span>
<span data-ttu-id="8cc9c-169">Jelzi, hogy ez a parancsmag engedélyezi a WinRM HTTP-t.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-169">Indicates that this cmdlet enables WinRM over HTTP.</span></span>

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

### <span data-ttu-id="8cc9c-170">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="8cc9c-170">-HostCaching</span></span>
<span data-ttu-id="8cc9c-171">Az operációs rendszer merevlemezének állomás-gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-171">Specifies the host caching mode for the operating system disk.</span></span>
<span data-ttu-id="8cc9c-172">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="8cc9c-172">Valid values are:</span></span> 

- <span data-ttu-id="8cc9c-173">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8cc9c-173">ReadOnly</span></span>
- <span data-ttu-id="8cc9c-174">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8cc9c-174">ReadWrite</span></span>

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

### <span data-ttu-id="8cc9c-175">-ImageName</span><span class="sxs-lookup"><span data-stu-id="8cc9c-175">-ImageName</span></span>
<span data-ttu-id="8cc9c-176">Annak a lemeznek a neve, amelyet a parancsmag az operációs rendszer lemezének létrehozásához használ.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-176">Specifies the name of the disk image this cmdlet uses to create the operating system disk.</span></span>

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

### <span data-ttu-id="8cc9c-177">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8cc9c-177">-InformationAction</span></span>
<span data-ttu-id="8cc9c-178">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-178">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8cc9c-179">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8cc9c-179">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8cc9c-180">Folytassa</span><span class="sxs-lookup"><span data-stu-id="8cc9c-180">Continue</span></span>
- <span data-ttu-id="8cc9c-181">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="8cc9c-181">Ignore</span></span>
- <span data-ttu-id="8cc9c-182">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="8cc9c-182">Inquire</span></span>
- <span data-ttu-id="8cc9c-183">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8cc9c-183">SilentlyContinue</span></span>
- <span data-ttu-id="8cc9c-184">állj</span><span class="sxs-lookup"><span data-stu-id="8cc9c-184">Stop</span></span>
- <span data-ttu-id="8cc9c-185">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="8cc9c-185">Suspend</span></span>

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

### <span data-ttu-id="8cc9c-186">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8cc9c-186">-InformationVariable</span></span>
<span data-ttu-id="8cc9c-187">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-187">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8cc9c-188">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="8cc9c-188">-InstanceSize</span></span>
<span data-ttu-id="8cc9c-189">A példány méretének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-189">Specifies the size of the instance.</span></span>
<span data-ttu-id="8cc9c-190">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="8cc9c-190">Valid values are:</span></span> 

- <span data-ttu-id="8cc9c-191">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="8cc9c-191">ExtraSmall</span></span>
- <span data-ttu-id="8cc9c-192">Kisvállalati</span><span class="sxs-lookup"><span data-stu-id="8cc9c-192">Small</span></span>
- <span data-ttu-id="8cc9c-193">Közepes</span><span class="sxs-lookup"><span data-stu-id="8cc9c-193">Medium</span></span>
- <span data-ttu-id="8cc9c-194">Nagy</span><span class="sxs-lookup"><span data-stu-id="8cc9c-194">Large</span></span>
- <span data-ttu-id="8cc9c-195">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="8cc9c-195">ExtraLarge</span></span>
- <span data-ttu-id="8cc9c-196">A5</span><span class="sxs-lookup"><span data-stu-id="8cc9c-196">A5</span></span>
- <span data-ttu-id="8cc9c-197">A6</span><span class="sxs-lookup"><span data-stu-id="8cc9c-197">A6</span></span>
- <span data-ttu-id="8cc9c-198">A7</span><span class="sxs-lookup"><span data-stu-id="8cc9c-198">A7</span></span>
- <span data-ttu-id="8cc9c-199">A8</span><span class="sxs-lookup"><span data-stu-id="8cc9c-199">A8</span></span>
- <span data-ttu-id="8cc9c-200">A9</span><span class="sxs-lookup"><span data-stu-id="8cc9c-200">A9</span></span>
- <span data-ttu-id="8cc9c-201">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="8cc9c-201">Basic_A0</span></span>
- <span data-ttu-id="8cc9c-202">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="8cc9c-202">Basic_A1</span></span>
- <span data-ttu-id="8cc9c-203">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="8cc9c-203">Basic_A2</span></span>
- <span data-ttu-id="8cc9c-204">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="8cc9c-204">Basic_A3</span></span>
- <span data-ttu-id="8cc9c-205">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="8cc9c-205">Basic_A4</span></span>
- <span data-ttu-id="8cc9c-206">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="8cc9c-206">Standard_D1</span></span>
- <span data-ttu-id="8cc9c-207">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="8cc9c-207">Standard_D2</span></span>
- <span data-ttu-id="8cc9c-208">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="8cc9c-208">Standard_D3</span></span>
- <span data-ttu-id="8cc9c-209">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="8cc9c-209">Standard_D4</span></span>
- <span data-ttu-id="8cc9c-210">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="8cc9c-210">Standard_D11</span></span>
- <span data-ttu-id="8cc9c-211">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="8cc9c-211">Standard_D12</span></span>
- <span data-ttu-id="8cc9c-212">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="8cc9c-212">Standard_D13</span></span>
- <span data-ttu-id="8cc9c-213">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="8cc9c-213">Standard_D14</span></span>

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

### <span data-ttu-id="8cc9c-214">-Linux</span><span class="sxs-lookup"><span data-stu-id="8cc9c-214">-Linux</span></span>
<span data-ttu-id="8cc9c-215">Jelzi, hogy ez a parancsmag egy Linux-beli virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-215">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

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

### <span data-ttu-id="8cc9c-216">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="8cc9c-216">-LinuxUser</span></span>
<span data-ttu-id="8cc9c-217">Annak a linuxos rendszergazdai fióknak a felhasználónevét adja meg, amelyet a parancsmag a virtuális gépen hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-217">Specifies the user name of the Linux administrative account that this cmdlet creates on the virtual machine.</span></span>

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

### <span data-ttu-id="8cc9c-218">-Hely</span><span class="sxs-lookup"><span data-stu-id="8cc9c-218">-Location</span></span>
<span data-ttu-id="8cc9c-219">A virtuális gépet működtető Azure-adatközpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-219">Specifies the Azure datacenter that hosts the virtual machine.</span></span>
<span data-ttu-id="8cc9c-220">Ha ezt a paramétert adja meg, a parancsmag egy Azure-szolgáltatást hoz létre a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-220">If you specify this parameter, the cmdlet creates an Azure service in the specified location.</span></span>
<span data-ttu-id="8cc9c-221">Ezt a paramétert vagy a *AffinityGroup* paramétert csak akkor adja meg, ha a parancsmag Azure-szolgáltatást hoz létre a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-221">Specify this parameter or the *AffinityGroup* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="8cc9c-222">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="8cc9c-222">-MediaLocation</span></span>
<span data-ttu-id="8cc9c-223">Annak az Azure-tárterületnek a helye, ahol a parancsmag létrehozza a virtuális gépek lemezeit.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-223">Specifies the Azure Storage location where this cmdlet creates the virtual machines disks.</span></span>

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

### <span data-ttu-id="8cc9c-224">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8cc9c-224">-Name</span></span>
<span data-ttu-id="8cc9c-225">Annak a virtuális gépnek a nevét adja meg, amelyre a parancsmag létrehozta.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-225">Specifies the name of the virtual machine that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8cc9c-226">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="8cc9c-226">-NoExportPrivateKey</span></span>
<span data-ttu-id="8cc9c-227">Azt jelzi, hogy ez a konfiguráció nem tölti fel a titkos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-227">Indicates that this configuration does not upload the private key.</span></span>

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

### <span data-ttu-id="8cc9c-228">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cc9c-228">-NoWinRMEndpoint</span></span>
<span data-ttu-id="8cc9c-229">Azt jelzi, hogy ez a parancsmag nem hoz létre WinRM-végpontot a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-229">Indicates that this cmdlet does not add a WinRM endpoint for the virtual machine.</span></span>

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

### <span data-ttu-id="8cc9c-230">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="8cc9c-230">-Password</span></span>
<span data-ttu-id="8cc9c-231">A felügyeleti fiók jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-231">Specifies the password for the administrative account.</span></span>

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

### <span data-ttu-id="8cc9c-232">-Profil</span><span class="sxs-lookup"><span data-stu-id="8cc9c-232">-Profile</span></span>
<span data-ttu-id="8cc9c-233">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-233">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8cc9c-234">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-234">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8cc9c-235">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="8cc9c-235">-ReservedIPName</span></span>
<span data-ttu-id="8cc9c-236">A fenntartott IP-nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-236">Specifies the reserved IP name.</span></span>

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

### <span data-ttu-id="8cc9c-237">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="8cc9c-237">-ReverseDnsFqdn</span></span>
<span data-ttu-id="8cc9c-238">A DNS-névlekérdezéshez a teljesen minősített tartománynevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-238">Specifies the fully qualified domain name for reverse DNS look up.</span></span>

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

### <span data-ttu-id="8cc9c-239">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="8cc9c-239">-ServiceName</span></span>
<span data-ttu-id="8cc9c-240">Annak az új vagy meglévő Azure-szolgáltatásnak a nevét adja meg, amelyre a parancsmag hozzáadja az új virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-240">Specifies the name of a new or existing Azure service to which this cmdlet adds the new virtual machine.</span></span>

<span data-ttu-id="8cc9c-241">Ha új szolgáltatást ad meg, a parancsmagok létrehozzák.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-241">If you specify a new service, this cmdlets creates it.</span></span>
<span data-ttu-id="8cc9c-242">Új szolgáltatás létrehozásához meg kell adnia a *helyet* vagy a *AffinityGroup* paramétert.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-242">To create a new service, you must specify the *Location* or *AffinityGroup* parameter.</span></span>

<span data-ttu-id="8cc9c-243">Ha meglévő szolgáltatást ad meg, ne adjon meg *helyet* vagy *AffinityGroup*.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-243">If you specify an existing service, do not specify *Location* or *AffinityGroup*.</span></span>

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

### <span data-ttu-id="8cc9c-244">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="8cc9c-244">-SSHKeyPairs</span></span>
<span data-ttu-id="8cc9c-245">Az SSH-kulcsok párjait adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-245">Specifies SSH key pairs.</span></span>

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

### <span data-ttu-id="8cc9c-246">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="8cc9c-246">-SSHPublicKeys</span></span>
<span data-ttu-id="8cc9c-247">Az SSH-beli nyilvános kulcsokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-247">Specifies SSH public keys.</span></span>

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

### <span data-ttu-id="8cc9c-248">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="8cc9c-248">-SubnetNames</span></span>
<span data-ttu-id="8cc9c-249">A virtuális gép alhálózatának neveinek egy tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-249">Specifies an array of names of subnet for the virtual machine.</span></span>

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

### <span data-ttu-id="8cc9c-250">-VNetName</span><span class="sxs-lookup"><span data-stu-id="8cc9c-250">-VNetName</span></span>
<span data-ttu-id="8cc9c-251">A virtuális gép virtuális hálózatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-251">Specifies the name of a virtual network for the virtual machine.</span></span>

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

### <span data-ttu-id="8cc9c-252">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="8cc9c-252">-WaitForBoot</span></span>
<span data-ttu-id="8cc9c-253">Jelzi, hogy ez a parancsmag várja, hogy a virtuális gép elérje az állam ReadyRole.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-253">Indicates that this cmdlet waits for the virtual machine to reach the state ReadyRole.</span></span>
<span data-ttu-id="8cc9c-254">Ha a virtuális gép eléri az alábbi állapotok egyikét, a parancsmag nem működik: FailedStartingVM, ProvisioningFailed vagy ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-254">If the virtual machine reaches one of the following states, the cmdlet fails: FailedStartingVM, ProvisioningFailed, or ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="8cc9c-255">-Windows</span><span class="sxs-lookup"><span data-stu-id="8cc9c-255">-Windows</span></span>
<span data-ttu-id="8cc9c-256">Jelzi, hogy ez a parancsmag létrehoz egy Windows Virtual Machine-t.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-256">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="8cc9c-257">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc9c-257">-WinRMCertificate</span></span>
<span data-ttu-id="8cc9c-258">Azt a tanúsítványt adja meg, amelyet a parancsmag a WinRM-végpontokhoz társít.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-258">Specifies a certificate that this cmdlet associates to a WinRM endpoint.</span></span>

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

### <span data-ttu-id="8cc9c-259">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="8cc9c-259">-X509Certificates</span></span>
<span data-ttu-id="8cc9c-260">A hosztolt szolgáltatásba telepített X509-tanúsítványok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-260">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

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

### <span data-ttu-id="8cc9c-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc9c-261">CommonParameters</span></span>
<span data-ttu-id="8cc9c-262">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8cc9c-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc9c-263">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cc9c-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc9c-264">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cc9c-264">INPUTS</span></span>

## <span data-ttu-id="8cc9c-265">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cc9c-265">OUTPUTS</span></span>

## <span data-ttu-id="8cc9c-266">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8cc9c-266">NOTES</span></span>

## <span data-ttu-id="8cc9c-267">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cc9c-267">RELATED LINKS</span></span>

[<span data-ttu-id="8cc9c-268">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="8cc9c-268">Get-AzureLocation</span></span>](./Get-AzureLocation.md)

[<span data-ttu-id="8cc9c-269">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="8cc9c-269">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="8cc9c-270">Új – AzureDns</span><span class="sxs-lookup"><span data-stu-id="8cc9c-270">New-AzureDns</span></span>](./New-AzureDns.md)



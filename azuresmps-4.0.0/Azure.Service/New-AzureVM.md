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
# <span data-ttu-id="d7f5e-101">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d7f5e-101">New-AzureVM</span></span>

## <span data-ttu-id="d7f5e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f5e-103">Azure virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-103">Creates an Azure virtual machine.</span></span>

## <span data-ttu-id="d7f5e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7f5e-104">SYNTAX</span></span>

### <span data-ttu-id="d7f5e-105">ExistingService (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7f5e-105">ExistingService (Default)</span></span>
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d7f5e-106">CreateService</span><span class="sxs-lookup"><span data-stu-id="d7f5e-106">CreateService</span></span>
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d7f5e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7f5e-107">DESCRIPTION</span></span>
<span data-ttu-id="d7f5e-108">A **New-AzureVM** parancsmag új virtuális gépet ad egy meglévő Azure-szolgáltatáshoz, vagy virtuális gépet és szolgáltatást hoz létre a jelenlegi előfizetésben, ha a *helyet* vagy a *AffinityGroup* adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-108">The **New-AzureVM** cmdlet adds a new virtual machine to an existing Azure service, or creates a virtual machine and service in the current subscription if either the *Location* or *AffinityGroup* is specified.</span></span>

## <span data-ttu-id="d7f5e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d7f5e-109">EXAMPLES</span></span>

### <span data-ttu-id="d7f5e-110">Példa 1: virtuális gép létrehozása Windows-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="d7f5e-110">Example 1: Create a virtual machine for a Windows configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

<span data-ttu-id="d7f5e-111">Ez a parancs létrehoz egy kiépítési konfigurációt a Windows operációs rendszer virtuálisgép-konfigurációja alapján, és egy virtuális gépet hoz létre a megadott affinitási csoportban.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-111">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="d7f5e-112">2. példa: virtuális gép létrehozása Linux-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="d7f5e-112">Example 2: Create a virtual machine for a Linux configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

<span data-ttu-id="d7f5e-113">Ez a parancs létrehoz egy kiépítési konfigurációt a Linux virtuális gép konfigurációja alapján, és egy virtuális gépet hoz létre a megadott affinitási csoportban.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-113">This command creates a provisioning configuration based on a virtual machine configuration for Linux, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="d7f5e-114">3. példa: virtuális gép létrehozása és adatlemez hozzáadása</span><span class="sxs-lookup"><span data-stu-id="d7f5e-114">Example 3: Create a virtual machine and add a data disk</span></span>
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

<span data-ttu-id="d7f5e-115">Az első két parancs a **Get-AzureVMImage** parancsmag használatával érheti el a képeket, és az $Image változóban tárolja az egyiket.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-115">The first two commands get available images by using the **Get-AzureVMImage** cmdlet, and stores one of them in the $Image variable.</span></span>

<span data-ttu-id="d7f5e-116">Ez a parancs létrehoz egy kiépítési konfigurációt a Windows operációs rendszer virtuálisgép-konfigurációja alapján, és egy virtuális gépet hoz létre Azure-adatlemezzel.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-116">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with an Azure data disk.</span></span>

### <span data-ttu-id="d7f5e-117">Példa 4: fenntartott IP-címmel rendelkező virtuális gép létrehozása</span><span class="sxs-lookup"><span data-stu-id="d7f5e-117">Example 4: Create a virtual machine with a reserved IP address</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

<span data-ttu-id="d7f5e-118">Ez a parancs létrehoz egy kiépítési konfigurációt a Windows operációs rendszer virtuálisgép-konfigurációja alapján, és egy fenntartott IP-címet használó virtuális gépet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-118">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with a reserved IP address.</span></span>

## <span data-ttu-id="d7f5e-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7f5e-119">PARAMETERS</span></span>

### <span data-ttu-id="d7f5e-120">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="d7f5e-120">-AffinityGroup</span></span>
<span data-ttu-id="d7f5e-121">Annak az Azure affinitásnak a csoportját adja meg, amelyben a Felhőbeli szolgáltatás található.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-121">Specifies the Azure affinity group in which the cloud service resides.</span></span>
<span data-ttu-id="d7f5e-122">Ehhez a paraméterhez csak akkor van szükség, ha a parancsmag felhőalapú szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-122">This parameter is required only when this cmdlet creates a cloud service.</span></span>

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

### <span data-ttu-id="d7f5e-123">-DeploymentLabel</span><span class="sxs-lookup"><span data-stu-id="d7f5e-123">-DeploymentLabel</span></span>
<span data-ttu-id="d7f5e-124">A központi telepítő címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-124">Specifies a label for the deployment.</span></span>

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

### <span data-ttu-id="d7f5e-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d7f5e-125">-DeploymentName</span></span>
<span data-ttu-id="d7f5e-126">A telepítő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-126">Specifies a deployment name.</span></span>
<span data-ttu-id="d7f5e-127">Ha nem adja meg, akkor ez a parancsmag a szolgáltatás nevét használja a központi telepítő nevében.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-127">If not specified, this cmdlet uses the service name as the deployment name.</span></span>

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

### <span data-ttu-id="d7f5e-128">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="d7f5e-128">-DnsSettings</span></span>
<span data-ttu-id="d7f5e-129">Megadja azt a DNS-kiszolgáló objektumot, amely meghatározza az új központi telepítő DNS-beállításait.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-129">Specifies a DNS Server object that defines the DNS settings for the new deployment.</span></span>

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

### <span data-ttu-id="d7f5e-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d7f5e-130">-InformationAction</span></span>
<span data-ttu-id="d7f5e-131">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d7f5e-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d7f5e-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d7f5e-133">Folytassa</span><span class="sxs-lookup"><span data-stu-id="d7f5e-133">Continue</span></span>
- <span data-ttu-id="d7f5e-134">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="d7f5e-134">Ignore</span></span>
- <span data-ttu-id="d7f5e-135">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="d7f5e-135">Inquire</span></span>
- <span data-ttu-id="d7f5e-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d7f5e-136">SilentlyContinue</span></span>
- <span data-ttu-id="d7f5e-137">állj</span><span class="sxs-lookup"><span data-stu-id="d7f5e-137">Stop</span></span>
- <span data-ttu-id="d7f5e-138">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="d7f5e-138">Suspend</span></span>

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

### <span data-ttu-id="d7f5e-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d7f5e-139">-InformationVariable</span></span>
<span data-ttu-id="d7f5e-140">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d7f5e-141">-InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="d7f5e-141">-InternalLoadBalancerConfig</span></span>
<span data-ttu-id="d7f5e-142">Belső terheléselosztót ad meg.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-142">Specifies an internal load balancer.</span></span>
<span data-ttu-id="d7f5e-143">Ezt a paramétert a program nem használja.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-143">This parameter is not used.</span></span>

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

### <span data-ttu-id="d7f5e-144">-Hely</span><span class="sxs-lookup"><span data-stu-id="d7f5e-144">-Location</span></span>
<span data-ttu-id="d7f5e-145">Az új szolgáltatást működtető helyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-145">Specifies the location that hosts the new service.</span></span>
<span data-ttu-id="d7f5e-146">Ha már létezik a szolgáltatás, ne adja meg ezt a paramétert.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-146">If the service already exists, do not specify this parameter.</span></span>

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

### <span data-ttu-id="d7f5e-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="d7f5e-147">-Profile</span></span>
<span data-ttu-id="d7f5e-148">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d7f5e-149">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d7f5e-150">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="d7f5e-150">-ReservedIPName</span></span>
<span data-ttu-id="d7f5e-151">A foglalt IP-cím nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-151">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="d7f5e-152">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="d7f5e-152">-ReverseDnsFqdn</span></span>
<span data-ttu-id="d7f5e-153">A DNS-név teljesen minősített tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-153">Specifies the fully-qualified domain name for reverse DNS.</span></span>

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

### <span data-ttu-id="d7f5e-154">-ServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d7f5e-154">-ServiceDescription</span></span>
<span data-ttu-id="d7f5e-155">Az új szolgáltatás leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-155">Specifies a description for the new service.</span></span>

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

### <span data-ttu-id="d7f5e-156">-ServiceLabel</span><span class="sxs-lookup"><span data-stu-id="d7f5e-156">-ServiceLabel</span></span>
<span data-ttu-id="d7f5e-157">Az új szolgáltatás feliratát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-157">Specifies a label for the new service.</span></span>

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

### <span data-ttu-id="d7f5e-158">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="d7f5e-158">-ServiceName</span></span>
<span data-ttu-id="d7f5e-159">Az új vagy meglévő szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-159">Specifies the new or existing service name.</span></span>

<span data-ttu-id="d7f5e-160">Ha a szolgáltatás nem létezik, akkor ez a parancsmag hozza létre Önnek a megfelelőt.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-160">If the service does not exist, this cmdlet creates it for you.</span></span>
<span data-ttu-id="d7f5e-161">A *hely* vagy a *AffinityGroup* paraméterrel megadhatja, hogy hová hozza létre a szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-161">Use the *Location* or *AffinityGroup* parameter to specify where to create the service.</span></span>

<span data-ttu-id="d7f5e-162">Ha a szolgáltatás létezik, a *hely* -vagy *AffinityGroup* paraméter nem szükséges.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-162">If the service exists, the *Location* or *AffinityGroup* parameter is not needed.</span></span>

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

### <span data-ttu-id="d7f5e-163">-VMs</span><span class="sxs-lookup"><span data-stu-id="d7f5e-163">-VMs</span></span>
<span data-ttu-id="d7f5e-164">A létrehozandó virtuális számítógép-objektumok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-164">Specifies a list of virtual machine objects to create.</span></span>

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

### <span data-ttu-id="d7f5e-165">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d7f5e-165">-VNetName</span></span>
<span data-ttu-id="d7f5e-166">Annak a virtuális hálózatnak a nevét adja meg, ahol ez a parancsmag telepíti a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-166">Specifies the virtual network name where this cmdlet deploys the virtual machine.</span></span>

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

### <span data-ttu-id="d7f5e-167">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="d7f5e-167">-WaitForBoot</span></span>
<span data-ttu-id="d7f5e-168">Itt adhatja meg, hogy ez a parancsmag várja a virtuális gépet a **ReadyRole** állapot eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-168">Specifies that this cmdlet waits for the virtual machine to reach the **ReadyRole** state.</span></span>
<span data-ttu-id="d7f5e-169">Ez a parancsmag nem hajtható végre, ha a virtuális gép az alábbi állapotok egyikére esik a várakozás közben: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="d7f5e-169">This cmdlet fails if the virtual machine falls in one of the following states while waiting: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="d7f5e-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f5e-170">CommonParameters</span></span>
<span data-ttu-id="d7f5e-171">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7f5e-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f5e-172">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7f5e-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f5e-173">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7f5e-173">INPUTS</span></span>

## <span data-ttu-id="d7f5e-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7f5e-174">OUTPUTS</span></span>

## <span data-ttu-id="d7f5e-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7f5e-175">NOTES</span></span>

## <span data-ttu-id="d7f5e-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7f5e-176">RELATED LINKS</span></span>

[<span data-ttu-id="d7f5e-177">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="d7f5e-177">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="d7f5e-178">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="d7f5e-178">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="d7f5e-179">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="d7f5e-179">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="d7f5e-180">Új – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="d7f5e-180">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)



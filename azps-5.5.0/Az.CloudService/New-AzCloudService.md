---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/new-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudService.md
ms.openlocfilehash: 24e90ebae59c9d9a4449c57270b7ca69f9b05b88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166667"
---
# <span data-ttu-id="03bdd-101">New-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="03bdd-101">New-AzCloudService</span></span>

## <span data-ttu-id="03bdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="03bdd-103">Felhőszolgáltatás létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="03bdd-103">Create or update a cloud service.</span></span>
<span data-ttu-id="03bdd-104">Felhívjuk a figyelmét arra, hogy egyes tulajdonságokat csak a felhőbeli szolgáltatások létrehozásakor lehet beállítani.</span><span class="sxs-lookup"><span data-stu-id="03bdd-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="03bdd-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03bdd-105">SYNTAX</span></span>

```
New-AzCloudService -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Configuration <String>] [-ConfigurationUrl <String>] [-ExtensionProfile <ICloudServiceExtensionProfile>]
 [-NetworkProfile <ICloudServiceNetworkProfile>] [-OSProfile <ICloudServiceOSProfile>] [-PackageUrl <String>]
 [-RoleProfile <ICloudServiceRoleProfile>] [-StartCloudService] [-Tag <Hashtable>]
 [-UpgradeMode <CloudServiceUpgradeMode>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="03bdd-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03bdd-106">DESCRIPTION</span></span>
<span data-ttu-id="03bdd-107">Felhőszolgáltatás létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="03bdd-107">Create or update a cloud service.</span></span>
<span data-ttu-id="03bdd-108">Felhívjuk a figyelmét arra, hogy egyes tulajdonságokat csak a felhőbeli szolgáltatások létrehozásakor lehet beállítani.</span><span class="sxs-lookup"><span data-stu-id="03bdd-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="03bdd-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03bdd-109">EXAMPLES</span></span>

### <span data-ttu-id="03bdd-110">1. példa: Új felhőszolgáltatás létrehozása egyetlen szerepkörben</span><span class="sxs-lookup"><span data-stu-id="03bdd-110">Example 1: Create new cloud service with single role</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile
```

<span data-ttu-id="03bdd-111">Parancskészlet felett létrehoz egy felhőszolgáltatást egyetlen szerepkörben</span><span class="sxs-lookup"><span data-stu-id="03bdd-111">Above set of commands creates a cloud service with single role</span></span>

### <span data-ttu-id="03bdd-112">2. példa: Új felhőszolgáltatás létrehozása egyetlen szerepkörű és RDP-kiterjesztéssel</span><span class="sxs-lookup"><span data-stu-id="03bdd-112">Example 2: Create new cloud service with single role and RDP extension</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosoOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
PS C:\> $extensionProfile = @{extension = @($extension)}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile
```

<span data-ttu-id="03bdd-113">A parancskészlet fölött egy felhőszolgáltatást hoz létre egyetlen szerepkörű és RDP-kiterjesztéssel</span><span class="sxs-lookup"><span data-stu-id="03bdd-113">Above set of commands creates a cloud service with single role and RDP extension</span></span>

### <span data-ttu-id="03bdd-114">3. példa: Új felhőszolgáltatás létrehozása egyetlen szerepkört és tanúsítványt a kulcstárolóból</span><span class="sxs-lookup"><span data-stu-id="03bdd-114">Example 3: Create new cloud service with single role and certificate from key vault</span></span>
```powershell
# Create role profile object
PS C:\> $role = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role)}

# Create OS profile object
$keyVault = Get-AzKeyVault -ResourceGroupName ContosOrg -VaultName ContosKeyVault
$certificate=Get-AzKeyVaultCertificate -VaultName ContosKeyVault -Name ContosCert
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
$osProfile = @{secret = @($secretGroup)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -OSProfile $osProfile
```

<span data-ttu-id="03bdd-115">A parancskészlet fölött egy felhőszolgáltatást hoz létre egyetlen szerepkörű és a kulcstárolóból származó tanúsítvánnyal.</span><span class="sxs-lookup"><span data-stu-id="03bdd-115">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

### <span data-ttu-id="03bdd-116">4. példa: Új felhőszolgáltatás létrehozása több szerepkört és bővítményt</span><span class="sxs-lookup"><span data-stu-id="03bdd-116">Example 4: Create new cloud service with multiple roles and extensions</span></span>
```powershell
# Create role profile object
PS C:\> $role1 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoFrontend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $role2 = New-AzCloudServiceCloudServiceRoleProfilePropertiesObject -Name 'ContosoBackend' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
PS C:\> $roleProfile = @{role = @($role1, $role2)}

# Create network profile object
PS C:\> $publicIp = Get-AzPublicIpAddress -ResourceGroupName ContosOrg -Name ContosIp
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
PS C:\> $networkProfile = @{loadBalancerConfiguration = $loadBalancerConfig}

# Create RDP extension object
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'

# Create Geneva extension object
PS C:\> $genevaExtension = New-AzCloudServiceExtensionObject -Name GenevaExtension -Publisher Microsoft.Azure.Geneva -Type GenevaMonitoringPaaS -TypeHandlerVersion "2.14.0.2"
PS C:\> $extensionProfile = @{extension = @($rdpExtension, $genevaExtension)}

# Add tags
$tag=@{"Owner" = "Contoso"}

# Read Configuration File
$cscfgFile = "<Path to cscfg configuration file>"
$cscfgContent = Get-Content $cscfgFile | Out-String

# Create cloud service
$cloudService = New-AzCloudService                                              `
                  -Name ContosoCS                                               `
                  -ResourceGroupName ContosOrg                                  `
                  -Location EastUS                                              `
                  -PackageUrl "https://xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"    `
                  -Configuration $cscfgContent                                  `
                  -UpgradeMode 'Auto'                                           `
                  -RoleProfile $roleProfile                                     `
                  -NetworkProfile $networkProfile                               `
                  -ExtensionProfile $extensionProfile                           `
                  -Tag $tag
```

<span data-ttu-id="03bdd-117">A parancskészlet fölött egy felhőszolgáltatást hoz létre egyetlen szerepkörű és a kulcstárolóból származó tanúsítvánnyal.</span><span class="sxs-lookup"><span data-stu-id="03bdd-117">Above set of commands creates a cloud service with single role and certificate from key vault.</span></span>

## <span data-ttu-id="03bdd-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03bdd-118">PARAMETERS</span></span>

### <span data-ttu-id="03bdd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03bdd-119">-AsJob</span></span>
<span data-ttu-id="03bdd-120">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="03bdd-120">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-121">- Konfiguráció</span><span class="sxs-lookup"><span data-stu-id="03bdd-121">-Configuration</span></span>
<span data-ttu-id="03bdd-122">A felhőszolgáltatás XML-szolgáltatáskonfigurációját (.cscfg) adja meg.</span><span class="sxs-lookup"><span data-stu-id="03bdd-122">Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-123">-ConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="03bdd-123">-ConfigurationUrl</span></span>
<span data-ttu-id="03bdd-124">Egy URL-címet ad meg, amely a blobszolgáltatás szolgáltatáskonfigurációjának helyére hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="03bdd-124">Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span>
<span data-ttu-id="03bdd-125">A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet SAS-URI. Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="03bdd-125">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bdd-126">-DefaultProfile</span></span>
<span data-ttu-id="03bdd-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03bdd-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-128">-ExtensionProfile</span><span class="sxs-lookup"><span data-stu-id="03bdd-128">-ExtensionProfile</span></span>
<span data-ttu-id="03bdd-129">A felhőbeli szolgáltatásbővítmény-profilt ismerteti.</span><span class="sxs-lookup"><span data-stu-id="03bdd-129">Describes a cloud service extension profile.</span></span>
<span data-ttu-id="03bdd-130">Ennek létrehozásáról az EXTENSIONPROFILE tulajdonságokat és egy kivonattáblát a NOTES (JEGYZETEK) című szakaszban láthat.</span><span class="sxs-lookup"><span data-stu-id="03bdd-130">To construct, see NOTES section for EXTENSIONPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceExtensionProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-131">-Location</span><span class="sxs-lookup"><span data-stu-id="03bdd-131">-Location</span></span>
<span data-ttu-id="03bdd-132">Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="03bdd-132">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-133">-Name</span><span class="sxs-lookup"><span data-stu-id="03bdd-133">-Name</span></span>
<span data-ttu-id="03bdd-134">A felhőszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="03bdd-134">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-135">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="03bdd-135">-NetworkProfile</span></span>
<span data-ttu-id="03bdd-136">A felhőszolgáltatás hálózati profilja.</span><span class="sxs-lookup"><span data-stu-id="03bdd-136">Network Profile for the cloud service.</span></span>
<span data-ttu-id="03bdd-137">Ennek létrehozásáról az NETWORKPROFILE tulajdonságokat és egy kivonattáblát a NOTES (JEGYZETEK) című szakaszban láthat.</span><span class="sxs-lookup"><span data-stu-id="03bdd-137">To construct, see NOTES section for NETWORKPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceNetworkProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="03bdd-138">-NoWait</span></span>
<span data-ttu-id="03bdd-139">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="03bdd-139">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-140">-OSProfile</span><span class="sxs-lookup"><span data-stu-id="03bdd-140">-OSProfile</span></span>
<span data-ttu-id="03bdd-141">A felhőszolgáltatás operációs rendszerprofilját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="03bdd-141">Describes the OS profile for the cloud service.</span></span>
<span data-ttu-id="03bdd-142">Ennek létrehozásáról az OSPROFILE tulajdonságairól és egy kivonattábláról a NOTES (JEGYZETEK) című szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="03bdd-142">To construct, see NOTES section for OSPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-143">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="03bdd-143">-PackageUrl</span></span>
<span data-ttu-id="03bdd-144">Egy URL-címet ad meg, amely a szolgáltatáscsomag blobszolgáltatásban való helyére hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="03bdd-144">Specifies a URL that refers to the location of the service package in the Blob service.</span></span>
<span data-ttu-id="03bdd-145">A szolgáltatáscsomag URL-címe bármilyen tárfiókból lehet SAS-URI. Ez egy írási tulajdonság, és a GET-hívásokban nem ad vissza.</span><span class="sxs-lookup"><span data-stu-id="03bdd-145">The service package URL can be Shared Access Signature (SAS) URI from any storage account.This is a write-only property and is not returned in GET calls.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03bdd-146">-ResourceGroupName</span></span>
<span data-ttu-id="03bdd-147">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="03bdd-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-148">-RoleProfile</span><span class="sxs-lookup"><span data-stu-id="03bdd-148">-RoleProfile</span></span>
<span data-ttu-id="03bdd-149">A felhőszolgáltatás szerepkörprofilját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="03bdd-149">Describes the role profile for the cloud service.</span></span>
<span data-ttu-id="03bdd-150">A FELépítésről a NOTES (JEGYZETEK) szakaszban található a ROLEPROFILE tulajdonságok és a hash tábla létrehozása.</span><span class="sxs-lookup"><span data-stu-id="03bdd-150">To construct, see NOTES section for ROLEPROFILE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceRoleProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-151">-StartCloudService</span><span class="sxs-lookup"><span data-stu-id="03bdd-151">-StartCloudService</span></span>
<span data-ttu-id="03bdd-152">(Nem kötelező) Azt jelzi, hogy a felhőszolgáltatást a létrehozása után azonnal el kell-e indítanunk.</span><span class="sxs-lookup"><span data-stu-id="03bdd-152">(Optional) Indicates whether to start the cloud service immediately after it is created.</span></span>
<span data-ttu-id="03bdd-153">Az alapértelmezett érték `true` a . Ha hamis, a szolgáltatásmodell továbbra is telepítve van, de a kód nem fut azonnal.</span><span class="sxs-lookup"><span data-stu-id="03bdd-153">The default value is `true`.If false, the service model is still deployed, but the code is not run immediately.</span></span>
<span data-ttu-id="03bdd-154">Ehelyett a szolgáltatás PoweredOff lesz, amíg fel nem hívja a Start menüt, és a szolgáltatás elindul.</span><span class="sxs-lookup"><span data-stu-id="03bdd-154">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span>
<span data-ttu-id="03bdd-155">A telepített szolgáltatások még akkor is költségeket is fizetninek, ha a szolgáltatás nem működik.</span><span class="sxs-lookup"><span data-stu-id="03bdd-155">A deployed service still incurs charges, even if it is poweredoff.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03bdd-156">-SubscriptionId</span></span>
<span data-ttu-id="03bdd-157">Az előfizetés hitelesítő adatai, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="03bdd-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="03bdd-158">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="03bdd-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="03bdd-159">-Tag</span></span>
<span data-ttu-id="03bdd-160">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="03bdd-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-161">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="03bdd-161">-UpgradeMode</span></span>
<span data-ttu-id="03bdd-162">A felhőszolgáltatás frissítési módja.</span><span class="sxs-lookup"><span data-stu-id="03bdd-162">Update mode for the cloud service.</span></span>
<span data-ttu-id="03bdd-163">A szerepkörpéldányok ki vannak osztva a tartományok frissítéséhez a szolgáltatás telepítésekor.</span><span class="sxs-lookup"><span data-stu-id="03bdd-163">Role instances are allocated to update domains when the service is deployed.</span></span>
<span data-ttu-id="03bdd-164">A frissítéseket manuálisan kezdeményezheti az egyes frissítési tartományokban, illetve automatikusan az összes frissítési tartományban. Lehetséges értékek: \<br /\> \<br /\> **Automatikus** \<br /\> \<br /\> **manuális** \<br /\> \<br /\> **egyidejűség,** ha \<br /\> \<br /\> nincs megadva, az alapértelmezett érték az Automatikus. Ha a Kézi beállítás van beállítva, akkor a PUT UpdateDomain tartományt meg kell hívva alkalmazni a frissítést.</span><span class="sxs-lookup"><span data-stu-id="03bdd-164">Updates can be initiated manually in each update domain or initiated automatically in all update domains.Possible Values are \<br /\>\<br /\>**Auto**\<br /\>\<br /\>**Manual** \<br /\>\<br /\>**Simultaneous**\<br /\>\<br /\>If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span>
<span data-ttu-id="03bdd-165">Ha az Automatikus beállítás van beállítva, a rendszer automatikusan alkalmazza a frissítést az egyes frissítési tartományokra.</span><span class="sxs-lookup"><span data-stu-id="03bdd-165">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.CloudServiceUpgradeMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03bdd-166">-Confirm</span></span>
<span data-ttu-id="03bdd-167">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="03bdd-167">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03bdd-168">-WhatIf</span></span>
<span data-ttu-id="03bdd-169">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="03bdd-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03bdd-170">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03bdd-170">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bdd-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bdd-171">CommonParameters</span></span>
<span data-ttu-id="03bdd-172">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03bdd-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bdd-173">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03bdd-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bdd-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03bdd-174">INPUTS</span></span>

## <span data-ttu-id="03bdd-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03bdd-175">OUTPUTS</span></span>

### <span data-ttu-id="03bdd-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="03bdd-176">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="03bdd-177">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03bdd-177">NOTES</span></span>

<span data-ttu-id="03bdd-178">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="03bdd-178">ALIASES</span></span>

<span data-ttu-id="03bdd-179">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="03bdd-179">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="03bdd-180">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="03bdd-180">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="03bdd-181">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="03bdd-181">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="03bdd-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile> : Egy felhőbeli szolgáltatásbővítmény-profilt ismertet.</span><span class="sxs-lookup"><span data-stu-id="03bdd-182">EXTENSIONPROFILE <ICloudServiceExtensionProfile>: Describes a cloud service extension profile.</span></span>
  - <span data-ttu-id="03bdd-183">`[Extension <IExtension[]>]`: A felhőszolgáltatás bővítményei.</span><span class="sxs-lookup"><span data-stu-id="03bdd-183">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
    - <span data-ttu-id="03bdd-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicit módon megadhatja, hogy a platform képes-e automatikusan frissíteni a TypeHandlerVersiont a nagyobb alverziókra, amikor elérhetővé válnak.</span><span class="sxs-lookup"><span data-stu-id="03bdd-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
    - <span data-ttu-id="03bdd-185">`[ForceUpdateTag <String>]`: Címkével kényszerítheti a megadott nyilvános és védett beállítások alkalmazását.</span><span class="sxs-lookup"><span data-stu-id="03bdd-185">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="03bdd-186">A címkeérték módosítása lehetővé teszi a bővítmény újrafuttatését a nyilvános vagy védett beállítások módosítása nélkül.</span><span class="sxs-lookup"><span data-stu-id="03bdd-186">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="03bdd-187">Ha a forceUpdateTag nem változik, a nyilvános vagy védett beállítások frissítéseit a kezelő továbbra is alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="03bdd-187">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="03bdd-188">Ha sem a forceUpdateTag, sem a nyilvános vagy védett beállítások egyike sem változik, a bővítmény a szerepkörpéldányba áramolna ugyanazokkal a sorszámmal, és a kezelő implementációja függ attól, hogy újra futtatja-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="03bdd-188">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
    - <span data-ttu-id="03bdd-189">`[Name <String>]`: A bővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="03bdd-189">`[Name <String>]`: The name of the extension.</span></span>
    - <span data-ttu-id="03bdd-190">`[ProtectedSetting <String>]`: A bővítmény védett beállításai, amelyek titkosítottak, mielőtt elkülde volna a szerepkörpéldánynak.</span><span class="sxs-lookup"><span data-stu-id="03bdd-190">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
    - <span data-ttu-id="03bdd-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="03bdd-191">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
    - <span data-ttu-id="03bdd-192">`[Publisher <String>]`: A bővítménykezelő közzétevője neve.</span><span class="sxs-lookup"><span data-stu-id="03bdd-192">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
    - <span data-ttu-id="03bdd-193">`[RolesAppliedTo <String[]>]`: A bővítmény alkalmazásához választható szerepkörök listája.</span><span class="sxs-lookup"><span data-stu-id="03bdd-193">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="03bdd-194">Ha a tulajdonság nincs megadva, vagy a "\*" érték meg van adva, a bővítmény a felhőszolgáltatás összes szerepkörében érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="03bdd-194">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
    - <span data-ttu-id="03bdd-195">`[Setting <String>]`: A bővítmény nyilvános beállításai.</span><span class="sxs-lookup"><span data-stu-id="03bdd-195">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="03bdd-196">JSON-bővítményekben ez a bővítmény JSON-beállításai.</span><span class="sxs-lookup"><span data-stu-id="03bdd-196">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="03bdd-197">XML-bővítmény (például RDP) esetén ez a bővítmény XML-beállítása.</span><span class="sxs-lookup"><span data-stu-id="03bdd-197">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
    - <span data-ttu-id="03bdd-198">`[SourceVaultId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="03bdd-198">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="03bdd-199">`[Type <String>]`: A bővítmény típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="03bdd-199">`[Type <String>]`: Specifies the type of the extension.</span></span>
    - <span data-ttu-id="03bdd-200">`[TypeHandlerVersion <String>]`: A bővítmény verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="03bdd-200">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="03bdd-201">A bővítmény verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="03bdd-201">Specifies the version of the extension.</span></span> <span data-ttu-id="03bdd-202">Ha ez az elem nincs megadva, vagy csillag (\*) használja értékként, akkor a bővítmény legújabb verzióját használja a program.</span><span class="sxs-lookup"><span data-stu-id="03bdd-202">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="03bdd-203">Ha az értéket egy főverzió számával, a csillagot pedig alverziószámmal (X.) adja meg, akkor a megadott főverzió legújabb alverziója van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="03bdd-203">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="03bdd-204">Ha a főverzió és az alverzió száma meg van adva (X.Y), akkor az adott bővítményverzió van kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="03bdd-204">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="03bdd-205">Ha egy verzió meg van adva, a szerepkörpéldányon automatikus frissítés történik.</span><span class="sxs-lookup"><span data-stu-id="03bdd-205">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>

<span data-ttu-id="03bdd-206">NETWORKPROFILE: <ICloudServiceNetworkProfile> A felhőszolgáltatás hálózati profilja.</span><span class="sxs-lookup"><span data-stu-id="03bdd-206">NETWORKPROFILE <ICloudServiceNetworkProfile>: Network Profile for the cloud service.</span></span>
  - <span data-ttu-id="03bdd-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: A felhőszolgáltatás terheléselosztási konfigurációjának listája.</span><span class="sxs-lookup"><span data-stu-id="03bdd-207">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
    - <span data-ttu-id="03bdd-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: AZ IP-címek listája</span><span class="sxs-lookup"><span data-stu-id="03bdd-208">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
      - <span data-ttu-id="03bdd-209">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="03bdd-209">`[Name <String>]`:</span></span> 
      - <span data-ttu-id="03bdd-210">`[PrivateIPAddress <String>]`: A felhőszolgáltatás által hivatkozott privát IP-cím.</span><span class="sxs-lookup"><span data-stu-id="03bdd-210">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
      - <span data-ttu-id="03bdd-211">`[PublicIPAddressId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="03bdd-211">`[PublicIPAddressId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="03bdd-212">`[SubnetId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="03bdd-212">`[SubnetId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="03bdd-213">`[Name <String>]`: Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="03bdd-213">`[Name <String>]`: Resource Name</span></span>
  - <span data-ttu-id="03bdd-214">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="03bdd-214">`[SwappableCloudService <ISubResource>]`:</span></span> 
    - <span data-ttu-id="03bdd-215">`[Id <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="03bdd-215">`[Id <String>]`: Resource Id</span></span>

<span data-ttu-id="03bdd-216">OSPROFILE: <ICloudServiceOSProfile> A felhőszolgáltatás operációs rendszerprofilját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="03bdd-216">OSPROFILE <ICloudServiceOSProfile>: Describes the OS profile for the cloud service.</span></span>
  - <span data-ttu-id="03bdd-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Megadja a szerepkörpéldányokra telepíthető tanúsítványok készletét.</span><span class="sxs-lookup"><span data-stu-id="03bdd-217">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
    - <span data-ttu-id="03bdd-218">`[SourceVaultId <String>]`: Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="03bdd-218">`[SourceVaultId <String>]`: Resource Id</span></span>
    - <span data-ttu-id="03bdd-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: A SourceVault kulcstár-hivatkozásai, amelyek tanúsítványokat tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="03bdd-219">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
      - <span data-ttu-id="03bdd-220">`[CertificateUrl <String>]`: Ez annak a tanúsítványnak az URL-címe, amely titkosként lett feltöltve a kulcstárolóba.</span><span class="sxs-lookup"><span data-stu-id="03bdd-220">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

<span data-ttu-id="03bdd-221">ROLEPROFILE <ICloudServiceRoleProfile> : A felhőszolgáltatás szerepkörprofilját ismerteti.</span><span class="sxs-lookup"><span data-stu-id="03bdd-221">ROLEPROFILE <ICloudServiceRoleProfile>: Describes the role profile for the cloud service.</span></span>
  - <span data-ttu-id="03bdd-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: A felhőszolgáltatás szerepkörei.</span><span class="sxs-lookup"><span data-stu-id="03bdd-222">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
    - <span data-ttu-id="03bdd-223">`[Name <String>]`: Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="03bdd-223">`[Name <String>]`: Resource name.</span></span>
    - <span data-ttu-id="03bdd-224">`[SkuCapacity <Int64?>]`: A felhőszolgáltatás szerepkör-példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="03bdd-224">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
    - <span data-ttu-id="03bdd-225">`[SkuName <String>]`: A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="03bdd-225">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="03bdd-226">MEGJEGYZÉS: Ha az új termékváltozat nem támogatott a felhőszolgáltatás által jelenleg használt hardveren, törölnie és újra létre kell hoznia a felhőszolgáltatást, vagy vissza kell lépnie a régi termékváltozatra.</span><span class="sxs-lookup"><span data-stu-id="03bdd-226">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
    - <span data-ttu-id="03bdd-227">`[SkuTier <String>]`: A felhőszolgáltatás rétegét adja meg.</span><span class="sxs-lookup"><span data-stu-id="03bdd-227">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="03bdd-228">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="03bdd-228">Possible Values are</span></span> <br /><br /> <span data-ttu-id="03bdd-229">**Normál**</span><span class="sxs-lookup"><span data-stu-id="03bdd-229">**Standard**</span></span> <br /><br /> <span data-ttu-id="03bdd-230">**Alapszintű**</span><span class="sxs-lookup"><span data-stu-id="03bdd-230">**Basic**</span></span>

## <span data-ttu-id="03bdd-231">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03bdd-231">RELATED LINKS</span></span>


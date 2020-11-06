---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: ee18925960b7f2afd9e35250a3cc33a5bd16e073
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494122"
---
# <span data-ttu-id="f418b-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f418b-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="f418b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f418b-102">SYNOPSIS</span></span>
<span data-ttu-id="f418b-103">Létrehozza a VMSS konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="f418b-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f418b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f418b-104">SYNTAX</span></span>

### <span data-ttu-id="f418b-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f418b-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f418b-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="f418b-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f418b-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="f418b-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f418b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f418b-108">DESCRIPTION</span></span>
<span data-ttu-id="f418b-109">A **New-AzureRmVmssConfig** parancsmag létrehoz egy konfigurálható helyi Virtual Manager Scale set (VMSS) objektumot.</span><span class="sxs-lookup"><span data-stu-id="f418b-109">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="f418b-110">A VMSS objektum konfigurálásához további parancsmagokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="f418b-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="f418b-111">Ezek a parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="f418b-111">These cmdlets are:</span></span>
- <span data-ttu-id="f418b-112">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="f418b-112">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="f418b-113">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="f418b-113">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="f418b-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f418b-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="f418b-115">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f418b-115">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="f418b-116">Példák</span><span class="sxs-lookup"><span data-stu-id="f418b-116">EXAMPLES</span></span>

### <span data-ttu-id="f418b-117">Példa 1: VMSS konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="f418b-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="f418b-118">Ebben a példában egy VMSS-konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f418b-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="f418b-119">Az első parancs a **New-AzureRmVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f418b-119">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="f418b-120">A második parancs a **New-AzureRmVmss** parancsmagot használja az első parancsban létrehozott VMSS konfigurációs OBJEKTUMOT használó VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="f418b-120">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="f418b-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f418b-121">PARAMETERS</span></span>

### <span data-ttu-id="f418b-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f418b-122">-AssignIdentity</span></span>
<span data-ttu-id="f418b-123">Adja meg a virtuálisgép-készlethez tartozó rendszerhez rendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="f418b-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="f418b-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="f418b-125">Azt adja meg, hogy az operációs rendszer frissítéseit a program automatikusan alkalmazza-e a méretarányos példányokra, ha a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="f418b-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="f418b-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f418b-126">-BootDiagnostic</span></span>
<span data-ttu-id="f418b-127">A virtuálisgép-készlet indítási diagnosztikai profilját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f418b-128">-DefaultProfile</span></span>
<span data-ttu-id="f418b-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f418b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="f418b-130">-DisableAutoRollback</span></span>
<span data-ttu-id="f418b-131">Automatikus visszagörgetés letiltása az automatikus operációs rendszer frissítési házirendjében</span><span class="sxs-lookup"><span data-stu-id="f418b-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="f418b-132">-EnableUltraSSD</span></span>
<span data-ttu-id="f418b-133">Lehetővé teszi, hogy egy vagy több felügyelt adatlemez legyen a virtuálisgép-készlet UltraSSD_LRS tárterület-fiók típusával.</span><span class="sxs-lookup"><span data-stu-id="f418b-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="f418b-134">A felügyelt lemezek tároló típusú UltraSSD_LRS csak akkor vehetők fel a VMSS, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="f418b-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="f418b-135">-EvictionPolicy</span></span>
<span data-ttu-id="f418b-136">A méretarányban a virtuális gépek kilakoltatási szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-137">-Extension (kiterjesztés)</span><span class="sxs-lookup"><span data-stu-id="f418b-137">-Extension</span></span>
<span data-ttu-id="f418b-138">A VMSS kiegészítő információs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="f418b-139">Ezt az objektumot az **Add-AzureRmVmssExtension** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-139">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="f418b-140">-HealthProbeId</span></span>
<span data-ttu-id="f418b-141">A virtuálisgép-készletben lévő példány állapotának meghatározásához használt terheléselosztó szonda AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="f418b-142">A HealthProbeId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}" formában jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="f418b-143">-IdentityId</span></span>
<span data-ttu-id="f418b-144">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="f418b-145">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="f418b-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f418b-146">-IdentityType</span></span>
<span data-ttu-id="f418b-147">A virtuálisgép-készlethez használt identitás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="f418b-148">Az "SystemAssignedUserAssigned" típus egy implicit módon létrehozott identitást és egy, a felhasználó által kiosztott identitást tartalmazó készletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="f418b-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="f418b-149">Ha a virtuálisgép-készletből eltávolítja az identitásokat, a "nincs" típust kell választania.</span><span class="sxs-lookup"><span data-stu-id="f418b-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="f418b-150">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f418b-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f418b-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="f418b-151">SystemAssigned</span></span>
- <span data-ttu-id="f418b-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="f418b-152">UserAssigned</span></span>
- <span data-ttu-id="f418b-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="f418b-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="f418b-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="f418b-154">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f418b-155">-LicenseType</span></span>
<span data-ttu-id="f418b-156">Adja meg azt a licenc-típust, amely a licencek használati forgatókönyvét hozza meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-156">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-157">-Hely</span><span class="sxs-lookup"><span data-stu-id="f418b-157">-Location</span></span>
<span data-ttu-id="f418b-158">Az az Azure-hely, ahol létrejön a VMSS.</span><span class="sxs-lookup"><span data-stu-id="f418b-158">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f418b-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="f418b-160">Megadja a VMSS konfigurációjának hálózati tulajdonságait tartalmazó hálózati profil objektumot.</span><span class="sxs-lookup"><span data-stu-id="f418b-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="f418b-161">Ezt az objektumot az **Add-AzureRmVmssNetworkInterfaceConfiguration** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-161">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="f418b-162">-OsProfile</span></span>
<span data-ttu-id="f418b-163">Annak az operációs rendszernek a profil-objektumát adja meg, amely az VMSS-konfiguráció operációs rendszerének tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f418b-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="f418b-164">Az objektum beállításához a **set-AzureRmVmssOsProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="f418b-164">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-165">-Túlszabályozás</span><span class="sxs-lookup"><span data-stu-id="f418b-165">-Overprovision</span></span>
<span data-ttu-id="f418b-166">Azt jelzi, hogy a parancsmag túla VMSS-e.</span><span class="sxs-lookup"><span data-stu-id="f418b-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-167">-PlanName</span><span class="sxs-lookup"><span data-stu-id="f418b-167">-PlanName</span></span>
<span data-ttu-id="f418b-168">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-168">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-169">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="f418b-169">-PlanProduct</span></span>
<span data-ttu-id="f418b-170">A csomag terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-170">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="f418b-171">-PlanPromotionCode</span></span>
<span data-ttu-id="f418b-172">A csomag-előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-172">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="f418b-173">-PlanPublisher</span></span>
<span data-ttu-id="f418b-174">A terv közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-174">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="f418b-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="f418b-176">Az egyes helyekhez tartozó hibák tartománya.</span><span class="sxs-lookup"><span data-stu-id="f418b-176">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-177">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="f418b-177">-Priority</span></span>
<span data-ttu-id="f418b-178">A beállított méretarányban a virtuális gépek prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-178">Specifies the priority for the virtual machines in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="f418b-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="f418b-180">A folyamatos frissítés szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-180">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f418b-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="f418b-182">Az egyetlen elhelyezés csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-182">Specifies the single placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f418b-183">-SkuCapacity</span></span>
<span data-ttu-id="f418b-184">A VMSS példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-184">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f418b-185">-SkuName</span></span>
<span data-ttu-id="f418b-186">A VMSS összes példányának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-186">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f418b-187">-SkuTier</span></span>
<span data-ttu-id="f418b-188">A VMSS küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="f418b-189">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f418b-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f418b-190">Standard</span><span class="sxs-lookup"><span data-stu-id="f418b-190">Standard</span></span>
- <span data-ttu-id="f418b-191">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="f418b-191">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="f418b-192">-StorageProfile</span></span>
<span data-ttu-id="f418b-193">A VMSS-konfigurációban a lemez tulajdonságait tartalmazó Storage profil objektum.</span><span class="sxs-lookup"><span data-stu-id="f418b-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="f418b-194">Az objektum beállításához a **set-AzureRmVmssStorageProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="f418b-194">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-195">-Címke</span><span class="sxs-lookup"><span data-stu-id="f418b-195">-Tag</span></span>
<span data-ttu-id="f418b-196">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="f418b-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f418b-197">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="f418b-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="f418b-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="f418b-199">A méretarányban a virtuális gépekre való frissítés módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="f418b-200">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f418b-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f418b-201">Automatikus</span><span class="sxs-lookup"><span data-stu-id="f418b-201">Automatic</span></span>
- <span data-ttu-id="f418b-202">Kézi</span><span class="sxs-lookup"><span data-stu-id="f418b-202">Manual</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-203">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="f418b-203">-Zone</span></span>
<span data-ttu-id="f418b-204">A virtuálisgép-készlethez tartozó zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f418b-204">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f418b-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="f418b-205">-ZoneBalance</span></span>
<span data-ttu-id="f418b-206">Annak megállapítása, hogy a virtuális gép csak a virtuális gépeken keresztül, több x-zónában van-e érvényben, ha van zóna</span><span class="sxs-lookup"><span data-stu-id="f418b-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="f418b-207">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f418b-207">-Confirm</span></span>
<span data-ttu-id="f418b-208">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f418b-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f418b-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f418b-209">-WhatIf</span></span>
<span data-ttu-id="f418b-210">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f418b-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f418b-211">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f418b-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f418b-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f418b-212">CommonParameters</span></span>
<span data-ttu-id="f418b-213">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f418b-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f418b-214">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f418b-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f418b-215">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f418b-215">INPUTS</span></span>

### <span data-ttu-id="f418b-216">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f418b-216">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f418b-217">System. String</span><span class="sxs-lookup"><span data-stu-id="f418b-217">System.String</span></span>

### <span data-ttu-id="f418b-218">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f418b-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f418b-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f418b-219">System.Int32</span></span>

### <span data-ttu-id="f418b-220">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. UpgradeMode, Microsoft. Azure. Management. kiszámítás, Version = 21.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f418b-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f418b-221">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="f418b-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="f418b-222">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="f418b-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="f418b-223">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f418b-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="f418b-224">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="f418b-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="f418b-225">System. string []</span><span class="sxs-lookup"><span data-stu-id="f418b-225">System.String[]</span></span>

### <span data-ttu-id="f418b-226">Microsoft. Azure. Management. kiszámítás. models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="f418b-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="f418b-227">Microsoft. Azure. Management. kiszámítás. models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f418b-227">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="f418b-228">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. ResourceIdentityType, Microsoft. Azure. Management. kiszámítás, Version = 21.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f418b-228">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="f418b-229">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f418b-229">OUTPUTS</span></span>

### <span data-ttu-id="f418b-230">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f418b-230">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f418b-231">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f418b-231">NOTES</span></span>

## <span data-ttu-id="f418b-232">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f418b-232">RELATED LINKS</span></span>

[<span data-ttu-id="f418b-233">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="f418b-233">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="f418b-234">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="f418b-234">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="f418b-235">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f418b-235">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="f418b-236">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f418b-236">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="f418b-237">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f418b-237">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

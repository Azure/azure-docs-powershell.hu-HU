---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 3c22f34b1dc4e01cf4e3ea2f2b3f9c6045197734
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002748"
---
# <span data-ttu-id="7514c-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7514c-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="7514c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7514c-102">SYNOPSIS</span></span>
<span data-ttu-id="7514c-103">Létrehozza a VMSS konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="7514c-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="7514c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7514c-104">SYNTAX</span></span>

### <span data-ttu-id="7514c-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7514c-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7514c-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7514c-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7514c-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7514c-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7514c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7514c-108">DESCRIPTION</span></span>
<span data-ttu-id="7514c-109">A **New-AzVmssConfig** parancsmag létrehoz egy konfigurálható helyi Virtual Manager Scale set (VMSS) objektumot.</span><span class="sxs-lookup"><span data-stu-id="7514c-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="7514c-110">A VMSS objektum konfigurálásához további parancsmagokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="7514c-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="7514c-111">Ezek a parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="7514c-111">These cmdlets are:</span></span>
- <span data-ttu-id="7514c-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="7514c-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="7514c-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7514c-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="7514c-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7514c-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="7514c-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="7514c-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="7514c-116">Példák</span><span class="sxs-lookup"><span data-stu-id="7514c-116">EXAMPLES</span></span>

### <span data-ttu-id="7514c-117">Példa 1: VMSS konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="7514c-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="7514c-118">Ebben a példában egy VMSS-konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7514c-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="7514c-119">Az első parancs a **New-AzVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7514c-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="7514c-120">A második parancs a **New-AzVmss** parancsmagot használja az első parancsban létrehozott VMSS konfigurációs OBJEKTUMOT használó VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="7514c-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="7514c-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7514c-121">PARAMETERS</span></span>

### <span data-ttu-id="7514c-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7514c-122">-AssignIdentity</span></span>
<span data-ttu-id="7514c-123">Adja meg a virtuálisgép-készlethez tartozó rendszerhez rendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="7514c-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="7514c-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="7514c-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="7514c-125">Az az idő, ameddig a VM-ben bekövetkezett változások miatt az automatikus javítás fel van függesztve.</span><span class="sxs-lookup"><span data-stu-id="7514c-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="7514c-126">A türelmi idő az állam módosításának befejeződése után kezdődik.</span><span class="sxs-lookup"><span data-stu-id="7514c-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="7514c-127">Ez segít elkerülni a korai vagy véletlenszerű javításokat.</span><span class="sxs-lookup"><span data-stu-id="7514c-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="7514c-128">Az időtartamot az ISO 8601-formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="7514c-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="7514c-129">Az alapértelmezett érték 5 perc (PT5M).</span><span class="sxs-lookup"><span data-stu-id="7514c-129">The default value is 5 minutes (PT5M).</span></span>

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

### <span data-ttu-id="7514c-130">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="7514c-130">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="7514c-131">A virtuális gépek százalékos aránya (scaleset), amely egyszerre kerül javításra.</span><span class="sxs-lookup"><span data-stu-id="7514c-131">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="7514c-132">Az alapértelmezett érték 20%.</span><span class="sxs-lookup"><span data-stu-id="7514c-132">The default value is 20%.</span></span>

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

### <span data-ttu-id="7514c-133">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="7514c-133">-AutoOSUpgrade</span></span>
<span data-ttu-id="7514c-134">Azt adja meg, hogy az operációs rendszer frissítéseit a program automatikusan alkalmazza-e a méretarányos példányokra, ha a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="7514c-134">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="7514c-135">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7514c-135">-BootDiagnostic</span></span>
<span data-ttu-id="7514c-136">A virtuálisgép-készlet indítási diagnosztikai profilját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-136">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="7514c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7514c-137">-DefaultProfile</span></span>
<span data-ttu-id="7514c-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7514c-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7514c-139">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="7514c-139">-DisableAutoRollback</span></span>
<span data-ttu-id="7514c-140">Automatikus visszagörgetés letiltása az automatikus operációs rendszer frissítési házirendjében</span><span class="sxs-lookup"><span data-stu-id="7514c-140">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="7514c-141">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="7514c-141">-EnableAutomaticRepair</span></span>
<span data-ttu-id="7514c-142">Engedélyezi az automatikus javítást a virtuálisgép-méretarány beállításakor.</span><span class="sxs-lookup"><span data-stu-id="7514c-142">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="7514c-143">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="7514c-143">-EnableUltraSSD</span></span>
<span data-ttu-id="7514c-144">Lehetővé teszi, hogy egy vagy több felügyelt adatlemez legyen a virtuálisgép-készlet UltraSSD_LRS tárterület-fiók típusával.</span><span class="sxs-lookup"><span data-stu-id="7514c-144">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="7514c-145">A felügyelt lemezek tároló típusú UltraSSD_LRS csak akkor vehetők fel a VMSS, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="7514c-145">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="7514c-146">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="7514c-146">-EvictionPolicy</span></span>
<span data-ttu-id="7514c-147">A méretarányban a virtuális gépek kilakoltatási szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-147">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="7514c-148">-Extension (kiterjesztés)</span><span class="sxs-lookup"><span data-stu-id="7514c-148">-Extension</span></span>
<span data-ttu-id="7514c-149">A VMSS kiegészítő információs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-149">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="7514c-150">Ezt az objektumot az **Add-AzVmssExtension** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-150">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7514c-151">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="7514c-151">-HealthProbeId</span></span>
<span data-ttu-id="7514c-152">A virtuálisgép-készletben lévő példány állapotának meghatározásához használt terheléselosztó szonda AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-152">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="7514c-153">A HealthProbeId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}" formában jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-153">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="7514c-154">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="7514c-154">-IdentityId</span></span>
<span data-ttu-id="7514c-155">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-155">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="7514c-156">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="7514c-156">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="7514c-157">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7514c-157">-IdentityType</span></span>
<span data-ttu-id="7514c-158">A virtuálisgép-készlethez használt identitás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-158">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="7514c-159">Az "SystemAssignedUserAssigned" típus egy implicit módon létrehozott identitást és egy, a felhasználó által kiosztott identitást tartalmazó készletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="7514c-159">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="7514c-160">Ha a virtuálisgép-készletből eltávolítja az identitásokat, a "nincs" típust kell választania.</span><span class="sxs-lookup"><span data-stu-id="7514c-160">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="7514c-161">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7514c-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7514c-162">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="7514c-162">SystemAssigned</span></span>
- <span data-ttu-id="7514c-163">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="7514c-163">UserAssigned</span></span>
- <span data-ttu-id="7514c-164">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="7514c-164">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="7514c-165">Nincs</span><span class="sxs-lookup"><span data-stu-id="7514c-165">None</span></span>

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

### <span data-ttu-id="7514c-166">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7514c-166">-LicenseType</span></span>
<span data-ttu-id="7514c-167">Adja meg azt a licenc-típust, amely a licencek használati forgatókönyvét hozza meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-167">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="7514c-168">-Hely</span><span class="sxs-lookup"><span data-stu-id="7514c-168">-Location</span></span>
<span data-ttu-id="7514c-169">Az az Azure-hely, ahol létrejön a VMSS.</span><span class="sxs-lookup"><span data-stu-id="7514c-169">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="7514c-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="7514c-170">-MaxPrice</span></span>
<span data-ttu-id="7514c-171">Itt adhatja meg, hogy az alacsony prioritású VM/VMSS milyen maximális árat fizessen.</span><span class="sxs-lookup"><span data-stu-id="7514c-171">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="7514c-172">Ez az ár amerikai dollárban van.</span><span class="sxs-lookup"><span data-stu-id="7514c-172">This price is in US Dollars.</span></span> <span data-ttu-id="7514c-173">Ezt az árat a program összehasonlítja a VM-méret jelenlegi alacsony prioritási árával.</span><span class="sxs-lookup"><span data-stu-id="7514c-173">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="7514c-174">Az árakat az alacsony prioritású VM/VMSS létrehozásának/frissítésének időpontjában is összehasonlították, és a művelet csak akkor fog sikerülni, ha a maxPrice nagyobb, mint a jelenlegi alacsony prioritású ár.</span><span class="sxs-lookup"><span data-stu-id="7514c-174">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="7514c-175">A maxPrice a VM/VMSS létrehozása után is az alacsony prioritású VM/VMSS eltávolítására használható, ha a jelenlegi alacsony prioritású ár túllépi a maxPrice.</span><span class="sxs-lookup"><span data-stu-id="7514c-175">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="7514c-176">Lehetséges értékek: bármely nullánál nagyobb decimális érték.</span><span class="sxs-lookup"><span data-stu-id="7514c-176">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="7514c-177">Példa: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="7514c-177">Example: 0.01538.</span></span>  <span data-ttu-id="7514c-178">-1 – azt jelzi, hogy az alacsony prioritású VM/VMSS nem szabad az árak miatt kizárni.</span><span class="sxs-lookup"><span data-stu-id="7514c-178">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="7514c-179">Az alapértelmezett Max ár is-1, ha az nem az Ön által megadott.</span><span class="sxs-lookup"><span data-stu-id="7514c-179">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7514c-180">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7514c-180">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="7514c-181">Megadja a VMSS konfigurációjának hálózati tulajdonságait tartalmazó hálózati profil objektumot.</span><span class="sxs-lookup"><span data-stu-id="7514c-181">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="7514c-182">Ezt az objektumot az **Add-AzVmssNetworkInterfaceConfiguration** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-182">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="7514c-183">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="7514c-183">-OsProfile</span></span>
<span data-ttu-id="7514c-184">Annak az operációs rendszernek a profil-objektumát adja meg, amely az VMSS-konfiguráció operációs rendszerének tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7514c-184">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="7514c-185">Az objektum beállításához a **set-AzVmssOsProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="7514c-185">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="7514c-186">-Túlszabályozás</span><span class="sxs-lookup"><span data-stu-id="7514c-186">-Overprovision</span></span>
<span data-ttu-id="7514c-187">Azt jelzi, hogy a parancsmag túla VMSS-e.</span><span class="sxs-lookup"><span data-stu-id="7514c-187">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="7514c-188">-PlanName</span><span class="sxs-lookup"><span data-stu-id="7514c-188">-PlanName</span></span>
<span data-ttu-id="7514c-189">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-189">Specifies the plan name.</span></span>

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

### <span data-ttu-id="7514c-190">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="7514c-190">-PlanProduct</span></span>
<span data-ttu-id="7514c-191">A csomag terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-191">Specifies the plan product.</span></span>

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

### <span data-ttu-id="7514c-192">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="7514c-192">-PlanPromotionCode</span></span>
<span data-ttu-id="7514c-193">A csomag-előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-193">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="7514c-194">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="7514c-194">-PlanPublisher</span></span>
<span data-ttu-id="7514c-195">A terv közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-195">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="7514c-196">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="7514c-196">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="7514c-197">Az egyes helyekhez tartozó hibák tartománya.</span><span class="sxs-lookup"><span data-stu-id="7514c-197">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="7514c-198">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="7514c-198">-Priority</span></span>
<span data-ttu-id="7514c-199">A méretarányban a virtuális machien prioritása.</span><span class="sxs-lookup"><span data-stu-id="7514c-199">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="7514c-200">Csak a támogatott értékek "normál", "spot" és "Low".</span><span class="sxs-lookup"><span data-stu-id="7514c-200">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="7514c-201">"Normál": a normál virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="7514c-201">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="7514c-202">A "spot" a direkt virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="7514c-202">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="7514c-203">Az "alacsony" a direkt virtuális gép is, de a helyére "spot" lép.</span><span class="sxs-lookup"><span data-stu-id="7514c-203">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="7514c-204">Kérjük, hogy az "alacsony" helyett a "spot" értéket használja.</span><span class="sxs-lookup"><span data-stu-id="7514c-204">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="7514c-205">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="7514c-205">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="7514c-206">Annak a közelségi helynek az erőforrás azonosítója, amellyel az adott méretarányt használni szeretné.</span><span class="sxs-lookup"><span data-stu-id="7514c-206">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="7514c-207">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="7514c-207">-RollingUpgradePolicy</span></span>
<span data-ttu-id="7514c-208">A folyamatos frissítés szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-208">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="7514c-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="7514c-209">-ScaleInPolicy</span></span>
<span data-ttu-id="7514c-210">A virtuális gép méretarányának beállításakor követendő szabályok.</span><span class="sxs-lookup"><span data-stu-id="7514c-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="7514c-211">A lehetséges értékek a következők: "alapértelmezett", "OldestVM" és "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="7514c-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="7514c-212">"Alapértelmezett": Ha egy virtuális gép méretarányát a program átméretezi, a program először a méretarányokat fogja kiegyensúlyozni a zónáknál, ha a zóna zóna.</span><span class="sxs-lookup"><span data-stu-id="7514c-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="7514c-213">Ezt követően a lehető legtöbbet fogja kiegyensúlyozni a hibák tartományában.</span><span class="sxs-lookup"><span data-stu-id="7514c-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="7514c-214">Az egyes hibák tartománya alatt az eltávolításra kiválasztott virtuális gépek a legújabbak lesznek, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="7514c-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="7514c-215">"OldestVM": Ha egy virtuálisgép-készletet méretarányos, a program a legrégebbi virtuális gépeket választja, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="7514c-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="7514c-216">A virtuális gép méretarányos készletei esetében a méretarány először a zónáknál lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="7514c-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="7514c-217">Az egyes zónákon belül a legrégebbi virtuális gépeket választják ki a program az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="7514c-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="7514c-218">"NewestVM": Ha egy virtuálisgép-készletet méretezéssel végeznek, a program az eltávolításhoz a legújabb virtuális gépeket választja, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="7514c-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="7514c-219">A virtuális gép méretarányos készletei esetében a méretarány először a zónáknál lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="7514c-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="7514c-220">Az egyes zónákon belül a legújabb virtuális gépek, amelyek nem védettek, kiválasztásra kerülnek az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="7514c-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="7514c-221">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7514c-221">-SinglePlacementGroup</span></span>
<span data-ttu-id="7514c-222">Az egyetlen elhelyezés csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-222">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="7514c-223">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="7514c-223">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="7514c-224">Azt adja meg, hogy a bővítmények nem futnak az extra túlépített VMs-eszközön.</span><span class="sxs-lookup"><span data-stu-id="7514c-224">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="7514c-225">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7514c-225">-SkuCapacity</span></span>
<span data-ttu-id="7514c-226">A VMSS példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-226">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="7514c-227">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7514c-227">-SkuName</span></span>
<span data-ttu-id="7514c-228">A VMSS összes példányának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-228">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="7514c-229">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="7514c-229">-SkuTier</span></span>
<span data-ttu-id="7514c-230">A VMSS küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-230">Specifies the tier of VMSS.</span></span> <span data-ttu-id="7514c-231">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7514c-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7514c-232">Standard</span><span class="sxs-lookup"><span data-stu-id="7514c-232">Standard</span></span>
- <span data-ttu-id="7514c-233">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="7514c-233">Basic</span></span>

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

### <span data-ttu-id="7514c-234">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="7514c-234">-StorageProfile</span></span>
<span data-ttu-id="7514c-235">A VMSS-konfigurációban a lemez tulajdonságait tartalmazó Storage profil objektum.</span><span class="sxs-lookup"><span data-stu-id="7514c-235">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="7514c-236">Az objektum beállításához a **set-AzVmssStorageProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="7514c-236">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="7514c-237">-Címke</span><span class="sxs-lookup"><span data-stu-id="7514c-237">-Tag</span></span>
<span data-ttu-id="7514c-238">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="7514c-238">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7514c-239">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="7514c-239">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7514c-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7514c-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="7514c-241">Konfigurálható időtartam (percben) a törölt virtuális gépet az esemény automatikus jóváhagyása előtt jóvá kell hagynia a befejezési ütemezett esemény előtt (időtúllépés esetén).</span><span class="sxs-lookup"><span data-stu-id="7514c-241">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="7514c-242">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="7514c-242">-TerminateScheduledEvents</span></span>
<span data-ttu-id="7514c-243">Az ütemezett események befejezésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="7514c-243">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="7514c-244">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="7514c-244">-UpgradePolicyMode</span></span>
<span data-ttu-id="7514c-245">A méretarányban a virtuális gépekre való frissítés módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-245">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="7514c-246">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7514c-246">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7514c-247">Automatikus</span><span class="sxs-lookup"><span data-stu-id="7514c-247">Automatic</span></span>
- <span data-ttu-id="7514c-248">Kézi</span><span class="sxs-lookup"><span data-stu-id="7514c-248">Manual</span></span>

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

### <span data-ttu-id="7514c-249">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="7514c-249">-Zone</span></span>
<span data-ttu-id="7514c-250">A virtuálisgép-készlethez tartozó zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7514c-250">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="7514c-251">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="7514c-251">-ZoneBalance</span></span>
<span data-ttu-id="7514c-252">Annak megállapítása, hogy a virtuális gép csak a virtuális gépeken keresztül, több x-zónában van-e érvényben, ha van zóna</span><span class="sxs-lookup"><span data-stu-id="7514c-252">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="7514c-253">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7514c-253">-Confirm</span></span>
<span data-ttu-id="7514c-254">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7514c-254">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7514c-255">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7514c-255">-WhatIf</span></span>
<span data-ttu-id="7514c-256">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7514c-256">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7514c-257">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7514c-257">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7514c-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7514c-258">CommonParameters</span></span>
<span data-ttu-id="7514c-259">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7514c-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7514c-260">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7514c-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7514c-261">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7514c-261">INPUTS</span></span>

### <span data-ttu-id="7514c-262">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7514c-262">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7514c-263">System. String</span><span class="sxs-lookup"><span data-stu-id="7514c-263">System.String</span></span>

### <span data-ttu-id="7514c-264">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7514c-264">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7514c-265">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7514c-265">System.Int32</span></span>

### <span data-ttu-id="7514c-266">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. UpgradeMode, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7514c-266">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7514c-267">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="7514c-267">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="7514c-268">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7514c-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="7514c-269">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="7514c-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="7514c-270">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="7514c-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="7514c-271">System. string []</span><span class="sxs-lookup"><span data-stu-id="7514c-271">System.String[]</span></span>

### <span data-ttu-id="7514c-272">Microsoft. Azure. Management. kiszámítás. models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="7514c-272">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="7514c-273">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7514c-273">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7514c-274">Microsoft. Azure. Management. kiszámítás. models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7514c-274">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="7514c-275">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. ResourceIdentityType, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7514c-275">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="7514c-276">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7514c-276">OUTPUTS</span></span>

### <span data-ttu-id="7514c-277">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7514c-277">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7514c-278">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7514c-278">NOTES</span></span>

## <span data-ttu-id="7514c-279">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7514c-279">RELATED LINKS</span></span>

[<span data-ttu-id="7514c-280">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="7514c-280">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="7514c-281">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7514c-281">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="7514c-282">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7514c-282">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="7514c-283">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="7514c-283">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="7514c-284">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="7514c-284">New-AzVmss</span></span>](./New-AzVmss.md)

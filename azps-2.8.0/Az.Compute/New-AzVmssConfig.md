---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: e65bfa607f9689a85f7734b1913bbabadd4dd115
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667347"
---
# <span data-ttu-id="4e3c9-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4e3c9-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="4e3c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="4e3c9-103">Létrehozza a VMSS konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="4e3c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e3c9-104">SYNTAX</span></span>

### <span data-ttu-id="4e3c9-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e3c9-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e3c9-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e3c9-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e3c9-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e3c9-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e3c9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e3c9-108">DESCRIPTION</span></span>
<span data-ttu-id="4e3c9-109">A **New-AzVmssConfig** parancsmag létrehoz egy konfigurálható helyi Virtual Manager Scale set (VMSS) objektumot.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="4e3c9-110">A VMSS objektum konfigurálásához további parancsmagokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="4e3c9-111">Ezek a parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="4e3c9-111">These cmdlets are:</span></span>
- <span data-ttu-id="4e3c9-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="4e3c9-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="4e3c9-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="4e3c9-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="4e3c9-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e3c9-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="4e3c9-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4e3c9-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="4e3c9-116">Példák</span><span class="sxs-lookup"><span data-stu-id="4e3c9-116">EXAMPLES</span></span>

### <span data-ttu-id="4e3c9-117">Példa 1: VMSS konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="4e3c9-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="4e3c9-118">Ebben a példában egy VMSS-konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="4e3c9-119">Az első parancs a **New-AzVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="4e3c9-120">A második parancs a **New-AzVmss** parancsmagot használja az első parancsban létrehozott VMSS konfigurációs OBJEKTUMOT használó VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="4e3c9-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e3c9-121">PARAMETERS</span></span>

### <span data-ttu-id="4e3c9-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4e3c9-122">-AssignIdentity</span></span>
<span data-ttu-id="4e3c9-123">Adja meg a virtuálisgép-készlethez tartozó rendszerhez rendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="4e3c9-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="4e3c9-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="4e3c9-125">Azt adja meg, hogy az operációs rendszer frissítéseit a program automatikusan alkalmazza-e a méretarányos példányokra, ha a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="4e3c9-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4e3c9-126">-BootDiagnostic</span></span>
<span data-ttu-id="4e3c9-127">A virtuálisgép-készlet indítási diagnosztikai profilját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="4e3c9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e3c9-128">-DefaultProfile</span></span>
<span data-ttu-id="4e3c9-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e3c9-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="4e3c9-130">-DisableAutoRollback</span></span>
<span data-ttu-id="4e3c9-131">Automatikus visszagörgetés letiltása az automatikus operációs rendszer frissítési házirendjében</span><span class="sxs-lookup"><span data-stu-id="4e3c9-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="4e3c9-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="4e3c9-132">-EnableUltraSSD</span></span>
<span data-ttu-id="4e3c9-133">Lehetővé teszi, hogy egy vagy több felügyelt adatlemez legyen a virtuálisgép-készlet UltraSSD_LRS tárterület-fiók típusával.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="4e3c9-134">A felügyelt lemezek tároló típusú UltraSSD_LRS csak akkor vehetők fel a VMSS, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="4e3c9-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="4e3c9-135">-EvictionPolicy</span></span>
<span data-ttu-id="4e3c9-136">A méretarányban a virtuális gépek kilakoltatási szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="4e3c9-137">-Extension (kiterjesztés)</span><span class="sxs-lookup"><span data-stu-id="4e3c9-137">-Extension</span></span>
<span data-ttu-id="4e3c9-138">A VMSS kiegészítő információs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="4e3c9-139">Ezt az objektumot az **Add-AzVmssExtension** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-139">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="4e3c9-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="4e3c9-140">-HealthProbeId</span></span>
<span data-ttu-id="4e3c9-141">A virtuálisgép-készletben lévő példány állapotának meghatározásához használt terheléselosztó szonda AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="4e3c9-142">A HealthProbeId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}" formában jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="4e3c9-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="4e3c9-143">-IdentityId</span></span>
<span data-ttu-id="4e3c9-144">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="4e3c9-145">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="4e3c9-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4e3c9-146">-IdentityType</span></span>
<span data-ttu-id="4e3c9-147">A virtuálisgép-készlethez használt identitás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="4e3c9-148">Az "SystemAssignedUserAssigned" típus egy implicit módon létrehozott identitást és egy, a felhasználó által kiosztott identitást tartalmazó készletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="4e3c9-149">Ha a virtuálisgép-készletből eltávolítja az identitásokat, a "nincs" típust kell választania.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="4e3c9-150">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4e3c9-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e3c9-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="4e3c9-151">SystemAssigned</span></span>
- <span data-ttu-id="4e3c9-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="4e3c9-152">UserAssigned</span></span>
- <span data-ttu-id="4e3c9-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="4e3c9-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="4e3c9-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="4e3c9-154">None</span></span>

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

### <span data-ttu-id="4e3c9-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4e3c9-155">-LicenseType</span></span>
<span data-ttu-id="4e3c9-156">Adja meg azt a licenc-típust, amely a licencek használati forgatókönyvét hozza meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="4e3c9-157">-Hely</span><span class="sxs-lookup"><span data-stu-id="4e3c9-157">-Location</span></span>
<span data-ttu-id="4e3c9-158">Az az Azure-hely, ahol létrejön a VMSS.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="4e3c9-159">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="4e3c9-159">-MaxPrice</span></span>
<span data-ttu-id="4e3c9-160">Itt adhatja meg, hogy az alacsony prioritású VM/VMSS milyen maximális árat fizessen.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-160">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="4e3c9-161">Ez az ár amerikai dollárban van.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-161">This price is in US Dollars.</span></span> <span data-ttu-id="4e3c9-162">Ezt az árat a program összehasonlítja a VM-méret jelenlegi alacsony prioritási árával.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-162">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="4e3c9-163">Az árakat az alacsony prioritású VM/VMSS létrehozásának/frissítésének időpontjában is összehasonlították, és a művelet csak akkor fog sikerülni, ha a maxPrice nagyobb, mint a jelenlegi alacsony prioritású ár.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-163">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="4e3c9-164">A maxPrice a VM/VMSS létrehozása után is az alacsony prioritású VM/VMSS eltávolítására használható, ha a jelenlegi alacsony prioritású ár túllépi a maxPrice.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-164">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="4e3c9-165">Lehetséges értékek: bármely nullánál nagyobb decimális érték.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-165">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="4e3c9-166">Példa: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-166">Example: 0.01538.</span></span>  <span data-ttu-id="4e3c9-167">-1 – azt jelzi, hogy az alacsony prioritású VM/VMSS nem szabad az árak miatt kizárni.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-167">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="4e3c9-168">Az alapértelmezett Max ár is-1, ha az nem az Ön által megadott.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-168">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="4e3c9-169">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e3c9-169">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="4e3c9-170">Megadja a VMSS konfigurációjának hálózati tulajdonságait tartalmazó hálózati profil objektumot.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-170">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="4e3c9-171">Ezt az objektumot az **Add-AzVmssNetworkInterfaceConfiguration** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-171">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="4e3c9-172">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="4e3c9-172">-OsProfile</span></span>
<span data-ttu-id="4e3c9-173">Annak az operációs rendszernek a profil-objektumát adja meg, amely az VMSS-konfiguráció operációs rendszerének tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-173">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="4e3c9-174">Az objektum beállításához a **set-AzVmssOsProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-174">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="4e3c9-175">-Túlszabályozás</span><span class="sxs-lookup"><span data-stu-id="4e3c9-175">-Overprovision</span></span>
<span data-ttu-id="4e3c9-176">Azt jelzi, hogy a parancsmag túla VMSS-e.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-176">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="4e3c9-177">-PlanName</span><span class="sxs-lookup"><span data-stu-id="4e3c9-177">-PlanName</span></span>
<span data-ttu-id="4e3c9-178">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-178">Specifies the plan name.</span></span>

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

### <span data-ttu-id="4e3c9-179">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="4e3c9-179">-PlanProduct</span></span>
<span data-ttu-id="4e3c9-180">A csomag terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-180">Specifies the plan product.</span></span>

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

### <span data-ttu-id="4e3c9-181">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="4e3c9-181">-PlanPromotionCode</span></span>
<span data-ttu-id="4e3c9-182">A csomag-előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-182">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="4e3c9-183">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="4e3c9-183">-PlanPublisher</span></span>
<span data-ttu-id="4e3c9-184">A terv közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-184">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="4e3c9-185">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="4e3c9-185">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="4e3c9-186">Az egyes helyekhez tartozó hibák tartománya.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-186">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="4e3c9-187">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="4e3c9-187">-Priority</span></span>
<span data-ttu-id="4e3c9-188">A beállított méretarányban a virtuális gépek prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-188">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="4e3c9-189">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="4e3c9-189">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="4e3c9-190">A ProximityPlacementGroup azonosítója</span><span class="sxs-lookup"><span data-stu-id="4e3c9-190">The Id of ProximityPlacementGroup</span></span>

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

### <span data-ttu-id="4e3c9-191">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="4e3c9-191">-RollingUpgradePolicy</span></span>
<span data-ttu-id="4e3c9-192">A folyamatos frissítés szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-192">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="4e3c9-193">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="4e3c9-193">-SinglePlacementGroup</span></span>
<span data-ttu-id="4e3c9-194">Az egyetlen elhelyezés csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-194">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="4e3c9-195">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4e3c9-195">-SkuCapacity</span></span>
<span data-ttu-id="4e3c9-196">A VMSS példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-196">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="4e3c9-197">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4e3c9-197">-SkuName</span></span>
<span data-ttu-id="4e3c9-198">A VMSS összes példányának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-198">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="4e3c9-199">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4e3c9-199">-SkuTier</span></span>
<span data-ttu-id="4e3c9-200">A VMSS küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-200">Specifies the tier of VMSS.</span></span> <span data-ttu-id="4e3c9-201">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4e3c9-201">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e3c9-202">Standard</span><span class="sxs-lookup"><span data-stu-id="4e3c9-202">Standard</span></span>
- <span data-ttu-id="4e3c9-203">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="4e3c9-203">Basic</span></span>

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

### <span data-ttu-id="4e3c9-204">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="4e3c9-204">-StorageProfile</span></span>
<span data-ttu-id="4e3c9-205">A VMSS-konfigurációban a lemez tulajdonságait tartalmazó Storage profil objektum.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-205">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="4e3c9-206">Az objektum beállításához a **set-AzVmssStorageProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-206">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="4e3c9-207">-Címke</span><span class="sxs-lookup"><span data-stu-id="4e3c9-207">-Tag</span></span>
<span data-ttu-id="4e3c9-208">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-208">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4e3c9-209">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="4e3c9-209">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4e3c9-210">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4e3c9-210">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="4e3c9-211">Konfigurálható időtartam (percben) a törölt virtuális gépet az esemény automatikus jóváhagyása előtt jóvá kell hagynia a befejezési ütemezett esemény előtt (időtúllépés esetén).</span><span class="sxs-lookup"><span data-stu-id="4e3c9-211">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="4e3c9-212">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="4e3c9-212">-TerminateScheduledEvents</span></span>
<span data-ttu-id="4e3c9-213">Az ütemezett események befejezésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="4e3c9-213">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="4e3c9-214">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="4e3c9-214">-UpgradePolicyMode</span></span>
<span data-ttu-id="4e3c9-215">A méretarányban a virtuális gépekre való frissítés módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-215">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="4e3c9-216">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4e3c9-216">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4e3c9-217">Automatikus</span><span class="sxs-lookup"><span data-stu-id="4e3c9-217">Automatic</span></span>
- <span data-ttu-id="4e3c9-218">Kézi</span><span class="sxs-lookup"><span data-stu-id="4e3c9-218">Manual</span></span>

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

### <span data-ttu-id="4e3c9-219">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="4e3c9-219">-Zone</span></span>
<span data-ttu-id="4e3c9-220">A virtuálisgép-készlethez tartozó zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-220">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="4e3c9-221">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="4e3c9-221">-ZoneBalance</span></span>
<span data-ttu-id="4e3c9-222">Annak megállapítása, hogy a virtuális gép csak a virtuális gépeken keresztül, több x-zónában van-e érvényben, ha van zóna</span><span class="sxs-lookup"><span data-stu-id="4e3c9-222">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="4e3c9-223">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4e3c9-223">-Confirm</span></span>
<span data-ttu-id="4e3c9-224">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e3c9-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e3c9-225">-WhatIf</span></span>
<span data-ttu-id="4e3c9-226">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-226">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e3c9-227">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e3c9-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e3c9-228">CommonParameters</span></span>
<span data-ttu-id="4e3c9-229">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e3c9-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e3c9-230">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4e3c9-230">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e3c9-231">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e3c9-231">INPUTS</span></span>

### <span data-ttu-id="4e3c9-232">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4e3c9-232">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4e3c9-233">System. String</span><span class="sxs-lookup"><span data-stu-id="4e3c9-233">System.String</span></span>

### <span data-ttu-id="4e3c9-234">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4e3c9-234">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4e3c9-235">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4e3c9-235">System.Int32</span></span>

### <span data-ttu-id="4e3c9-236">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. UpgradeMode, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4e3c9-236">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="4e3c9-237">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="4e3c9-237">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="4e3c9-238">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="4e3c9-238">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="4e3c9-239">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="4e3c9-239">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="4e3c9-240">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="4e3c9-240">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="4e3c9-241">System. string []</span><span class="sxs-lookup"><span data-stu-id="4e3c9-241">System.String[]</span></span>

### <span data-ttu-id="4e3c9-242">Microsoft. Azure. Management. kiszámítás. models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="4e3c9-242">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="4e3c9-243">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4e3c9-243">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4e3c9-244">Microsoft. Azure. Management. kiszámítás. models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4e3c9-244">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="4e3c9-245">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. ResourceIdentityType, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4e3c9-245">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="4e3c9-246">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e3c9-246">OUTPUTS</span></span>

### <span data-ttu-id="4e3c9-247">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4e3c9-247">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4e3c9-248">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e3c9-248">NOTES</span></span>

## <span data-ttu-id="4e3c9-249">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e3c9-249">RELATED LINKS</span></span>

[<span data-ttu-id="4e3c9-250">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="4e3c9-250">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="4e3c9-251">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="4e3c9-251">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="4e3c9-252">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e3c9-252">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="4e3c9-253">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4e3c9-253">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="4e3c9-254">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="4e3c9-254">New-AzVmss</span></span>](./New-AzVmss.md)

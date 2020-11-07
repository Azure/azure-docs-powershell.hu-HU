---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: beb9c067fb2ca625fcf756747a52eef0bf1ca9b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671299"
---
# <span data-ttu-id="bc333-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="bc333-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="bc333-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc333-102">SYNOPSIS</span></span>
<span data-ttu-id="bc333-103">Létrehozza a VMSS konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="bc333-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="bc333-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc333-104">SYNTAX</span></span>

### <span data-ttu-id="bc333-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bc333-105">DefaultParameterSet (Default)</span></span>
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
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc333-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc333-106">ExplicitIdentityParameterSet</span></span>
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
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc333-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc333-107">AssignIdentityParameterSet</span></span>
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
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc333-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc333-108">DESCRIPTION</span></span>
<span data-ttu-id="bc333-109">A **New-AzVmssConfig** parancsmag létrehoz egy konfigurálható helyi Virtual Manager Scale set (VMSS) objektumot.</span><span class="sxs-lookup"><span data-stu-id="bc333-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="bc333-110">A VMSS objektum konfigurálásához további parancsmagokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="bc333-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="bc333-111">Ezek a parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="bc333-111">These cmdlets are:</span></span>
- <span data-ttu-id="bc333-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="bc333-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="bc333-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="bc333-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="bc333-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc333-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="bc333-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="bc333-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="bc333-116">Példák</span><span class="sxs-lookup"><span data-stu-id="bc333-116">EXAMPLES</span></span>

### <span data-ttu-id="bc333-117">Példa 1: VMSS konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="bc333-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="bc333-118">Ebben a példában egy VMSS-konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bc333-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="bc333-119">Az első parancs a **New-AzVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="bc333-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="bc333-120">A második parancs a **New-AzVmss** parancsmagot használja az első parancsban létrehozott VMSS konfigurációs OBJEKTUMOT használó VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="bc333-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="bc333-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc333-121">PARAMETERS</span></span>

### <span data-ttu-id="bc333-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="bc333-122">-AssignIdentity</span></span>
<span data-ttu-id="bc333-123">Adja meg a virtuálisgép-készlethez tartozó rendszerhez rendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="bc333-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="bc333-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="bc333-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="bc333-125">Azt adja meg, hogy az operációs rendszer frissítéseit a program automatikusan alkalmazza-e a méretarányos példányokra, ha a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="bc333-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="bc333-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bc333-126">-BootDiagnostic</span></span>
<span data-ttu-id="bc333-127">A virtuálisgép-készlet indítási diagnosztikai profilját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="bc333-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc333-128">-DefaultProfile</span></span>
<span data-ttu-id="bc333-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc333-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc333-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="bc333-130">-DisableAutoRollback</span></span>
<span data-ttu-id="bc333-131">Automatikus visszagörgetés letiltása az automatikus operációs rendszer frissítési házirendjében</span><span class="sxs-lookup"><span data-stu-id="bc333-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="bc333-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="bc333-132">-EnableUltraSSD</span></span>
<span data-ttu-id="bc333-133">Lehetővé teszi, hogy egy vagy több felügyelt adatlemez legyen a virtuálisgép-készlet UltraSSD_LRS tárterület-fiók típusával.</span><span class="sxs-lookup"><span data-stu-id="bc333-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="bc333-134">A felügyelt lemezek tároló típusú UltraSSD_LRS csak akkor vehetők fel a VMSS, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="bc333-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="bc333-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="bc333-135">-EvictionPolicy</span></span>
<span data-ttu-id="bc333-136">A méretarányban a virtuális gépek kilakoltatási szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="bc333-137">-Extension (kiterjesztés)</span><span class="sxs-lookup"><span data-stu-id="bc333-137">-Extension</span></span>
<span data-ttu-id="bc333-138">A VMSS kiegészítő információs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="bc333-139">Ezt az objektumot az **Add-AzVmssExtension** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-139">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="bc333-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="bc333-140">-HealthProbeId</span></span>
<span data-ttu-id="bc333-141">A virtuálisgép-készletben lévő példány állapotának meghatározásához használt terheléselosztó szonda AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="bc333-142">A HealthProbeId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}" formában jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="bc333-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="bc333-143">-IdentityId</span></span>
<span data-ttu-id="bc333-144">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="bc333-145">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="bc333-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="bc333-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="bc333-146">-IdentityType</span></span>
<span data-ttu-id="bc333-147">A virtuálisgép-készlethez használt identitás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="bc333-148">Az "SystemAssignedUserAssigned" típus egy implicit módon létrehozott identitást és egy, a felhasználó által kiosztott identitást tartalmazó készletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="bc333-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="bc333-149">Ha a virtuálisgép-készletből eltávolítja az identitásokat, a "nincs" típust kell választania.</span><span class="sxs-lookup"><span data-stu-id="bc333-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="bc333-150">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bc333-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc333-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="bc333-151">SystemAssigned</span></span>
- <span data-ttu-id="bc333-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="bc333-152">UserAssigned</span></span>
- <span data-ttu-id="bc333-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="bc333-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="bc333-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="bc333-154">None</span></span>

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

### <span data-ttu-id="bc333-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="bc333-155">-LicenseType</span></span>
<span data-ttu-id="bc333-156">Adja meg azt a licenc-típust, amely a licencek használati forgatókönyvét hozza meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="bc333-157">-Hely</span><span class="sxs-lookup"><span data-stu-id="bc333-157">-Location</span></span>
<span data-ttu-id="bc333-158">Az az Azure-hely, ahol létrejön a VMSS.</span><span class="sxs-lookup"><span data-stu-id="bc333-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="bc333-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc333-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="bc333-160">Megadja a VMSS konfigurációjának hálózati tulajdonságait tartalmazó hálózati profil objektumot.</span><span class="sxs-lookup"><span data-stu-id="bc333-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="bc333-161">Ezt az objektumot az **Add-AzVmssNetworkInterfaceConfiguration** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-161">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="bc333-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="bc333-162">-OsProfile</span></span>
<span data-ttu-id="bc333-163">Annak az operációs rendszernek a profil-objektumát adja meg, amely az VMSS-konfiguráció operációs rendszerének tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bc333-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="bc333-164">Az objektum beállításához a **set-AzVmssOsProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="bc333-164">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="bc333-165">-Túlszabályozás</span><span class="sxs-lookup"><span data-stu-id="bc333-165">-Overprovision</span></span>
<span data-ttu-id="bc333-166">Azt jelzi, hogy a parancsmag túla VMSS-e.</span><span class="sxs-lookup"><span data-stu-id="bc333-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="bc333-167">-PlanName</span><span class="sxs-lookup"><span data-stu-id="bc333-167">-PlanName</span></span>
<span data-ttu-id="bc333-168">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="bc333-169">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="bc333-169">-PlanProduct</span></span>
<span data-ttu-id="bc333-170">A csomag terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="bc333-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="bc333-171">-PlanPromotionCode</span></span>
<span data-ttu-id="bc333-172">A csomag-előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="bc333-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="bc333-173">-PlanPublisher</span></span>
<span data-ttu-id="bc333-174">A terv közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="bc333-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="bc333-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="bc333-176">Az egyes helyekhez tartozó hibák tartománya.</span><span class="sxs-lookup"><span data-stu-id="bc333-176">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="bc333-177">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="bc333-177">-Priority</span></span>
<span data-ttu-id="bc333-178">A beállított méretarányban a virtuális gépek prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="bc333-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="bc333-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="bc333-180">A folyamatos frissítés szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="bc333-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="bc333-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="bc333-182">Az egyetlen elhelyezés csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="bc333-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="bc333-183">-SkuCapacity</span></span>
<span data-ttu-id="bc333-184">A VMSS példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-184">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="bc333-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bc333-185">-SkuName</span></span>
<span data-ttu-id="bc333-186">A VMSS összes példányának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="bc333-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="bc333-187">-SkuTier</span></span>
<span data-ttu-id="bc333-188">A VMSS küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="bc333-189">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bc333-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc333-190">Standard</span><span class="sxs-lookup"><span data-stu-id="bc333-190">Standard</span></span>
- <span data-ttu-id="bc333-191">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="bc333-191">Basic</span></span>

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

### <span data-ttu-id="bc333-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="bc333-192">-StorageProfile</span></span>
<span data-ttu-id="bc333-193">A VMSS-konfigurációban a lemez tulajdonságait tartalmazó Storage profil objektum.</span><span class="sxs-lookup"><span data-stu-id="bc333-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="bc333-194">Az objektum beállításához a **set-AzVmssStorageProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="bc333-194">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="bc333-195">-Címke</span><span class="sxs-lookup"><span data-stu-id="bc333-195">-Tag</span></span>
<span data-ttu-id="bc333-196">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="bc333-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bc333-197">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="bc333-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bc333-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="bc333-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="bc333-199">A méretarányban a virtuális gépekre való frissítés módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="bc333-200">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="bc333-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc333-201">Automatikus</span><span class="sxs-lookup"><span data-stu-id="bc333-201">Automatic</span></span>
- <span data-ttu-id="bc333-202">Kézi</span><span class="sxs-lookup"><span data-stu-id="bc333-202">Manual</span></span>

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

### <span data-ttu-id="bc333-203">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="bc333-203">-Zone</span></span>
<span data-ttu-id="bc333-204">A virtuálisgép-készlethez tartozó zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc333-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="bc333-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="bc333-205">-ZoneBalance</span></span>
<span data-ttu-id="bc333-206">Annak megállapítása, hogy a virtuális gép csak a virtuális gépeken keresztül, több x-zónában van-e érvényben, ha van zóna</span><span class="sxs-lookup"><span data-stu-id="bc333-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="bc333-207">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bc333-207">-Confirm</span></span>
<span data-ttu-id="bc333-208">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc333-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc333-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc333-209">-WhatIf</span></span>
<span data-ttu-id="bc333-210">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bc333-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc333-211">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc333-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc333-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc333-212">CommonParameters</span></span>
<span data-ttu-id="bc333-213">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc333-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc333-214">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc333-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc333-215">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc333-215">INPUTS</span></span>

### <span data-ttu-id="bc333-216">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bc333-216">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bc333-217">System. String</span><span class="sxs-lookup"><span data-stu-id="bc333-217">System.String</span></span>

### <span data-ttu-id="bc333-218">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc333-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bc333-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bc333-219">System.Int32</span></span>

### <span data-ttu-id="bc333-220">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. UpgradeMode, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="bc333-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="bc333-221">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="bc333-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="bc333-222">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="bc333-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="bc333-223">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="bc333-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="bc333-224">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="bc333-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="bc333-225">System. string []</span><span class="sxs-lookup"><span data-stu-id="bc333-225">System.String[]</span></span>

### <span data-ttu-id="bc333-226">Microsoft. Azure. Management. kiszámítás. models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="bc333-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="bc333-227">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bc333-227">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bc333-228">Microsoft. Azure. Management. kiszámítás. models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bc333-228">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="bc333-229">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. ResourceIdentityType, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="bc333-229">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="bc333-230">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc333-230">OUTPUTS</span></span>

### <span data-ttu-id="bc333-231">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bc333-231">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bc333-232">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc333-232">NOTES</span></span>

## <span data-ttu-id="bc333-233">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc333-233">RELATED LINKS</span></span>

[<span data-ttu-id="bc333-234">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="bc333-234">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="bc333-235">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="bc333-235">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="bc333-236">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc333-236">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="bc333-237">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="bc333-237">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="bc333-238">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="bc333-238">New-AzVmss</span></span>](./New-AzVmss.md)

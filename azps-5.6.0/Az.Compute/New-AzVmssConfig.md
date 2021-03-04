---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: ba44e397aa09834b1371fa9188527a056153017c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937106"
---
# <span data-ttu-id="ef27f-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ef27f-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="ef27f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef27f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef27f-103">VMSS konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ef27f-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="ef27f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef27f-104">SYNTAX</span></span>

### <span data-ttu-id="ef27f-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef27f-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] [-EncryptionAtHost]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef27f-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef27f-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef27f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef27f-107">DESCRIPTION</span></span>
<span data-ttu-id="ef27f-108">A **New-AzVmssConfig** parancsmag létrehoz egy konfigurálható virtuálismenedzser-méretezési készletet (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ef27f-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="ef27f-109">A VMSS-objektum konfigurálásához további parancsmagok is szükségesek.</span><span class="sxs-lookup"><span data-stu-id="ef27f-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="ef27f-110">Ezek a parancsmagok az alábbi parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="ef27f-110">These cmdlets are:</span></span>
- <span data-ttu-id="ef27f-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ef27f-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="ef27f-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ef27f-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="ef27f-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef27f-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="ef27f-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ef27f-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="ef27f-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef27f-115">EXAMPLES</span></span>

### <span data-ttu-id="ef27f-116">1. példa: VMSS konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="ef27f-116">Example 1: Create a VMSS configuration object</span></span>
```powershell
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

<span data-ttu-id="ef27f-117">Ebben a példában egy VMSS konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ef27f-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="ef27f-118">Az első parancs a **New-AzVmssConfig** parancsmaggal hoz létre egy VMSS konfigurációs objektumot, és az eredményt a következő nevű változóban $VMSS.</span><span class="sxs-lookup"><span data-stu-id="ef27f-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="ef27f-119">A második parancs a **New-AzVmss** parancsmag segítségével létrehoz egy VMSS-t, amely az első parancsban létrehozott VMSS konfigurációs objektumot használja.</span><span class="sxs-lookup"><span data-stu-id="ef27f-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="ef27f-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="ef27f-120">Example 2</span></span>

<span data-ttu-id="ef27f-121">VMSS konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ef27f-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="ef27f-122">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="ef27f-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="ef27f-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef27f-123">PARAMETERS</span></span>

### <span data-ttu-id="ef27f-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="ef27f-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="ef27f-125">Az az idő, amelyre az automatikus javítást felfüggeszti a rendszer a VM-en egy állapotváltozás miatt.</span><span class="sxs-lookup"><span data-stu-id="ef27f-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="ef27f-126">A türelmi idő az állapotváltozás befejezése után kezdődik.</span><span class="sxs-lookup"><span data-stu-id="ef27f-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="ef27f-127">Ez segít elkerülni a véletlen vagy a véletlen javításokat.</span><span class="sxs-lookup"><span data-stu-id="ef27f-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="ef27f-128">Az időidőtartamot ISO 8601 formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="ef27f-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="ef27f-129">A minimális türelmi időszak 30 perc (PT30M), amely egyben az alapértelmezett érték is.</span><span class="sxs-lookup"><span data-stu-id="ef27f-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="ef27f-130">A maximális türelmi idő 90 perc (PT90M).</span><span class="sxs-lookup"><span data-stu-id="ef27f-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="ef27f-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ef27f-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="ef27f-132">Azt adja meg, hogy a rendszer automatikusan alkalmazza-e az operációs rendszer frissítését a méretarány-készlet példányainak gördülékenként való alkalmazására, amikor a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="ef27f-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="ef27f-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ef27f-133">-BootDiagnostic</span></span>
<span data-ttu-id="ef27f-134">A virtuális gép méretarányos halmazának indítási diagnosztikai profilját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef27f-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="ef27f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef27f-135">-DefaultProfile</span></span>
<span data-ttu-id="ef27f-136">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef27f-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef27f-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="ef27f-137">-DisableAutoRollback</span></span>
<span data-ttu-id="ef27f-138">Az automatikus visszaállítás letiltása az automatikus operációs rendszer frissítési házirendje esetén</span><span class="sxs-lookup"><span data-stu-id="ef27f-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="ef27f-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="ef27f-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="ef27f-140">Engedélyezi az automatikus javításokat a virtuális gép méretaránykészletében.</span><span class="sxs-lookup"><span data-stu-id="ef27f-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ef27f-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="ef27f-141">-EnableUltraSSD</span></span>
<span data-ttu-id="ef27f-142">Lehetővé teszi, hogy egy vagy több felügyelt adatlemezt UltraSSD_LRS tárolófióktípussal a virtuális gép méretaránykészletén.</span><span class="sxs-lookup"><span data-stu-id="ef27f-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="ef27f-143">A tárfiók-típussal rendelkező felügyelt UltraSSD_LRS a VMSS-hez csak akkor lehet hozzáadni, ha ez a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="ef27f-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="ef27f-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="ef27f-144">-EncryptionAtHost</span></span>
<span data-ttu-id="ef27f-145">Ez a paraméter engedélyezi a titkosítást az összes lemezen, beleértve magában az erőforrás-/ideiglenes lemezen is.</span><span class="sxs-lookup"><span data-stu-id="ef27f-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="ef27f-146">Alapértelmezett: A gazdaszámítógép titkosítása le lesz tiltva, hacsak ez a tulajdonság nincs igazra állítva az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="ef27f-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="ef27f-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="ef27f-147">-EvictionPolicy</span></span>
<span data-ttu-id="ef27f-148">A virtuális gépek kiviction házirendét adja meg a méretaránykészletben.</span><span class="sxs-lookup"><span data-stu-id="ef27f-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="ef27f-149">-Extension</span><span class="sxs-lookup"><span data-stu-id="ef27f-149">-Extension</span></span>
<span data-ttu-id="ef27f-150">A VMSS bővítményinformációs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef27f-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="ef27f-151">Ezt az objektumot az **Add-AzVmssExtension** parancsmag használatával használhatja.</span><span class="sxs-lookup"><span data-stu-id="ef27f-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="ef27f-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="ef27f-152">-HealthProbeId</span></span>
<span data-ttu-id="ef27f-153">A virtuális gép méretkészletében lévő példány állapotának meghatározásához használt terhelésegyenleg-terheléselosztási terhelésazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef27f-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="ef27f-154">A HealthProbeId a következő alakban áll: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/ezres/{name}'.</span><span class="sxs-lookup"><span data-stu-id="ef27f-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="ef27f-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="ef27f-155">-IdentityId</span></span>
<span data-ttu-id="ef27f-156">A virtuális gép méretkészletével társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef27f-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="ef27f-157">A felhasználói identitáshivatkozások ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="ef27f-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="ef27f-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ef27f-158">-IdentityType</span></span>
<span data-ttu-id="ef27f-159">A virtuális gép méretaránykészletében használt identitás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ef27f-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="ef27f-160">A "SystemAssignedUserAssigned" típus egy implicit módon létrehozott identitást és egy felhasználóhoz rendelt identitáskészletet is tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ef27f-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="ef27f-161">A "Nincs" típus eltávolítja az identitásokat a virtuális gép méretkészletből.</span><span class="sxs-lookup"><span data-stu-id="ef27f-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="ef27f-162">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="ef27f-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ef27f-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="ef27f-163">SystemAssigned</span></span>
- <span data-ttu-id="ef27f-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="ef27f-164">UserAssigned</span></span>
- <span data-ttu-id="ef27f-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="ef27f-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="ef27f-166">Nincs</span><span class="sxs-lookup"><span data-stu-id="ef27f-166">None</span></span>

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

### <span data-ttu-id="ef27f-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ef27f-167">-LicenseType</span></span>
<span data-ttu-id="ef27f-168">Adja meg a licenc típusát, amely a saját licenccel használható.</span><span class="sxs-lookup"><span data-stu-id="ef27f-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="ef27f-169">-Location</span><span class="sxs-lookup"><span data-stu-id="ef27f-169">-Location</span></span>
<span data-ttu-id="ef27f-170">Megadja azt az Azure-helyet, ahol a VMSS létrejön.</span><span class="sxs-lookup"><span data-stu-id="ef27f-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="ef27f-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="ef27f-171">-MaxPrice</span></span>
<span data-ttu-id="ef27f-172">Azt a maximális árat adja meg, amelyért fizet a spot VM/VMSS-ekért.</span><span class="sxs-lookup"><span data-stu-id="ef27f-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="ef27f-173">Ez az ár amerikai dollárban van meg.</span><span class="sxs-lookup"><span data-stu-id="ef27f-173">This price is in US Dollars.</span></span> <span data-ttu-id="ef27f-174">Ezt az árat összehasonlítjuk a virtuális gép méretének aktuális spotárával.</span><span class="sxs-lookup"><span data-stu-id="ef27f-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="ef27f-175">Ezenkívül az árakat a helyszíni VM/VMSS létrehozása/frissítése során hasonlítják össze, és a művelet csak akkor lesz sikeres, ha a maxPrice nagyobb, mint az aktuális azonnali ár.</span><span class="sxs-lookup"><span data-stu-id="ef27f-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="ef27f-176">A maxPrice akkor is használatos a helyszíni VM/VMSS kivoktatására, ha a jelenlegi spotár meghaladja a vm/VMSS létrehozását követően a maxPrice értéken.</span><span class="sxs-lookup"><span data-stu-id="ef27f-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="ef27f-177">A lehetséges értékek a nullánál nagyobb decimális értékek.</span><span class="sxs-lookup"><span data-stu-id="ef27f-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="ef27f-178">Példa: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="ef27f-178">Example: 0.01538.</span></span>  <span data-ttu-id="ef27f-179">-1 azt jelzi, hogy a helyszíni VM/VMSS ár okokból nem szükséges.</span><span class="sxs-lookup"><span data-stu-id="ef27f-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="ef27f-180">Az alapértelmezett maximális ár -1, ha nem Ön biztosítja.</span><span class="sxs-lookup"><span data-stu-id="ef27f-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="ef27f-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef27f-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="ef27f-182">Megadja azt a hálózati profilobjektumot, amely a VMSS-konfiguráció hálózati tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ef27f-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="ef27f-183">Az Objektum hozzáadásához használhatja az **Add-AzVmssNetworkInterfaceConfiguration** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ef27f-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="ef27f-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="ef27f-184">-OsProfile</span></span>
<span data-ttu-id="ef27f-185">Azt az operációsrendszer-profilobjektumot adja meg, amely a VMSS-konfigurációhoz az operációs rendszer tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ef27f-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="ef27f-186">Az objektum beállításához használhatja a **Set-AzVmssOsProfile** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ef27f-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="ef27f-187">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="ef27f-187">-Overprovision</span></span>
<span data-ttu-id="ef27f-188">Azt jelzi, hogy a parancsmag túlépíti-e a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="ef27f-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="ef27f-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="ef27f-189">-PlanName</span></span>
<span data-ttu-id="ef27f-190">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef27f-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="ef27f-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="ef27f-191">-PlanProduct</span></span>
<span data-ttu-id="ef27f-192">A csomag termékét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ef27f-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="ef27f-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="ef27f-193">-PlanPromotionCode</span></span>
<span data-ttu-id="ef27f-194">A csomag promóciós kódját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef27f-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="ef27f-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ef27f-195">-PlanPublisher</span></span>
<span data-ttu-id="ef27f-196">A terv közzétevője.</span><span class="sxs-lookup"><span data-stu-id="ef27f-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="ef27f-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="ef27f-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="ef27f-198">A hibatartományok száma az egyes elhelyezési csoportoknál.</span><span class="sxs-lookup"><span data-stu-id="ef27f-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="ef27f-199">-Priority</span><span class="sxs-lookup"><span data-stu-id="ef27f-199">-Priority</span></span>
<span data-ttu-id="ef27f-200">A virtuális machien prioritása a méretaránykészletben.</span><span class="sxs-lookup"><span data-stu-id="ef27f-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="ef27f-201">Csak a "Regular", a "Spot" és a "Low" támogatott értékeket támogatja.</span><span class="sxs-lookup"><span data-stu-id="ef27f-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="ef27f-202">A "Regular" normál virtuális géphez való.</span><span class="sxs-lookup"><span data-stu-id="ef27f-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="ef27f-203">A "Spot" a direkt virtuális gépekhez való.</span><span class="sxs-lookup"><span data-stu-id="ef27f-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="ef27f-204">A "Low" a direkt virtuális gépre is igaz, de a "Spot" (Direkt) szövegre cseréli.</span><span class="sxs-lookup"><span data-stu-id="ef27f-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="ef27f-205">A "Gyenge" helyett használja a "Spot" (Direkt) használhatja.</span><span class="sxs-lookup"><span data-stu-id="ef27f-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="ef27f-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="ef27f-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="ef27f-207">Az ezzel a méretkészlethez használható Közelség elhelyezési csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef27f-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="ef27f-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="ef27f-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="ef27f-209">Megadja a frissítési házirendet.</span><span class="sxs-lookup"><span data-stu-id="ef27f-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="ef27f-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="ef27f-210">-ScaleInPolicy</span></span>
<span data-ttu-id="ef27f-211">A virtuális gép méretarányának beállításakor be kell tartani a szabályokat.</span><span class="sxs-lookup"><span data-stu-id="ef27f-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="ef27f-212">Lehetséges értékek: "Alapértelmezett", "LegrégebbiVM" és "LegújabbVM".</span><span class="sxs-lookup"><span data-stu-id="ef27f-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="ef27f-213">Az "Alapértelmezett" érték a virtuális gép méretarány-készletének méretaránya esetén először a zónák között lesz kiegyensúlyozott, ha az egy állatövi méretarányú készlet.</span><span class="sxs-lookup"><span data-stu-id="ef27f-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="ef27f-214">Ezt követően lehetőség szerint kiegyensúlyozott lesz a hibatartományok között.</span><span class="sxs-lookup"><span data-stu-id="ef27f-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="ef27f-215">Az egyes hibatartományok esetén az eltávolításhoz kiválasztott virtuális gépek lesznek a legújabbak, amelyek nem védettek a méretaránytól.</span><span class="sxs-lookup"><span data-stu-id="ef27f-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="ef27f-216">A "OldestVM" (LegrégebbiVM) akkor lesz kiválasztva eltávolításra, ha egy virtuális gép méretaránykészletét méretarányosra méretezi.</span><span class="sxs-lookup"><span data-stu-id="ef27f-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="ef27f-217">Az állatövi virtuális gép méretaránykészletek esetében a méretaránykészlet először zónák között lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="ef27f-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="ef27f-218">Az egyes zónákban a nem védett legrégebbi virtuális gépek lesznek kiválasztva eltávolításra.</span><span class="sxs-lookup"><span data-stu-id="ef27f-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="ef27f-219">"LegújabbVM", amikor egy virtuális gép méretaránykészletét méretarányosra méretezik, a rendszer eltávolítja a méretaránytól nem védett legújabb virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="ef27f-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="ef27f-220">Az állatövi virtuális gép méretaránykészletek esetében a méretaránykészlet először zónák között lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="ef27f-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="ef27f-221">Az egyes zónákon belül a nem védett legújabb virtuális gépek lesznek kiválasztva eltávolításra.</span><span class="sxs-lookup"><span data-stu-id="ef27f-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="ef27f-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ef27f-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="ef27f-223">Az egyetlen elhelyezési csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef27f-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="ef27f-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="ef27f-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="ef27f-225">Azt adja meg, hogy a bővítmények nem futnak túlzsúfolt virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="ef27f-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="ef27f-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ef27f-226">-SkuCapacity</span></span>
<span data-ttu-id="ef27f-227">A VMSS-ban található példányok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef27f-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="ef27f-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ef27f-228">-SkuName</span></span>
<span data-ttu-id="ef27f-229">A VMSS összes példányának mérete.</span><span class="sxs-lookup"><span data-stu-id="ef27f-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="ef27f-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ef27f-230">-SkuTier</span></span>
<span data-ttu-id="ef27f-231">A VMSS-hez megadott szint.</span><span class="sxs-lookup"><span data-stu-id="ef27f-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="ef27f-232">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="ef27f-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ef27f-233">Normál</span><span class="sxs-lookup"><span data-stu-id="ef27f-233">Standard</span></span>
- <span data-ttu-id="ef27f-234">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="ef27f-234">Basic</span></span>

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

### <span data-ttu-id="ef27f-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="ef27f-235">-StorageProfile</span></span>
<span data-ttu-id="ef27f-236">A VMSS-konfiguráció lemeztulajdonságokat tartalmazó tárolóprofil-objektuma.</span><span class="sxs-lookup"><span data-stu-id="ef27f-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="ef27f-237">Az objektum beállításához használhatja a **Set-AzVmssStorageProfile** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ef27f-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="ef27f-238">-Tag</span><span class="sxs-lookup"><span data-stu-id="ef27f-238">-Tag</span></span>
<span data-ttu-id="ef27f-239">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="ef27f-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ef27f-240">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="ef27f-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ef27f-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ef27f-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="ef27f-242">A virtuális gép által törölt virtuális gépnek a konfigurálható időtartamnak (percben) jóvá kell hagynia az ütemezett esemény megszüntetését, mielőtt az esemény automatikusan jóváhagyásra kerül (időkorra).</span><span class="sxs-lookup"><span data-stu-id="ef27f-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="ef27f-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="ef27f-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="ef27f-244">Az Ütemezett események megszüntetésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="ef27f-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="ef27f-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="ef27f-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="ef27f-246">A virtuális gépekre való frissítés módját adja meg a méretaránykészletben.</span><span class="sxs-lookup"><span data-stu-id="ef27f-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="ef27f-247">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="ef27f-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ef27f-248">Automatikus</span><span class="sxs-lookup"><span data-stu-id="ef27f-248">Automatic</span></span>
- <span data-ttu-id="ef27f-249">Kézi</span><span class="sxs-lookup"><span data-stu-id="ef27f-249">Manual</span></span>

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

### <span data-ttu-id="ef27f-250">-Zone</span><span class="sxs-lookup"><span data-stu-id="ef27f-250">-Zone</span></span>
<span data-ttu-id="ef27f-251">A virtuális gép méretaránykészletének zónalistát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef27f-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ef27f-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="ef27f-252">-ZoneBalance</span></span>
<span data-ttu-id="ef27f-253">Legyen-e szükség arra, hogy a virtuális gép eloszlása szigorúan x-zónákon belül legyen-e, ha zónakimaradás állna elő.</span><span class="sxs-lookup"><span data-stu-id="ef27f-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="ef27f-254">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef27f-254">-Confirm</span></span>
<span data-ttu-id="ef27f-255">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ef27f-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef27f-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef27f-256">-WhatIf</span></span>
<span data-ttu-id="ef27f-257">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ef27f-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef27f-258">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef27f-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef27f-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef27f-259">CommonParameters</span></span>
<span data-ttu-id="ef27f-260">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef27f-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef27f-261">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef27f-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef27f-262">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef27f-262">INPUTS</span></span>

### <span data-ttu-id="ef27f-263">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ef27f-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ef27f-264">System.String</span><span class="sxs-lookup"><span data-stu-id="ef27f-264">System.String</span></span>

### <span data-ttu-id="ef27f-265">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ef27f-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ef27f-266">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ef27f-266">System.Int32</span></span>

### <span data-ttu-id="ef27f-267">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ef27f-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ef27f-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="ef27f-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="ef27f-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ef27f-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="ef27f-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="ef27f-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="ef27f-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span><span class="sxs-lookup"><span data-stu-id="ef27f-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="ef27f-272">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ef27f-272">System.String[]</span></span>

### <span data-ttu-id="ef27f-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="ef27f-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="ef27f-274">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ef27f-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ef27f-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ef27f-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="ef27f-276">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ef27f-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ef27f-277">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef27f-277">OUTPUTS</span></span>

### <span data-ttu-id="ef27f-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ef27f-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ef27f-279">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef27f-279">NOTES</span></span>

## <span data-ttu-id="ef27f-280">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef27f-280">RELATED LINKS</span></span>

[<span data-ttu-id="ef27f-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ef27f-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="ef27f-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ef27f-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="ef27f-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef27f-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="ef27f-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ef27f-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="ef27f-285">Új-AzVms</span><span class="sxs-lookup"><span data-stu-id="ef27f-285">New-AzVmss</span></span>](./New-AzVmss.md)

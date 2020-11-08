---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024827"
---
# <span data-ttu-id="5bda2-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5bda2-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="5bda2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5bda2-102">SYNOPSIS</span></span>
<span data-ttu-id="5bda2-103">Létrehozza a VMSS konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="5bda2-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="5bda2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5bda2-104">SYNTAX</span></span>

### <span data-ttu-id="5bda2-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5bda2-105">DefaultParameterSet (Default)</span></span>
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

### <span data-ttu-id="5bda2-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bda2-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="5bda2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5bda2-107">DESCRIPTION</span></span>
<span data-ttu-id="5bda2-108">A **New-AzVmssConfig** parancsmag létrehoz egy konfigurálható helyi Virtual Manager Scale set (VMSS) objektumot.</span><span class="sxs-lookup"><span data-stu-id="5bda2-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="5bda2-109">A VMSS objektum konfigurálásához további parancsmagokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="5bda2-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="5bda2-110">Ezek a parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="5bda2-110">These cmdlets are:</span></span>
- <span data-ttu-id="5bda2-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="5bda2-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="5bda2-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5bda2-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="5bda2-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5bda2-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="5bda2-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5bda2-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="5bda2-115">Példák</span><span class="sxs-lookup"><span data-stu-id="5bda2-115">EXAMPLES</span></span>

### <span data-ttu-id="5bda2-116">Példa 1: VMSS konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="5bda2-116">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="5bda2-117">Ebben a példában egy VMSS-konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5bda2-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="5bda2-118">Az első parancs a **New-AzVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5bda2-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="5bda2-119">A második parancs a **New-AzVmss** parancsmagot használja az első parancsban létrehozott VMSS konfigurációs OBJEKTUMOT használó VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="5bda2-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="5bda2-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="5bda2-120">Example 2</span></span>

<span data-ttu-id="5bda2-121">Létrehozza a VMSS konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="5bda2-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="5bda2-122">autogenerated</span><span class="sxs-lookup"><span data-stu-id="5bda2-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="5bda2-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5bda2-123">PARAMETERS</span></span>

### <span data-ttu-id="5bda2-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="5bda2-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="5bda2-125">Az az idő, ameddig a VM-ben bekövetkezett változások miatt az automatikus javítás fel van függesztve.</span><span class="sxs-lookup"><span data-stu-id="5bda2-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="5bda2-126">A türelmi idő az állam módosításának befejeződése után kezdődik.</span><span class="sxs-lookup"><span data-stu-id="5bda2-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="5bda2-127">Ez segít elkerülni a korai vagy véletlenszerű javításokat.</span><span class="sxs-lookup"><span data-stu-id="5bda2-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="5bda2-128">Az időtartamot az ISO 8601-formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="5bda2-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="5bda2-129">A minimális megengedett türelmi időszak 30 perc (PT30M), amely egyben az alapértelmezett érték is.</span><span class="sxs-lookup"><span data-stu-id="5bda2-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="5bda2-130">A megengedett maximális türelmi időszak 90 perc (PT90M).</span><span class="sxs-lookup"><span data-stu-id="5bda2-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="5bda2-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="5bda2-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="5bda2-132">Azt adja meg, hogy az operációs rendszer frissítéseit a program automatikusan alkalmazza-e a méretarányos példányokra, ha a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="5bda2-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="5bda2-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5bda2-133">-BootDiagnostic</span></span>
<span data-ttu-id="5bda2-134">A virtuálisgép-készlet indítási diagnosztikai profilját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="5bda2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bda2-135">-DefaultProfile</span></span>
<span data-ttu-id="5bda2-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bda2-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bda2-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="5bda2-137">-DisableAutoRollback</span></span>
<span data-ttu-id="5bda2-138">Automatikus visszagörgetés letiltása az automatikus operációs rendszer frissítési házirendjében</span><span class="sxs-lookup"><span data-stu-id="5bda2-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="5bda2-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="5bda2-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="5bda2-140">Engedélyezi az automatikus javítást a virtuálisgép-méretarány beállításakor.</span><span class="sxs-lookup"><span data-stu-id="5bda2-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="5bda2-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="5bda2-141">-EnableUltraSSD</span></span>
<span data-ttu-id="5bda2-142">Lehetővé teszi, hogy egy vagy több felügyelt adatlemez legyen a virtuálisgép-készlet UltraSSD_LRS tárterület-fiók típusával.</span><span class="sxs-lookup"><span data-stu-id="5bda2-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="5bda2-143">A felügyelt lemezek tároló típusú UltraSSD_LRS csak akkor vehetők fel a VMSS, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="5bda2-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="5bda2-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="5bda2-144">-EncryptionAtHost</span></span>
<span data-ttu-id="5bda2-145">Ez a paraméter lehetővé teszi az összes lemez titkosítását, például az erőforrás/Temp diskt az állomáson.</span><span class="sxs-lookup"><span data-stu-id="5bda2-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="5bda2-146">Alapértelmezés: az állomáson a titkosítás le lesz tiltva, kivéve ha a tulajdonság értéke igaz az erőforrás esetében.</span><span class="sxs-lookup"><span data-stu-id="5bda2-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="5bda2-147">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="5bda2-147">-EvictionPolicy</span></span>
<span data-ttu-id="5bda2-148">A méretarányban a virtuális gépek kilakoltatási szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="5bda2-149">-Extension (kiterjesztés)</span><span class="sxs-lookup"><span data-stu-id="5bda2-149">-Extension</span></span>
<span data-ttu-id="5bda2-150">A VMSS kiegészítő információs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="5bda2-151">Ezt az objektumot az **Add-AzVmssExtension** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="5bda2-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="5bda2-152">-HealthProbeId</span></span>
<span data-ttu-id="5bda2-153">A virtuálisgép-készletben lévő példány állapotának meghatározásához használt terheléselosztó szonda AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="5bda2-154">A HealthProbeId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}" formában jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="5bda2-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="5bda2-155">-IdentityId</span></span>
<span data-ttu-id="5bda2-156">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="5bda2-157">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="5bda2-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="5bda2-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5bda2-158">-IdentityType</span></span>
<span data-ttu-id="5bda2-159">A virtuálisgép-készlethez használt identitás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="5bda2-160">Az "SystemAssignedUserAssigned" típus egy implicit módon létrehozott identitást és egy, a felhasználó által kiosztott identitást tartalmazó készletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="5bda2-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="5bda2-161">Ha a virtuálisgép-készletből eltávolítja az identitásokat, a "nincs" típust kell választania.</span><span class="sxs-lookup"><span data-stu-id="5bda2-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="5bda2-162">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5bda2-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5bda2-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="5bda2-163">SystemAssigned</span></span>
- <span data-ttu-id="5bda2-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="5bda2-164">UserAssigned</span></span>
- <span data-ttu-id="5bda2-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="5bda2-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="5bda2-166">Nincs</span><span class="sxs-lookup"><span data-stu-id="5bda2-166">None</span></span>

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

### <span data-ttu-id="5bda2-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5bda2-167">-LicenseType</span></span>
<span data-ttu-id="5bda2-168">Adja meg azt a licenc-típust, amely a licencek használati forgatókönyvét hozza meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="5bda2-169">-Hely</span><span class="sxs-lookup"><span data-stu-id="5bda2-169">-Location</span></span>
<span data-ttu-id="5bda2-170">Az az Azure-hely, ahol létrejön a VMSS.</span><span class="sxs-lookup"><span data-stu-id="5bda2-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="5bda2-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="5bda2-171">-MaxPrice</span></span>
<span data-ttu-id="5bda2-172">Itt adhatja meg, hogy a helyszíni VM/VMSS milyen maximális árat fizessen.</span><span class="sxs-lookup"><span data-stu-id="5bda2-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="5bda2-173">Ez az ár amerikai dollárban van.</span><span class="sxs-lookup"><span data-stu-id="5bda2-173">This price is in US Dollars.</span></span> <span data-ttu-id="5bda2-174">Ezt az árat a program összehasonlítja a VM-méret aktuális áraival.</span><span class="sxs-lookup"><span data-stu-id="5bda2-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="5bda2-175">A helyszíni VM/VMSS létrehozásának/frissítésének időpontjában az árak is összehasonlíthatók lesznek, és a művelet csak akkor fog sikerülni, ha a maxPrice nagyobb, mint a jelenlegi ár.</span><span class="sxs-lookup"><span data-stu-id="5bda2-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="5bda2-176">A maxPrice a VM/VMSS létrehozása után is használni fogja a helyszíni VM/VMSS, ha a jelenlegi ár túllépi a maxPrice.</span><span class="sxs-lookup"><span data-stu-id="5bda2-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="5bda2-177">Lehetséges értékek: bármely nullánál nagyobb decimális érték.</span><span class="sxs-lookup"><span data-stu-id="5bda2-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="5bda2-178">Példa: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="5bda2-178">Example: 0.01538.</span></span>  <span data-ttu-id="5bda2-179">-1 – azt jelzi, hogy a hely VM/VMSS nem szabad az árak miatt kizárni.</span><span class="sxs-lookup"><span data-stu-id="5bda2-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="5bda2-180">Az alapértelmezett Max ár is-1, ha az nem az Ön által megadott.</span><span class="sxs-lookup"><span data-stu-id="5bda2-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="5bda2-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5bda2-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="5bda2-182">Megadja a VMSS konfigurációjának hálózati tulajdonságait tartalmazó hálózati profil objektumot.</span><span class="sxs-lookup"><span data-stu-id="5bda2-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="5bda2-183">Ezt az objektumot az **Add-AzVmssNetworkInterfaceConfiguration** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="5bda2-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="5bda2-184">-OsProfile</span></span>
<span data-ttu-id="5bda2-185">Annak az operációs rendszernek a profil-objektumát adja meg, amely az VMSS-konfiguráció operációs rendszerének tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5bda2-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="5bda2-186">Az objektum beállításához a **set-AzVmssOsProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="5bda2-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="5bda2-187">-Túlszabályozás</span><span class="sxs-lookup"><span data-stu-id="5bda2-187">-Overprovision</span></span>
<span data-ttu-id="5bda2-188">Azt jelzi, hogy a parancsmag túla VMSS-e.</span><span class="sxs-lookup"><span data-stu-id="5bda2-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="5bda2-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="5bda2-189">-PlanName</span></span>
<span data-ttu-id="5bda2-190">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="5bda2-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="5bda2-191">-PlanProduct</span></span>
<span data-ttu-id="5bda2-192">A csomag terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="5bda2-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="5bda2-193">-PlanPromotionCode</span></span>
<span data-ttu-id="5bda2-194">A csomag-előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="5bda2-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="5bda2-195">-PlanPublisher</span></span>
<span data-ttu-id="5bda2-196">A terv közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="5bda2-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="5bda2-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="5bda2-198">Az egyes helyekhez tartozó hibák tartománya.</span><span class="sxs-lookup"><span data-stu-id="5bda2-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="5bda2-199">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="5bda2-199">-Priority</span></span>
<span data-ttu-id="5bda2-200">A méretarányban a virtuális machien prioritása.</span><span class="sxs-lookup"><span data-stu-id="5bda2-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="5bda2-201">Csak a támogatott értékek "normál", "spot" és "Low".</span><span class="sxs-lookup"><span data-stu-id="5bda2-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="5bda2-202">"Normál": a normál virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="5bda2-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="5bda2-203">A "spot" a direkt virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="5bda2-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="5bda2-204">Az "alacsony" a direkt virtuális gép is, de a helyére "spot" lép.</span><span class="sxs-lookup"><span data-stu-id="5bda2-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="5bda2-205">Kérjük, hogy az "alacsony" helyett a "spot" értéket használja.</span><span class="sxs-lookup"><span data-stu-id="5bda2-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="5bda2-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="5bda2-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="5bda2-207">Annak a közelségi helynek az erőforrás azonosítója, amellyel az adott méretarányt használni szeretné.</span><span class="sxs-lookup"><span data-stu-id="5bda2-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="5bda2-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="5bda2-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="5bda2-209">A folyamatos frissítés szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="5bda2-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="5bda2-210">-ScaleInPolicy</span></span>
<span data-ttu-id="5bda2-211">A virtuális gép méretarányának beállításakor követendő szabályok.</span><span class="sxs-lookup"><span data-stu-id="5bda2-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="5bda2-212">A lehetséges értékek a következők: "alapértelmezett", "OldestVM" és "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="5bda2-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="5bda2-213">"Alapértelmezett": Ha egy virtuális gép méretarányát a program átméretezi, a program először a méretarányokat fogja kiegyensúlyozni a zónáknál, ha a zóna zóna.</span><span class="sxs-lookup"><span data-stu-id="5bda2-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="5bda2-214">Ezt követően a lehető legtöbbet fogja kiegyensúlyozni a hibák tartományában.</span><span class="sxs-lookup"><span data-stu-id="5bda2-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="5bda2-215">Az egyes hibák tartománya alatt az eltávolításra kiválasztott virtuális gépek a legújabbak lesznek, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="5bda2-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="5bda2-216">"OldestVM": Ha egy virtuálisgép-készletet méretarányos, a program a legrégebbi virtuális gépeket választja, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="5bda2-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="5bda2-217">A virtuális gép méretarányos készletei esetében a méretarány először a zónáknál lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="5bda2-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="5bda2-218">Az egyes zónákon belül a legrégebbi virtuális gépeket választják ki a program az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="5bda2-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="5bda2-219">"NewestVM": Ha egy virtuálisgép-készletet méretezéssel végeznek, a program az eltávolításhoz a legújabb virtuális gépeket választja, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="5bda2-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="5bda2-220">A virtuális gép méretarányos készletei esetében a méretarány először a zónáknál lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="5bda2-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="5bda2-221">Az egyes zónákon belül a legújabb virtuális gépek, amelyek nem védettek, kiválasztásra kerülnek az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="5bda2-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="5bda2-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5bda2-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="5bda2-223">Az egyetlen elhelyezés csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="5bda2-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="5bda2-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="5bda2-225">Azt adja meg, hogy a bővítmények nem futnak az extra túlépített VMs-eszközön.</span><span class="sxs-lookup"><span data-stu-id="5bda2-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="5bda2-226">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="5bda2-226">-SkuCapacity</span></span>
<span data-ttu-id="5bda2-227">A VMSS példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="5bda2-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5bda2-228">-SkuName</span></span>
<span data-ttu-id="5bda2-229">A VMSS összes példányának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="5bda2-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5bda2-230">-SkuTier</span></span>
<span data-ttu-id="5bda2-231">A VMSS küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="5bda2-232">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5bda2-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5bda2-233">Standard</span><span class="sxs-lookup"><span data-stu-id="5bda2-233">Standard</span></span>
- <span data-ttu-id="5bda2-234">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="5bda2-234">Basic</span></span>

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

### <span data-ttu-id="5bda2-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="5bda2-235">-StorageProfile</span></span>
<span data-ttu-id="5bda2-236">A VMSS-konfigurációban a lemez tulajdonságait tartalmazó Storage profil objektum.</span><span class="sxs-lookup"><span data-stu-id="5bda2-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="5bda2-237">Az objektum beállításához a **set-AzVmssStorageProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="5bda2-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="5bda2-238">-Címke</span><span class="sxs-lookup"><span data-stu-id="5bda2-238">-Tag</span></span>
<span data-ttu-id="5bda2-239">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="5bda2-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5bda2-240">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="5bda2-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5bda2-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="5bda2-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="5bda2-242">Konfigurálható időtartam (percben) a törölt virtuális gépet az esemény automatikus jóváhagyása előtt jóvá kell hagynia a befejezési ütemezett esemény előtt (időtúllépés esetén).</span><span class="sxs-lookup"><span data-stu-id="5bda2-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="5bda2-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="5bda2-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="5bda2-244">Az ütemezett események befejezésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="5bda2-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="5bda2-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="5bda2-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="5bda2-246">A méretarányban a virtuális gépekre való frissítés módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="5bda2-247">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5bda2-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5bda2-248">Automatikus</span><span class="sxs-lookup"><span data-stu-id="5bda2-248">Automatic</span></span>
- <span data-ttu-id="5bda2-249">Kézi</span><span class="sxs-lookup"><span data-stu-id="5bda2-249">Manual</span></span>

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

### <span data-ttu-id="5bda2-250">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="5bda2-250">-Zone</span></span>
<span data-ttu-id="5bda2-251">A virtuálisgép-készlethez tartozó zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5bda2-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="5bda2-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="5bda2-252">-ZoneBalance</span></span>
<span data-ttu-id="5bda2-253">Annak megállapítása, hogy a virtuális gép csak a virtuális gépeken keresztül, több x-zónában van-e érvényben, ha van zóna</span><span class="sxs-lookup"><span data-stu-id="5bda2-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="5bda2-254">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5bda2-254">-Confirm</span></span>
<span data-ttu-id="5bda2-255">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bda2-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bda2-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bda2-256">-WhatIf</span></span>
<span data-ttu-id="5bda2-257">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5bda2-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bda2-258">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5bda2-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bda2-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bda2-259">CommonParameters</span></span>
<span data-ttu-id="5bda2-260">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5bda2-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bda2-261">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5bda2-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bda2-262">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bda2-262">INPUTS</span></span>

### <span data-ttu-id="5bda2-263">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5bda2-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5bda2-264">System. String</span><span class="sxs-lookup"><span data-stu-id="5bda2-264">System.String</span></span>

### <span data-ttu-id="5bda2-265">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5bda2-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5bda2-266">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5bda2-266">System.Int32</span></span>

### <span data-ttu-id="5bda2-267">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. UpgradeMode, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5bda2-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5bda2-268">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="5bda2-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="5bda2-269">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5bda2-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="5bda2-270">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="5bda2-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="5bda2-271">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="5bda2-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="5bda2-272">System. string []</span><span class="sxs-lookup"><span data-stu-id="5bda2-272">System.String[]</span></span>

### <span data-ttu-id="5bda2-273">Microsoft. Azure. Management. kiszámítás. models. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="5bda2-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="5bda2-274">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5bda2-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5bda2-275">Microsoft. Azure. Management. kiszámítás. models. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5bda2-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="5bda2-276">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. ResourceIdentityType, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5bda2-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="5bda2-277">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bda2-277">OUTPUTS</span></span>

### <span data-ttu-id="5bda2-278">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5bda2-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5bda2-279">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5bda2-279">NOTES</span></span>

## <span data-ttu-id="5bda2-280">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bda2-280">RELATED LINKS</span></span>

[<span data-ttu-id="5bda2-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="5bda2-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="5bda2-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5bda2-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="5bda2-283">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5bda2-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="5bda2-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5bda2-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="5bda2-285">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="5bda2-285">New-AzVmss</span></span>](./New-AzVmss.md)

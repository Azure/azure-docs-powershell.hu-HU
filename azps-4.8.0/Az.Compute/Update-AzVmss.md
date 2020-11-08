---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183067"
---
# <span data-ttu-id="4fadb-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4fadb-101">Update-AzVmss</span></span>

## <span data-ttu-id="4fadb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fadb-102">SYNOPSIS</span></span>
<span data-ttu-id="4fadb-103">Frissíti egy VMSS állapotát.</span><span class="sxs-lookup"><span data-stu-id="4fadb-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="4fadb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fadb-104">SYNTAX</span></span>

### <span data-ttu-id="4fadb-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4fadb-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fadb-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fadb-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fadb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fadb-107">DESCRIPTION</span></span>
<span data-ttu-id="4fadb-108">Az **Update-AzVmss** parancsmag a virtuálisgép-készlet (VMSS) állapotát egy helyi VMSS objektum állapotára frissíti.</span><span class="sxs-lookup"><span data-stu-id="4fadb-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="4fadb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4fadb-109">EXAMPLES</span></span>

### <span data-ttu-id="4fadb-110">Példa 1: egy VMSS állapotának frissítése egy helyi VMSS-objektum állapotával.</span><span class="sxs-lookup"><span data-stu-id="4fadb-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="4fadb-111">Ez a parancs frissíti a Group001 nevű VMSS001 nevű VMSS állapotát egy helyi VMSS objektum állapotához, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="4fadb-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="4fadb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fadb-112">PARAMETERS</span></span>

### <span data-ttu-id="4fadb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fadb-113">-AsJob</span></span>
<span data-ttu-id="4fadb-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="4fadb-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4fadb-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="4fadb-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="4fadb-116">Azt adja meg, hogy az operációs rendszer frissítéseit a program automatikusan alkalmazza-e a méretarányos példányokra, ha a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="4fadb-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="4fadb-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="4fadb-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="4fadb-118">Az az idő, ameddig a VM-ben bekövetkezett változások miatt az automatikus javítás fel van függesztve.</span><span class="sxs-lookup"><span data-stu-id="4fadb-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="4fadb-119">A türelmi idő az állam módosításának befejeződése után kezdődik.</span><span class="sxs-lookup"><span data-stu-id="4fadb-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="4fadb-120">Ez segít elkerülni a korai vagy véletlenszerű javításokat.</span><span class="sxs-lookup"><span data-stu-id="4fadb-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="4fadb-121">Az időtartamot az ISO 8601-formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="4fadb-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="4fadb-122">A minimális megengedett türelmi időszak 30 perc (PT30M), amely egyben az alapértelmezett érték is.</span><span class="sxs-lookup"><span data-stu-id="4fadb-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="4fadb-123">A megengedett maximális türelmi időszak 90 perc (PT90M).</span><span class="sxs-lookup"><span data-stu-id="4fadb-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="4fadb-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="4fadb-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="4fadb-125">A rendszerindítási diagnosztikát engedélyezni kell-e a virtuálisgép-méretarány beállításakor.</span><span class="sxs-lookup"><span data-stu-id="4fadb-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="4fadb-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="4fadb-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="4fadb-127">A konzol kimenetének és képernyőképének elhelyezéséhez használandó tárolási fiók URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4fadb-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="4fadb-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="4fadb-128">-CustomData</span></span>
<span data-ttu-id="4fadb-129">Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="4fadb-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="4fadb-130">Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.</span><span class="sxs-lookup"><span data-stu-id="4fadb-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="4fadb-131">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="4fadb-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="4fadb-132">Ha a VM rendszerhez a Cloud-init-ot szeretné használni, akkor olvassa el a következő témakört: a [Felhőbeli init használata a Linux VM testreszabására](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="4fadb-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="4fadb-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fadb-133">-DefaultProfile</span></span>
<span data-ttu-id="4fadb-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fadb-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fadb-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="4fadb-135">-DisableAutoRollback</span></span>
<span data-ttu-id="4fadb-136">Automatikus visszagörgetés letiltása az automatikus operációs rendszer frissítési házirendjében</span><span class="sxs-lookup"><span data-stu-id="4fadb-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="4fadb-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="4fadb-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="4fadb-138">Jelzi, hogy ez a parancsmag letiltja a Linux operációs rendszerhez használt jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="4fadb-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="4fadb-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="4fadb-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="4fadb-140">Engedélyezze vagy tiltsa le az automatikus javítást a virtuálisgép-készlet beállítása lapon.</span><span class="sxs-lookup"><span data-stu-id="4fadb-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="4fadb-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="4fadb-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="4fadb-142">Azt jelzi, hogy a VMSS engedélyezve vannak-e a Windows virtuális gépek az automatikus frissítésekhez.</span><span class="sxs-lookup"><span data-stu-id="4fadb-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="4fadb-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="4fadb-143">-EncryptionAtHost</span></span>
<span data-ttu-id="4fadb-144">Ezt a paramétert a felhasználó a virtuálisgép-készlet titkosításának engedélyezéséhez vagy letiltásához használhatja.</span><span class="sxs-lookup"><span data-stu-id="4fadb-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

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

### <span data-ttu-id="4fadb-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="4fadb-145">-IdentityId</span></span>
<span data-ttu-id="4fadb-146">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="4fadb-147">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="4fadb-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4fadb-148">-IdentityType</span></span>
<span data-ttu-id="4fadb-149">A virtuálisgép-készlethez használt identitás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="4fadb-150">Az "SystemAssignedUserAssigned" típus egy implicit módon létrehozott identitást és egy, a felhasználó által kiosztott identitást tartalmazó készletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="4fadb-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="4fadb-151">Ha a virtuálisgép-készletből eltávolítja az identitásokat, a "nincs" típust kell választania.</span><span class="sxs-lookup"><span data-stu-id="4fadb-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="4fadb-152">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4fadb-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4fadb-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="4fadb-153">SystemAssigned</span></span>
- <span data-ttu-id="4fadb-154">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="4fadb-154">UserAssigned</span></span>
- <span data-ttu-id="4fadb-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="4fadb-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="4fadb-156">Nincs</span><span class="sxs-lookup"><span data-stu-id="4fadb-156">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="4fadb-157">-ImageReferenceId</span></span>
<span data-ttu-id="4fadb-158">A kép hivatkozási AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="4fadb-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="4fadb-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="4fadb-160">A Virtual Machine Image (VMImage) ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="4fadb-161">Képajánlat beolvasásához használja az Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4fadb-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="4fadb-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="4fadb-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="4fadb-163">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="4fadb-164">Publisher beolvasásához használja az Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4fadb-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="4fadb-165">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="4fadb-165">-ImageReferenceSku</span></span>
<span data-ttu-id="4fadb-166">A VMImage SKU-ot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="4fadb-167">A SKU beolvasásához használja az Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4fadb-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="4fadb-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="4fadb-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="4fadb-169">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="4fadb-170">A legújabb verzió használatához adjon meg egy új értéket az adott verzió helyett.</span><span class="sxs-lookup"><span data-stu-id="4fadb-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="4fadb-171">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="4fadb-171">-ImageUri</span></span>
<span data-ttu-id="4fadb-172">A felhasználói kép blob-URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="4fadb-173">A VMSS létrehozza az operációs rendszer lemezét a felhasználói kép ugyanazon tárolójában.</span><span class="sxs-lookup"><span data-stu-id="4fadb-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="4fadb-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4fadb-174">-LicenseType</span></span>
<span data-ttu-id="4fadb-175">Adja meg azt a licenc-típust, amely a licencek használati forgatókönyvét hozza meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="4fadb-176">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4fadb-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="4fadb-177">A felügyelt lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="4fadb-178">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4fadb-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4fadb-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="4fadb-179">StandardLRS</span></span>
- <span data-ttu-id="4fadb-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="4fadb-180">PremiumLRS</span></span>

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

### <span data-ttu-id="4fadb-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="4fadb-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="4fadb-182">Annak a virtuális gép-példányoknak a maximális százalékos aránya, amelyet a rendszer egy kötegben a folyamatos frissítéssel egyidejűleg frissít.</span><span class="sxs-lookup"><span data-stu-id="4fadb-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="4fadb-183">Mivel az előző vagy a jövőbeli kötegekben ez a maximális, egészségtelen előfordulás, a kötegben lévő példányok százalékos arányát a nagyobb megbízhatóság érdekében is csökkentheti.</span><span class="sxs-lookup"><span data-stu-id="4fadb-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="4fadb-184">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="4fadb-184">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="4fadb-185">-MaxPrice</span></span>
<span data-ttu-id="4fadb-186">Itt adhatja meg, hogy az alacsony prioritású VM/VMSS milyen maximális árat fizessen.</span><span class="sxs-lookup"><span data-stu-id="4fadb-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="4fadb-187">Ez az ár amerikai dollárban van.</span><span class="sxs-lookup"><span data-stu-id="4fadb-187">This price is in US Dollars.</span></span> <span data-ttu-id="4fadb-188">Ezt az árat a program összehasonlítja a VM-méret jelenlegi alacsony prioritási árával.</span><span class="sxs-lookup"><span data-stu-id="4fadb-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="4fadb-189">Az árakat az alacsony prioritású VM/VMSS létrehozásának/frissítésének időpontjában is összehasonlították, és a művelet csak akkor fog sikerülni, ha a maxPrice nagyobb, mint a jelenlegi alacsony prioritású ár.</span><span class="sxs-lookup"><span data-stu-id="4fadb-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="4fadb-190">A maxPrice a VM/VMSS létrehozása után is az alacsony prioritású VM/VMSS eltávolítására használható, ha a jelenlegi alacsony prioritású ár túllépi a maxPrice.</span><span class="sxs-lookup"><span data-stu-id="4fadb-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="4fadb-191">Lehetséges értékek: bármely nullánál nagyobb decimális érték.</span><span class="sxs-lookup"><span data-stu-id="4fadb-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="4fadb-192">Példa: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="4fadb-192">Example: 0.01538.</span></span>  <span data-ttu-id="4fadb-193">-1 – azt jelzi, hogy az alacsony prioritású VM/VMSS nem szabad az árak miatt kizárni.</span><span class="sxs-lookup"><span data-stu-id="4fadb-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="4fadb-194">Az alapértelmezett Max ár is-1, ha az nem az Ön által megadott.</span><span class="sxs-lookup"><span data-stu-id="4fadb-194">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="4fadb-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="4fadb-196">A teljes virtuálisgép-példányok maximális százalékos aránya a készletben, amely egyidejű egészségtelen lehet, akár a frissítés során, akár a virtuálisgép-állapot ellenőrzésekor, a frissítés megszakítása előtt.</span><span class="sxs-lookup"><span data-stu-id="4fadb-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="4fadb-197">Ezt a korlátozást a program minden köteg kezdése előtt ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="4fadb-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="4fadb-198">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="4fadb-198">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="4fadb-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="4fadb-200">A frissített virtuálisgép-példányok maximális százaléka, amely egészségtelen állapotban található.</span><span class="sxs-lookup"><span data-stu-id="4fadb-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="4fadb-201">Ez az ellenőrzés minden köteg frissítésekor megtörténik.</span><span class="sxs-lookup"><span data-stu-id="4fadb-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="4fadb-202">Ha a százalékos érték túllépve, a gördülési frissítés leáll.</span><span class="sxs-lookup"><span data-stu-id="4fadb-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="4fadb-203">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="4fadb-203">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-204">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="4fadb-204">-OsDiskCaching</span></span>
<span data-ttu-id="4fadb-205">Az operációs rendszer lemezének gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="4fadb-206">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4fadb-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4fadb-207">Nincs</span><span class="sxs-lookup"><span data-stu-id="4fadb-207">None</span></span>
- <span data-ttu-id="4fadb-208">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4fadb-208">ReadOnly</span></span>
- <span data-ttu-id="4fadb-209">ReadWrite: az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="4fadb-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="4fadb-210">Ha módosítja a gyorsítótár értékét, akkor a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="4fadb-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="4fadb-211">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="4fadb-211">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-212">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="4fadb-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="4fadb-213">Megadja, hogy az operációs rendszer merevlemezén engedélyezni vagy tiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="4fadb-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="4fadb-214">-Túlszabályozás</span><span class="sxs-lookup"><span data-stu-id="4fadb-214">-Overprovision</span></span>
<span data-ttu-id="4fadb-215">Azt jelzi, hogy a parancsmag túla VMSS-e.</span><span class="sxs-lookup"><span data-stu-id="4fadb-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="4fadb-216">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="4fadb-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="4fadb-217">Az egy kötegben lévő összes virtuális gép frissítésének várakozási ideje, és a következő köteg indítása.</span><span class="sxs-lookup"><span data-stu-id="4fadb-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="4fadb-218">Az időtartamot az ISO 8601-formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="4fadb-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="4fadb-219">Az alapértelmezett érték a 0 másodperc (PT0S).</span><span class="sxs-lookup"><span data-stu-id="4fadb-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="4fadb-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="4fadb-220">-PlanName</span></span>
<span data-ttu-id="4fadb-221">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="4fadb-222">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="4fadb-222">-PlanProduct</span></span>
<span data-ttu-id="4fadb-223">A csomag terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="4fadb-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="4fadb-224">-PlanPromotionCode</span></span>
<span data-ttu-id="4fadb-225">A csomag-előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="4fadb-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="4fadb-226">-PlanPublisher</span></span>
<span data-ttu-id="4fadb-227">A terv közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="4fadb-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="4fadb-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="4fadb-229">Azt jelzi, hogy a virtuális gép ügynöknek kiépítve kell-e lennie a Windows virtuális gépeken a VMSS.</span><span class="sxs-lookup"><span data-stu-id="4fadb-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="4fadb-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="4fadb-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="4fadb-231">Annak a közelségi helynek az erőforrás azonosítója, amellyel az adott méretarányt használni szeretné.</span><span class="sxs-lookup"><span data-stu-id="4fadb-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="4fadb-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fadb-232">-ResourceGroupName</span></span>
<span data-ttu-id="4fadb-233">Annak a csoportnak a neve, amelyhez a VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="4fadb-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="4fadb-234">-ScaleInPolicy</span></span>
<span data-ttu-id="4fadb-235">A virtuális gép méretarányának beállításakor követendő szabályok.</span><span class="sxs-lookup"><span data-stu-id="4fadb-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="4fadb-236">A lehetséges értékek a következők: "alapértelmezett", "OldestVM" és "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="4fadb-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="4fadb-237">"Alapértelmezett": Ha egy virtuális gép méretarányát a program átméretezi, a program először a méretarányokat fogja kiegyensúlyozni a zónáknál, ha a zóna zóna.</span><span class="sxs-lookup"><span data-stu-id="4fadb-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="4fadb-238">Ezt követően a lehető legtöbbet fogja kiegyensúlyozni a hibák tartományában.</span><span class="sxs-lookup"><span data-stu-id="4fadb-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="4fadb-239">Az egyes hibák tartománya alatt az eltávolításra kiválasztott virtuális gépek a legújabbak lesznek, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="4fadb-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="4fadb-240">"OldestVM": Ha egy virtuálisgép-készletet méretarányos, a program a legrégebbi virtuális gépeket választja, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="4fadb-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="4fadb-241">A virtuális gép méretarányos készletei esetében a méretarány először a zónáknál lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="4fadb-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="4fadb-242">Az egyes zónákon belül a legrégebbi virtuális gépeket választják ki a program az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="4fadb-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="4fadb-243">"NewestVM": Ha egy virtuálisgép-készletet méretezéssel végeznek, a program az eltávolításhoz a legújabb virtuális gépeket választja, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="4fadb-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="4fadb-244">A virtuális gép méretarányos készletei esetében a méretarány először a zónáknál lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="4fadb-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="4fadb-245">Az egyes zónákon belül a legújabb virtuális gépek, amelyek nem védettek, kiválasztásra kerülnek az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="4fadb-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="4fadb-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="4fadb-247">Az egyetlen elhelyezés csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-247">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="4fadb-248">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="4fadb-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="4fadb-249">Azt adja meg, hogy a bővítmények nem futnak az extra túlépített VMs-eszközön.</span><span class="sxs-lookup"><span data-stu-id="4fadb-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="4fadb-250">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4fadb-250">-SkuCapacity</span></span>
<span data-ttu-id="4fadb-251">A VMSS példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-251">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-252">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4fadb-252">-SkuName</span></span>
<span data-ttu-id="4fadb-253">A VMSS összes példányának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="4fadb-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4fadb-254">-SkuTier</span></span>
<span data-ttu-id="4fadb-255">A VMSS küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="4fadb-256">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4fadb-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4fadb-257">Standard</span><span class="sxs-lookup"><span data-stu-id="4fadb-257">Standard</span></span>
- <span data-ttu-id="4fadb-258">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="4fadb-258">Basic</span></span>

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

### <span data-ttu-id="4fadb-259">-Címke</span><span class="sxs-lookup"><span data-stu-id="4fadb-259">-Tag</span></span>
<span data-ttu-id="4fadb-260">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="4fadb-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4fadb-261">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="4fadb-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4fadb-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4fadb-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="4fadb-263">Konfigurálható időtartam (percben) a törölt virtuális gépet az esemény automatikus jóváhagyása előtt jóvá kell hagynia a befejezési ütemezett esemény előtt (időtúllépés esetén).</span><span class="sxs-lookup"><span data-stu-id="4fadb-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="4fadb-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="4fadb-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="4fadb-265">Azt adja meg, hogy engedélyezve van-e a Befejezés ütemezett esemény vagy le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="4fadb-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-266">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="4fadb-266">-TimeZone</span></span>
<span data-ttu-id="4fadb-267">A Windows operációs rendszerhez használt időzónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="4fadb-268">például \" Pacific standard Time \" .</span><span class="sxs-lookup"><span data-stu-id="4fadb-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="4fadb-269">A lehetséges értékek a [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)által eredményül adott időzónákban is [TimeZoneInfo.id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) .</span><span class="sxs-lookup"><span data-stu-id="4fadb-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="4fadb-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="4fadb-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="4fadb-271">A jelölő, amely lehetővé teszi vagy tiltja egy vagy több felügyelt adatlemez egy vagy több felügyelt adatlemezének UltraSSD_LRS tárolási fiók típusát a virtuálisgép-készlet beállításakor.</span><span class="sxs-lookup"><span data-stu-id="4fadb-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="4fadb-272">A felügyelt lemezek tároló típusú UltraSSD_LRS csak akkor vehetők fel a VMSS, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="4fadb-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="4fadb-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="4fadb-274">A méretarányban a virtuális gépekre való frissítés módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="4fadb-275">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4fadb-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4fadb-276">Automatikus</span><span class="sxs-lookup"><span data-stu-id="4fadb-276">Automatic</span></span>
- <span data-ttu-id="4fadb-277">Kézi</span><span class="sxs-lookup"><span data-stu-id="4fadb-277">Manual</span></span>
- <span data-ttu-id="4fadb-278">Gördülő</span><span class="sxs-lookup"><span data-stu-id="4fadb-278">Rolling</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-279">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="4fadb-279">-VhdContainer</span></span>
<span data-ttu-id="4fadb-280">Annak a tárolónak a tároló URL-címét adja meg, amely a VMSS operációs rendszer lemezének tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="4fadb-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4fadb-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4fadb-282">Helyi VMSS-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4fadb-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="4fadb-283">VMSS objektum beolvasásához használja az Get-AzVmss parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4fadb-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="4fadb-284">Ez a virtuálisgép-objektum a VMSS frissített állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4fadb-284">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4fadb-285">-VMScaleSetName</span></span>
<span data-ttu-id="4fadb-286">Annak a VMSS a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4fadb-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-287">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4fadb-287">-Confirm</span></span>
<span data-ttu-id="4fadb-288">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4fadb-288">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fadb-289">-WhatIf</span></span>
<span data-ttu-id="4fadb-290">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4fadb-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fadb-291">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fadb-291">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fadb-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fadb-292">CommonParameters</span></span>
<span data-ttu-id="4fadb-293">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fadb-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fadb-294">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4fadb-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fadb-295">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fadb-295">INPUTS</span></span>

### <span data-ttu-id="4fadb-296">System. String</span><span class="sxs-lookup"><span data-stu-id="4fadb-296">System.String</span></span>

### <span data-ttu-id="4fadb-297">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4fadb-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="4fadb-298">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4fadb-298">System.Boolean</span></span>

## <span data-ttu-id="4fadb-299">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fadb-299">OUTPUTS</span></span>

### <span data-ttu-id="4fadb-300">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4fadb-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4fadb-301">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fadb-301">NOTES</span></span>

## <span data-ttu-id="4fadb-302">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fadb-302">RELATED LINKS</span></span>

[<span data-ttu-id="4fadb-303">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4fadb-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="4fadb-304">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="4fadb-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="4fadb-305">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4fadb-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="4fadb-306">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="4fadb-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="4fadb-307">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4fadb-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="4fadb-308">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4fadb-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="4fadb-309">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4fadb-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)



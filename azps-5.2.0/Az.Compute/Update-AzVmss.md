---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344766"
---
# <span data-ttu-id="22a49-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="22a49-101">Update-AzVmss</span></span>

## <span data-ttu-id="22a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22a49-102">SYNOPSIS</span></span>
<span data-ttu-id="22a49-103">Frissíti a VMSS állapotát.</span><span class="sxs-lookup"><span data-stu-id="22a49-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="22a49-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22a49-104">SYNTAX</span></span>

### <span data-ttu-id="22a49-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22a49-105">DefaultParameter (Default)</span></span>
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

### <span data-ttu-id="22a49-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="22a49-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="22a49-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22a49-107">DESCRIPTION</span></span>
<span data-ttu-id="22a49-108">Az **Update-AzVmss** parancsmag frissíti a virtuálisgép-méretarány-készlet (VMSS) állapotát egy helyi VMSS-objektum állapotára.</span><span class="sxs-lookup"><span data-stu-id="22a49-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="22a49-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22a49-109">EXAMPLES</span></span>

### <span data-ttu-id="22a49-110">1. példa: A VMSS-objektumok állapotának frissítése helyi VMSS-objektum állapotára.</span><span class="sxs-lookup"><span data-stu-id="22a49-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="22a49-111">Ez a parancs frissíti a VMSS001 nevű VMSSS-t, amely a Group0001 nevű erőforráscsoporthoz tartozik, és frissíti egy helyi VMSS-objektum ( $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="22a49-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="22a49-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22a49-112">PARAMETERS</span></span>

### <span data-ttu-id="22a49-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22a49-113">-AsJob</span></span>
<span data-ttu-id="22a49-114">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="22a49-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="22a49-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="22a49-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="22a49-116">Azt adja meg, hogy a rendszer automatikusan alkalmazza-e az operációs rendszer frissítését a méretarány-készlet példányainak gördülékenként való alkalmazására, amikor a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="22a49-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="22a49-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="22a49-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="22a49-118">Az az idő, amelyre az automatikus javítást felfüggeszti a rendszer a VM-en egy állapotváltozás miatt.</span><span class="sxs-lookup"><span data-stu-id="22a49-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="22a49-119">A türelmi idő az állapotváltozás befejezése után kezdődik.</span><span class="sxs-lookup"><span data-stu-id="22a49-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="22a49-120">Ez segít elkerülni a véletlen vagy a véletlen javításokat.</span><span class="sxs-lookup"><span data-stu-id="22a49-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="22a49-121">Az időidőtartamot ISO 8601 formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="22a49-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="22a49-122">A minimális türelmi időszak 30 perc (PT30M), amely egyben az alapértelmezett érték is.</span><span class="sxs-lookup"><span data-stu-id="22a49-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="22a49-123">A maximális türelmi idő 90 perc (PT90M).</span><span class="sxs-lookup"><span data-stu-id="22a49-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="22a49-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="22a49-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="22a49-125">Be kell-e állítani a rendszerindítási diagnosztika funkciót a virtuális gép méretarány-készletében.</span><span class="sxs-lookup"><span data-stu-id="22a49-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="22a49-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="22a49-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="22a49-127">A konzol kimenetének és képernyőképének elhelyezéséhez használt tárfiók URI-ja.</span><span class="sxs-lookup"><span data-stu-id="22a49-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="22a49-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="22a49-128">-CustomData</span></span>
<span data-ttu-id="22a49-129">Egy 64-es alapkódolt egyéni adatokat kódolt karakterláncot ad meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="22a49-130">Ezt egy bináris tömbbe dekódolja, amely fájlként van mentve a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="22a49-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="22a49-131">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="22a49-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="22a49-132">Ha felhőbeli initet használ a VIRTUÁLIS GÉPhez, tekintse meg a Linux-virtuális gép testreszabása [felhőbeli init használatával a készítés során.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="22a49-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="22a49-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a49-133">-DefaultProfile</span></span>
<span data-ttu-id="22a49-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22a49-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22a49-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="22a49-135">-DisableAutoRollback</span></span>
<span data-ttu-id="22a49-136">Az automatikus visszaállítás letiltása az automatikus operációs rendszer frissítési házirendje esetén</span><span class="sxs-lookup"><span data-stu-id="22a49-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="22a49-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="22a49-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="22a49-138">Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést Linux operációs rendszerben.</span><span class="sxs-lookup"><span data-stu-id="22a49-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="22a49-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="22a49-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="22a49-140">Engedélyezze vagy tiltsa le az automatikus javításokat a virtuális gép méretaránykészletén.</span><span class="sxs-lookup"><span data-stu-id="22a49-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="22a49-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="22a49-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="22a49-142">Azt jelzi, hogy a VMSS virtuális gépei engedélyezve vannak-e az automatikus frissítésekhez.</span><span class="sxs-lookup"><span data-stu-id="22a49-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="22a49-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="22a49-143">-EncryptionAtHost</span></span>
<span data-ttu-id="22a49-144">Ezt a paramétert a felhasználó használhatja a kérésben a gazdatitkosítás engedélyezéséhez vagy letiltásához a virtuális gép méretaránykészletében.</span><span class="sxs-lookup"><span data-stu-id="22a49-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

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

### <span data-ttu-id="22a49-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="22a49-145">-IdentityId</span></span>
<span data-ttu-id="22a49-146">A virtuális gép méretkészletével társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="22a49-147">A felhasználói identitáshivatkozások ARM következő űrlapon található erőforrás-azonosítók lesznek: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="22a49-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="22a49-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="22a49-148">-IdentityType</span></span>
<span data-ttu-id="22a49-149">A virtuális gép méretaránykészletében használt identitás típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="22a49-150">A "SystemAssignedUserAssigned" típus egy implicit módon létrehozott identitást és egy felhasználóhoz rendelt identitáskészletet is tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="22a49-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="22a49-151">A "Nincs" típus eltávolítja az identitásokat a virtuális gép méretkészletből.</span><span class="sxs-lookup"><span data-stu-id="22a49-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="22a49-152">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="22a49-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22a49-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="22a49-153">SystemAssigned</span></span>
- <span data-ttu-id="22a49-154">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="22a49-154">UserAssigned</span></span>
- <span data-ttu-id="22a49-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="22a49-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="22a49-156">Nincs</span><span class="sxs-lookup"><span data-stu-id="22a49-156">None</span></span>

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

### <span data-ttu-id="22a49-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="22a49-157">-ImageReferenceId</span></span>
<span data-ttu-id="22a49-158">A képhivatkozás azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="22a49-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="22a49-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="22a49-160">A virtuális gép lemezképének (VMImage) ajánlat típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="22a49-161">Képajánlat beszerzéséhez használja a Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="22a49-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="22a49-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="22a49-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="22a49-163">Egy VMImage-közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="22a49-164">Közzétevő beszerzéséhez használja a Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="22a49-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="22a49-165">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="22a49-165">-ImageReferenceSku</span></span>
<span data-ttu-id="22a49-166">A VMImage termékváltozatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="22a49-167">Az SKUs-k beszerzéséhez használja a Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="22a49-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="22a49-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="22a49-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="22a49-169">A VMImage verziójának megadása.</span><span class="sxs-lookup"><span data-stu-id="22a49-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="22a49-170">A legújabb verzió csak akkor használható, ha az adott verzió helyett a legújabb értéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="22a49-171">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="22a49-171">-ImageUri</span></span>
<span data-ttu-id="22a49-172">A felhasználói kép blob-URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="22a49-173">A VMSS egy operációs rendszerlemezt hoz létre a felhasználói lemezkép ugyanazon tárolóban.</span><span class="sxs-lookup"><span data-stu-id="22a49-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="22a49-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="22a49-174">-LicenseType</span></span>
<span data-ttu-id="22a49-175">Adja meg a licenc típusát, amely a saját licenccel használható.</span><span class="sxs-lookup"><span data-stu-id="22a49-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="22a49-176">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="22a49-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="22a49-177">A felügyelt lemez tárfióktípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="22a49-178">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="22a49-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22a49-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="22a49-179">StandardLRS</span></span>
- <span data-ttu-id="22a49-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="22a49-180">PremiumLRS</span></span>

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

### <span data-ttu-id="22a49-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="22a49-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="22a49-182">Az összes virtuális gépi példánynak az a maximális százalékos aránya, amelyet egy kötegben a frissítéssel egyidejűleg frissít a rendszer.</span><span class="sxs-lookup"><span data-stu-id="22a49-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="22a49-183">Mivel ez a maximális, nem biztonságos példányok korábbi vagy jövőbeli kötegek esetén, a nagyobb megbízhatóság érdekében csökkentheti a kötegek példányainak százalékos arányát.</span><span class="sxs-lookup"><span data-stu-id="22a49-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="22a49-184">Ha az érték nincs megadva, akkor a 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="22a49-184">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="22a49-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="22a49-185">-MaxPrice</span></span>
<span data-ttu-id="22a49-186">Megadja az alacsony prioritású VM/VMSS-ek maximális árát.</span><span class="sxs-lookup"><span data-stu-id="22a49-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="22a49-187">Ez az ár amerikai dollárban van meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-187">This price is in US Dollars.</span></span> <span data-ttu-id="22a49-188">Ezt az árat összehasonlítjuk a VM-méret jelenlegi alacsony prioritású árával.</span><span class="sxs-lookup"><span data-stu-id="22a49-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="22a49-189">Ezenkívül az alacsony prioritású VM/VMSS létrehozása/frissítése során összehasonlítja az árakat, és a művelet csak akkor lesz sikeres, ha a maxPrice nagyobb, mint a jelenlegi alacsony prioritású ár.</span><span class="sxs-lookup"><span data-stu-id="22a49-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="22a49-190">A maxPrice akkor is használatos az alacsony prioritású VM/VMSS kivül, ha a jelenlegi alacsony prioritású ár meghaladja a VM/VMSS létrehozását követően a maxPrice értéken.</span><span class="sxs-lookup"><span data-stu-id="22a49-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="22a49-191">A lehetséges értékek a nullánál nagyobb decimális értékek.</span><span class="sxs-lookup"><span data-stu-id="22a49-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="22a49-192">Példa: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="22a49-192">Example: 0.01538.</span></span>  <span data-ttu-id="22a49-193">-1 azt jelzi, hogy az alacsony prioritású VM/VMSS nem lesz kiváltva ár miatt.</span><span class="sxs-lookup"><span data-stu-id="22a49-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="22a49-194">Az alapértelmezett maximális ár -1, ha nem Ön biztosítja.</span><span class="sxs-lookup"><span data-stu-id="22a49-194">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="22a49-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="22a49-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="22a49-196">A méretaránykészletben lévő összes virtuális gépi példánynak az a maximális százalékos értéke, amely egyidejűleg nem megfelelő működésű lehet, akár frissítés eredményeként, akár a virtuális gép állapot-ellenőrzése során nem megfelelő állapotban lévő állapot esetén, a frissítés megszakítása előtt.</span><span class="sxs-lookup"><span data-stu-id="22a49-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="22a49-197">Ezt a kényszert a köteg kezdése előtt ellenőrizni fogjuk.</span><span class="sxs-lookup"><span data-stu-id="22a49-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="22a49-198">Ha az érték nincs megadva, akkor a 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="22a49-198">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="22a49-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="22a49-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="22a49-200">A frissített virtuális gépi példányok azon maximális százalékos értéke, amely nem megfelelő állapotban van.</span><span class="sxs-lookup"><span data-stu-id="22a49-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="22a49-201">Ez az ellenőrzés az egyes kötegek frissítése után fog megtörténni.</span><span class="sxs-lookup"><span data-stu-id="22a49-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="22a49-202">Ha túllépi ezt a százalékos arányt, a görgető frissítés megszakad.</span><span class="sxs-lookup"><span data-stu-id="22a49-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="22a49-203">Ha az érték nincs megadva, akkor a 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="22a49-203">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="22a49-204">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="22a49-204">-OsDiskCaching</span></span>
<span data-ttu-id="22a49-205">Az operációs rendszer lemezének gyorsítótárazása.</span><span class="sxs-lookup"><span data-stu-id="22a49-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="22a49-206">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="22a49-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22a49-207">Nincs</span><span class="sxs-lookup"><span data-stu-id="22a49-207">None</span></span>
- <span data-ttu-id="22a49-208">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="22a49-208">ReadOnly</span></span>
- <span data-ttu-id="22a49-209">ReadWrite The default value is ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="22a49-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="22a49-210">Ha módosítja a gyorsítótárazás értékét, a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="22a49-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="22a49-211">Ez a beállítás befolyásolja a lemez konzisztenciáját és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="22a49-211">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="22a49-212">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="22a49-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="22a49-213">Azt adja meg, hogy a WriteAccelerator engedélyezve vagy letiltva legyen-e az operációs rendszer lemezén.</span><span class="sxs-lookup"><span data-stu-id="22a49-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="22a49-214">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="22a49-214">-Overprovision</span></span>
<span data-ttu-id="22a49-215">Azt jelzi, hogy a parancsmag túlépíti-e a VMSS-t.</span><span class="sxs-lookup"><span data-stu-id="22a49-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="22a49-216">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="22a49-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="22a49-217">A frissítés befejezése és a következő köteg megkezdése közötti várakozási idő az összes virtuális gépre egy kötegben.</span><span class="sxs-lookup"><span data-stu-id="22a49-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="22a49-218">Az időidőtartamot ISO 8601 formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="22a49-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="22a49-219">Az alapértelmezett érték 0 másodperc (PT0S).</span><span class="sxs-lookup"><span data-stu-id="22a49-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="22a49-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="22a49-220">-PlanName</span></span>
<span data-ttu-id="22a49-221">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="22a49-222">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="22a49-222">-PlanProduct</span></span>
<span data-ttu-id="22a49-223">A csomag termékét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="22a49-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="22a49-224">-PlanPromotionCode</span></span>
<span data-ttu-id="22a49-225">A csomag promóciós kódját adja meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="22a49-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="22a49-226">-PlanPublisher</span></span>
<span data-ttu-id="22a49-227">A terv közzétevője.</span><span class="sxs-lookup"><span data-stu-id="22a49-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="22a49-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="22a49-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="22a49-229">Azt jelzi, hogy a virtuális gép ügynökét a VMSS-beli Windows virtuális gépeken kell-e kiépítenünk.</span><span class="sxs-lookup"><span data-stu-id="22a49-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="22a49-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="22a49-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="22a49-231">Az ezzel a méretkészlethez használható Közelség elhelyezési csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="22a49-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="22a49-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a49-232">-ResourceGroupName</span></span>
<span data-ttu-id="22a49-233">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="22a49-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="22a49-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="22a49-234">-ScaleInPolicy</span></span>
<span data-ttu-id="22a49-235">A virtuális gép méretarányának beállításakor be kell tartani a szabályokat.</span><span class="sxs-lookup"><span data-stu-id="22a49-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="22a49-236">Lehetséges értékek: "Alapértelmezett", "LegrégebbiVM" és "LegújabbVM".</span><span class="sxs-lookup"><span data-stu-id="22a49-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="22a49-237">Az "Alapértelmezett" érték a virtuális gép méretarány-készletének méretaránya esetén először a zónák között lesz kiegyensúlyozott, ha az egy állatövi méretarányú készlet.</span><span class="sxs-lookup"><span data-stu-id="22a49-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="22a49-238">Ezt követően lehetőség szerint kiegyensúlyozott lesz a hibatartományok között.</span><span class="sxs-lookup"><span data-stu-id="22a49-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="22a49-239">Az egyes hibatartományok esetén az eltávolításhoz kiválasztott virtuális gépek lesznek a legújabbak, amelyek nem védettek a méretaránytól.</span><span class="sxs-lookup"><span data-stu-id="22a49-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="22a49-240">A "OldestVM" (LegrégebbiVM) akkor lesz kiválasztva eltávolításra, ha egy virtuális gép méretaránykészletét méretarányosra méretezi.</span><span class="sxs-lookup"><span data-stu-id="22a49-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="22a49-241">Az állatövi virtuális gép méretaránykészletek esetében a méretaránykészlet először zónák között lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="22a49-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="22a49-242">Az egyes zónákban a nem védett legrégebbi virtuális gépek lesznek kiválasztva eltávolításra.</span><span class="sxs-lookup"><span data-stu-id="22a49-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="22a49-243">"LegújabbVM", amikor egy virtuális gép méretaránykészletét méretarányosra méretezik, a rendszer eltávolítja a méretaránytól nem védett legújabb virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="22a49-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="22a49-244">Az állatövi virtuális gép méretaránykészletek esetében a méretaránykészlet először zónák között lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="22a49-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="22a49-245">Az egyes zónákon belül a nem védett legújabb virtuális gépek lesznek kiválasztva eltávolításra.</span><span class="sxs-lookup"><span data-stu-id="22a49-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="22a49-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="22a49-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="22a49-247">Az egyetlen elhelyezési csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-247">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="22a49-248">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="22a49-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="22a49-249">Azt adja meg, hogy a bővítmények nem futnak túlzsúfolt virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="22a49-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="22a49-250">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="22a49-250">-SkuCapacity</span></span>
<span data-ttu-id="22a49-251">A VMSS-ban található példányok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-251">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="22a49-252">-SkuName</span><span class="sxs-lookup"><span data-stu-id="22a49-252">-SkuName</span></span>
<span data-ttu-id="22a49-253">A VMSS összes példányának mérete.</span><span class="sxs-lookup"><span data-stu-id="22a49-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="22a49-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="22a49-254">-SkuTier</span></span>
<span data-ttu-id="22a49-255">A VMSS-hez megadott szint.</span><span class="sxs-lookup"><span data-stu-id="22a49-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="22a49-256">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="22a49-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22a49-257">Normál</span><span class="sxs-lookup"><span data-stu-id="22a49-257">Standard</span></span>
- <span data-ttu-id="22a49-258">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="22a49-258">Basic</span></span>

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

### <span data-ttu-id="22a49-259">-Tag</span><span class="sxs-lookup"><span data-stu-id="22a49-259">-Tag</span></span>
<span data-ttu-id="22a49-260">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="22a49-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="22a49-261">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="22a49-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="22a49-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="22a49-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="22a49-263">A virtuális gép által törölt virtuális gépnek a konfigurálható időtartamnak (percben) jóvá kell hagynia az Ütemezett esemény megszüntetését az esemény automatikus jóváhagyása (időkorrekta) előtt.</span><span class="sxs-lookup"><span data-stu-id="22a49-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="22a49-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="22a49-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="22a49-265">Azt adja meg, hogy engedélyezve vagy letiltva legyen-e az Ütemezett esemény megszüntetése esemény.</span><span class="sxs-lookup"><span data-stu-id="22a49-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="22a49-266">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="22a49-266">-TimeZone</span></span>
<span data-ttu-id="22a49-267">A Windows operációs rendszer időzónáját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="22a49-268">például a \" csendes-óceáni téli \" idő.</span><span class="sxs-lookup"><span data-stu-id="22a49-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="22a49-269">A lehetséges értékek a [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones) [által visszaadott](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) időzónákból származó TimeZoneInfo.Id is beállíthatók.</span><span class="sxs-lookup"><span data-stu-id="22a49-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="22a49-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="22a49-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="22a49-271">Az a jelölő, amely lehetővé teszi vagy letiltja azt a lehetőséget, hogy egy vagy több felügyelt adatlemez UltraSSD_LRS tárolófiók-típussal a virtuális gép méretaránykészletén legyen.</span><span class="sxs-lookup"><span data-stu-id="22a49-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="22a49-272">A tárfiók-típussal rendelkező felügyelt UltraSSD_LRS a VMSS-hez csak akkor lehet hozzáadni, ha ez a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="22a49-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="22a49-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="22a49-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="22a49-274">A virtuális gépekre való frissítés módját adja meg a méretaránykészletben.</span><span class="sxs-lookup"><span data-stu-id="22a49-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="22a49-275">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="22a49-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22a49-276">Automatikus</span><span class="sxs-lookup"><span data-stu-id="22a49-276">Automatic</span></span>
- <span data-ttu-id="22a49-277">Kézi</span><span class="sxs-lookup"><span data-stu-id="22a49-277">Manual</span></span>
- <span data-ttu-id="22a49-278">Görgetve</span><span class="sxs-lookup"><span data-stu-id="22a49-278">Rolling</span></span>

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

### <span data-ttu-id="22a49-279">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="22a49-279">-VhdContainer</span></span>
<span data-ttu-id="22a49-280">Megadja a VMSS operációs rendszer lemezének tárolására használt tároló URL-eket.</span><span class="sxs-lookup"><span data-stu-id="22a49-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="22a49-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="22a49-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="22a49-282">Egy helyi VMSS-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="22a49-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="22a49-283">VMSS-objektum beszerzéséhez használja a Get-AzVmss parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="22a49-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="22a49-284">Ez a virtuális gépi objektum a VMSS frissített állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="22a49-284">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="22a49-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="22a49-285">-VMScaleSetName</span></span>
<span data-ttu-id="22a49-286">A parancsmag által létrehozott VMSS neve.</span><span class="sxs-lookup"><span data-stu-id="22a49-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="22a49-287">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22a49-287">-Confirm</span></span>
<span data-ttu-id="22a49-288">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="22a49-288">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22a49-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22a49-289">-WhatIf</span></span>
<span data-ttu-id="22a49-290">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="22a49-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22a49-291">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22a49-291">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22a49-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a49-292">CommonParameters</span></span>
<span data-ttu-id="22a49-293">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22a49-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a49-294">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22a49-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a49-295">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22a49-295">INPUTS</span></span>

### <span data-ttu-id="22a49-296">System.String</span><span class="sxs-lookup"><span data-stu-id="22a49-296">System.String</span></span>

### <span data-ttu-id="22a49-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="22a49-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="22a49-298">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="22a49-298">System.Boolean</span></span>

## <span data-ttu-id="22a49-299">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22a49-299">OUTPUTS</span></span>

### <span data-ttu-id="22a49-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="22a49-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="22a49-301">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22a49-301">NOTES</span></span>

## <span data-ttu-id="22a49-302">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22a49-302">RELATED LINKS</span></span>

[<span data-ttu-id="22a49-303">Get-AzVms</span><span class="sxs-lookup"><span data-stu-id="22a49-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="22a49-304">Új-AzVms</span><span class="sxs-lookup"><span data-stu-id="22a49-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="22a49-305">Remove-AzVms</span><span class="sxs-lookup"><span data-stu-id="22a49-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="22a49-306">Restart-AzVms</span><span class="sxs-lookup"><span data-stu-id="22a49-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="22a49-307">Set-AzVms</span><span class="sxs-lookup"><span data-stu-id="22a49-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="22a49-308">Start-AzVms</span><span class="sxs-lookup"><span data-stu-id="22a49-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="22a49-309">Stop-AzVms</span><span class="sxs-lookup"><span data-stu-id="22a49-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)



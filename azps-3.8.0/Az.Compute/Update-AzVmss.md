---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: bf8fa8c4b7d1d08cdb6d0c2c348f5c97a2788a4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014587"
---
# <span data-ttu-id="ddd30-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd30-101">Update-AzVmss</span></span>

## <span data-ttu-id="ddd30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ddd30-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd30-103">Frissíti egy VMSS állapotát.</span><span class="sxs-lookup"><span data-stu-id="ddd30-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="ddd30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ddd30-104">SYNTAX</span></span>

### <span data-ttu-id="ddd30-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ddd30-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddd30-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd30-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddd30-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ddd30-107">DESCRIPTION</span></span>
<span data-ttu-id="ddd30-108">Az **Update-AzVmss** parancsmag a virtuálisgép-készlet (VMSS) állapotát egy helyi VMSS objektum állapotára frissíti.</span><span class="sxs-lookup"><span data-stu-id="ddd30-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="ddd30-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ddd30-109">EXAMPLES</span></span>

### <span data-ttu-id="ddd30-110">Példa 1: egy VMSS állapotának frissítése egy helyi VMSS-objektum állapotával.</span><span class="sxs-lookup"><span data-stu-id="ddd30-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="ddd30-111">Ez a parancs frissíti a Group001 nevű VMSS001 nevű VMSS állapotát egy helyi VMSS objektum állapotához, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd30-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="ddd30-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ddd30-112">PARAMETERS</span></span>

### <span data-ttu-id="ddd30-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddd30-113">-AsJob</span></span>
<span data-ttu-id="ddd30-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="ddd30-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ddd30-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ddd30-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="ddd30-116">Azt adja meg, hogy az operációs rendszer frissítéseit a program automatikusan alkalmazza-e a méretarányos példányokra, ha a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="ddd30-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="ddd30-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="ddd30-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="ddd30-118">Az az idő, ameddig a VM-ben bekövetkezett változások miatt az automatikus javítás fel van függesztve.</span><span class="sxs-lookup"><span data-stu-id="ddd30-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="ddd30-119">A türelmi idő az állam módosításának befejeződése után kezdődik.</span><span class="sxs-lookup"><span data-stu-id="ddd30-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="ddd30-120">Ez segít elkerülni a korai vagy véletlenszerű javításokat.</span><span class="sxs-lookup"><span data-stu-id="ddd30-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="ddd30-121">Az időtartamot az ISO 8601-formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="ddd30-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="ddd30-122">Az alapértelmezett érték 5 perc (PT5M).</span><span class="sxs-lookup"><span data-stu-id="ddd30-122">The default value is 5 minutes (PT5M).</span></span>

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

### <span data-ttu-id="ddd30-123">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="ddd30-123">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="ddd30-124">A virtuális gépek százalékos aránya (scaleset), amely egyszerre kerül javításra.</span><span class="sxs-lookup"><span data-stu-id="ddd30-124">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="ddd30-125">Az alapértelmezett érték 20%.</span><span class="sxs-lookup"><span data-stu-id="ddd30-125">The default value is 20%.</span></span>

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

### <span data-ttu-id="ddd30-126">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="ddd30-126">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="ddd30-127">A rendszerindítási diagnosztikát engedélyezni kell-e a virtuálisgép-méretarány beállításakor.</span><span class="sxs-lookup"><span data-stu-id="ddd30-127">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ddd30-128">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="ddd30-128">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="ddd30-129">A konzol kimenetének és képernyőképének elhelyezéséhez használandó tárolási fiók URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ddd30-129">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="ddd30-130">-CustomData</span><span class="sxs-lookup"><span data-stu-id="ddd30-130">-CustomData</span></span>
<span data-ttu-id="ddd30-131">Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="ddd30-131">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="ddd30-132">Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.</span><span class="sxs-lookup"><span data-stu-id="ddd30-132">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="ddd30-133">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="ddd30-133">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="ddd30-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd30-134">-DefaultProfile</span></span>
<span data-ttu-id="ddd30-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ddd30-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddd30-136">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="ddd30-136">-DisableAutoRollback</span></span>
<span data-ttu-id="ddd30-137">Automatikus visszagörgetés letiltása az automatikus operációs rendszer frissítési házirendjében</span><span class="sxs-lookup"><span data-stu-id="ddd30-137">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="ddd30-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="ddd30-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="ddd30-139">Jelzi, hogy ez a parancsmag letiltja a Linux operációs rendszerhez használt jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="ddd30-139">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="ddd30-140">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="ddd30-140">-EnableAutomaticRepair</span></span>
<span data-ttu-id="ddd30-141">Engedélyezze vagy tiltsa le az automatikus javítást a virtuálisgép-készlet beállítása lapon.</span><span class="sxs-lookup"><span data-stu-id="ddd30-141">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ddd30-142">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="ddd30-142">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="ddd30-143">Azt jelzi, hogy a VMSS engedélyezve vannak-e a Windows virtuális gépek az automatikus frissítésekhez.</span><span class="sxs-lookup"><span data-stu-id="ddd30-143">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="ddd30-144">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="ddd30-144">-IdentityId</span></span>
<span data-ttu-id="ddd30-145">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-145">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="ddd30-146">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="ddd30-146">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="ddd30-147">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ddd30-147">-IdentityType</span></span>
<span data-ttu-id="ddd30-148">A virtuálisgép-készlethez használt identitás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-148">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="ddd30-149">Az "SystemAssignedUserAssigned" típus egy implicit módon létrehozott identitást és egy, a felhasználó által kiosztott identitást tartalmazó készletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ddd30-149">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="ddd30-150">Ha a virtuálisgép-készletből eltávolítja az identitásokat, a "nincs" típust kell választania.</span><span class="sxs-lookup"><span data-stu-id="ddd30-150">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="ddd30-151">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ddd30-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd30-152">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="ddd30-152">SystemAssigned</span></span>
- <span data-ttu-id="ddd30-153">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="ddd30-153">UserAssigned</span></span>
- <span data-ttu-id="ddd30-154">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="ddd30-154">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="ddd30-155">Nincs</span><span class="sxs-lookup"><span data-stu-id="ddd30-155">None</span></span>

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

### <span data-ttu-id="ddd30-156">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="ddd30-156">-ImageReferenceId</span></span>
<span data-ttu-id="ddd30-157">A kép hivatkozási AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-157">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="ddd30-158">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="ddd30-158">-ImageReferenceOffer</span></span>
<span data-ttu-id="ddd30-159">A Virtual Machine Image (VMImage) ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-159">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="ddd30-160">Képajánlat beolvasásához használja az Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ddd30-160">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="ddd30-161">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="ddd30-161">-ImageReferencePublisher</span></span>
<span data-ttu-id="ddd30-162">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-162">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="ddd30-163">Publisher beolvasásához használja az Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ddd30-163">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="ddd30-164">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="ddd30-164">-ImageReferenceSku</span></span>
<span data-ttu-id="ddd30-165">A VMImage SKU-ot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-165">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="ddd30-166">A SKU beolvasásához használja az Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ddd30-166">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="ddd30-167">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="ddd30-167">-ImageReferenceVersion</span></span>
<span data-ttu-id="ddd30-168">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-168">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="ddd30-169">A legújabb verzió használatához adjon meg egy új értéket az adott verzió helyett.</span><span class="sxs-lookup"><span data-stu-id="ddd30-169">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="ddd30-170">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="ddd30-170">-ImageUri</span></span>
<span data-ttu-id="ddd30-171">A felhasználói kép blob-URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-171">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="ddd30-172">A VMSS létrehozza az operációs rendszer lemezét a felhasználói kép ugyanazon tárolójában.</span><span class="sxs-lookup"><span data-stu-id="ddd30-172">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="ddd30-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ddd30-173">-LicenseType</span></span>
<span data-ttu-id="ddd30-174">Adja meg azt a licenc-típust, amely a licencek használati forgatókönyvét hozza meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-174">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="ddd30-175">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ddd30-175">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="ddd30-176">A felügyelt lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-176">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="ddd30-177">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ddd30-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd30-178">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="ddd30-178">StandardLRS</span></span>
- <span data-ttu-id="ddd30-179">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="ddd30-179">PremiumLRS</span></span>

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

### <span data-ttu-id="ddd30-180">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="ddd30-180">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="ddd30-181">Annak a virtuális gép-példányoknak a maximális százalékos aránya, amelyet a rendszer egy kötegben a folyamatos frissítéssel egyidejűleg frissít.</span><span class="sxs-lookup"><span data-stu-id="ddd30-181">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="ddd30-182">Mivel az előző vagy a jövőbeli kötegekben ez a maximális, egészségtelen előfordulás, a kötegben lévő példányok százalékos arányát a nagyobb megbízhatóság érdekében is csökkentheti.</span><span class="sxs-lookup"><span data-stu-id="ddd30-182">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="ddd30-183">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="ddd30-183">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="ddd30-184">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="ddd30-184">-MaxPrice</span></span>
<span data-ttu-id="ddd30-185">Itt adhatja meg, hogy az alacsony prioritású VM/VMSS milyen maximális árat fizessen.</span><span class="sxs-lookup"><span data-stu-id="ddd30-185">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="ddd30-186">Ez az ár amerikai dollárban van.</span><span class="sxs-lookup"><span data-stu-id="ddd30-186">This price is in US Dollars.</span></span> <span data-ttu-id="ddd30-187">Ezt az árat a program összehasonlítja a VM-méret jelenlegi alacsony prioritási árával.</span><span class="sxs-lookup"><span data-stu-id="ddd30-187">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="ddd30-188">Az árakat az alacsony prioritású VM/VMSS létrehozásának/frissítésének időpontjában is összehasonlították, és a művelet csak akkor fog sikerülni, ha a maxPrice nagyobb, mint a jelenlegi alacsony prioritású ár.</span><span class="sxs-lookup"><span data-stu-id="ddd30-188">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="ddd30-189">A maxPrice a VM/VMSS létrehozása után is az alacsony prioritású VM/VMSS eltávolítására használható, ha a jelenlegi alacsony prioritású ár túllépi a maxPrice.</span><span class="sxs-lookup"><span data-stu-id="ddd30-189">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="ddd30-190">Lehetséges értékek: bármely nullánál nagyobb decimális érték.</span><span class="sxs-lookup"><span data-stu-id="ddd30-190">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="ddd30-191">Példa: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="ddd30-191">Example: 0.01538.</span></span>  <span data-ttu-id="ddd30-192">-1 – azt jelzi, hogy az alacsony prioritású VM/VMSS nem szabad az árak miatt kizárni.</span><span class="sxs-lookup"><span data-stu-id="ddd30-192">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="ddd30-193">Az alapértelmezett Max ár is-1, ha az nem az Ön által megadott.</span><span class="sxs-lookup"><span data-stu-id="ddd30-193">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="ddd30-194">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="ddd30-194">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="ddd30-195">A teljes virtuálisgép-példányok maximális százalékos aránya a készletben, amely egyidejű egészségtelen lehet, akár a frissítés során, akár a virtuálisgép-állapot ellenőrzésekor, a frissítés megszakítása előtt.</span><span class="sxs-lookup"><span data-stu-id="ddd30-195">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="ddd30-196">Ezt a korlátozást a program minden köteg kezdése előtt ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="ddd30-196">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="ddd30-197">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="ddd30-197">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="ddd30-198">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="ddd30-198">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="ddd30-199">A frissített virtuálisgép-példányok maximális százaléka, amely egészségtelen állapotban található.</span><span class="sxs-lookup"><span data-stu-id="ddd30-199">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="ddd30-200">Ez az ellenőrzés minden köteg frissítésekor megtörténik.</span><span class="sxs-lookup"><span data-stu-id="ddd30-200">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="ddd30-201">Ha a százalékos érték túllépve, a gördülési frissítés leáll.</span><span class="sxs-lookup"><span data-stu-id="ddd30-201">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="ddd30-202">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="ddd30-202">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="ddd30-203">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="ddd30-203">-OsDiskCaching</span></span>
<span data-ttu-id="ddd30-204">Az operációs rendszer lemezének gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-204">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="ddd30-205">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ddd30-205">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd30-206">Nincs</span><span class="sxs-lookup"><span data-stu-id="ddd30-206">None</span></span>
- <span data-ttu-id="ddd30-207">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ddd30-207">ReadOnly</span></span>
- <span data-ttu-id="ddd30-208">ReadWrite: az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="ddd30-208">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="ddd30-209">Ha módosítja a gyorsítótár értékét, akkor a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="ddd30-209">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="ddd30-210">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="ddd30-210">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="ddd30-211">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="ddd30-211">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="ddd30-212">Megadja, hogy az operációs rendszer merevlemezén engedélyezni vagy tiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="ddd30-212">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="ddd30-213">-Túlszabályozás</span><span class="sxs-lookup"><span data-stu-id="ddd30-213">-Overprovision</span></span>
<span data-ttu-id="ddd30-214">Azt jelzi, hogy a parancsmag túla VMSS-e.</span><span class="sxs-lookup"><span data-stu-id="ddd30-214">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="ddd30-215">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="ddd30-215">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="ddd30-216">Az egy kötegben lévő összes virtuális gép frissítésének várakozási ideje, és a következő köteg indítása.</span><span class="sxs-lookup"><span data-stu-id="ddd30-216">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="ddd30-217">Az időtartamot az ISO 8601-formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="ddd30-217">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="ddd30-218">Az alapértelmezett érték a 0 másodperc (PT0S).</span><span class="sxs-lookup"><span data-stu-id="ddd30-218">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="ddd30-219">-PlanName</span><span class="sxs-lookup"><span data-stu-id="ddd30-219">-PlanName</span></span>
<span data-ttu-id="ddd30-220">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-220">Specifies the plan name.</span></span>

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

### <span data-ttu-id="ddd30-221">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="ddd30-221">-PlanProduct</span></span>
<span data-ttu-id="ddd30-222">A csomag terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-222">Specifies the plan product.</span></span>

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

### <span data-ttu-id="ddd30-223">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="ddd30-223">-PlanPromotionCode</span></span>
<span data-ttu-id="ddd30-224">A csomag-előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-224">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="ddd30-225">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ddd30-225">-PlanPublisher</span></span>
<span data-ttu-id="ddd30-226">A terv közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-226">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="ddd30-227">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="ddd30-227">-ProvisionVMAgent</span></span>
<span data-ttu-id="ddd30-228">Azt jelzi, hogy a virtuális gép ügynöknek kiépítve kell-e lennie a Windows virtuális gépeken a VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd30-228">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="ddd30-229">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="ddd30-229">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="ddd30-230">Annak a közelségi helynek az erőforrás azonosítója, amellyel az adott méretarányt használni szeretné.</span><span class="sxs-lookup"><span data-stu-id="ddd30-230">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="ddd30-231">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd30-231">-ResourceGroupName</span></span>
<span data-ttu-id="ddd30-232">Annak a csoportnak a neve, amelyhez a VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="ddd30-232">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="ddd30-233">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="ddd30-233">-ScaleInPolicy</span></span>
<span data-ttu-id="ddd30-234">A virtuális gép méretarányának beállításakor követendő szabályok.</span><span class="sxs-lookup"><span data-stu-id="ddd30-234">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="ddd30-235">A lehetséges értékek a következők: "alapértelmezett", "OldestVM" és "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="ddd30-235">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="ddd30-236">"Alapértelmezett": Ha egy virtuális gép méretarányát a program átméretezi, a program először a méretarányokat fogja kiegyensúlyozni a zónáknál, ha a zóna zóna.</span><span class="sxs-lookup"><span data-stu-id="ddd30-236">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="ddd30-237">Ezt követően a lehető legtöbbet fogja kiegyensúlyozni a hibák tartományában.</span><span class="sxs-lookup"><span data-stu-id="ddd30-237">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="ddd30-238">Az egyes hibák tartománya alatt az eltávolításra kiválasztott virtuális gépek a legújabbak lesznek, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="ddd30-238">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="ddd30-239">"OldestVM": Ha egy virtuálisgép-készletet méretarányos, a program a legrégebbi virtuális gépeket választja, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="ddd30-239">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="ddd30-240">A virtuális gép méretarányos készletei esetében a méretarány először a zónáknál lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="ddd30-240">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="ddd30-241">Az egyes zónákon belül a legrégebbi virtuális gépeket választják ki a program az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="ddd30-241">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="ddd30-242">"NewestVM": Ha egy virtuálisgép-készletet méretezéssel végeznek, a program az eltávolításhoz a legújabb virtuális gépeket választja, amelyek nem védettek a méretarányban.</span><span class="sxs-lookup"><span data-stu-id="ddd30-242">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="ddd30-243">A virtuális gép méretarányos készletei esetében a méretarány először a zónáknál lesz kiegyensúlyozott.</span><span class="sxs-lookup"><span data-stu-id="ddd30-243">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="ddd30-244">Az egyes zónákon belül a legújabb virtuális gépek, amelyek nem védettek, kiválasztásra kerülnek az eltávolításhoz.</span><span class="sxs-lookup"><span data-stu-id="ddd30-244">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="ddd30-245">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ddd30-245">-SinglePlacementGroup</span></span>
<span data-ttu-id="ddd30-246">Az egyetlen elhelyezés csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-246">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="ddd30-247">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="ddd30-247">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="ddd30-248">Azt adja meg, hogy a bővítmények nem futnak az extra túlépített VMs-eszközön.</span><span class="sxs-lookup"><span data-stu-id="ddd30-248">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="ddd30-249">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ddd30-249">-SkuCapacity</span></span>
<span data-ttu-id="ddd30-250">A VMSS példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-250">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="ddd30-251">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ddd30-251">-SkuName</span></span>
<span data-ttu-id="ddd30-252">A VMSS összes példányának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-252">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="ddd30-253">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ddd30-253">-SkuTier</span></span>
<span data-ttu-id="ddd30-254">A VMSS küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-254">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="ddd30-255">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ddd30-255">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd30-256">Standard</span><span class="sxs-lookup"><span data-stu-id="ddd30-256">Standard</span></span>
- <span data-ttu-id="ddd30-257">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="ddd30-257">Basic</span></span>

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

### <span data-ttu-id="ddd30-258">-Címke</span><span class="sxs-lookup"><span data-stu-id="ddd30-258">-Tag</span></span>
<span data-ttu-id="ddd30-259">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="ddd30-259">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ddd30-260">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="ddd30-260">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ddd30-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ddd30-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="ddd30-262">Konfigurálható időtartam (percben) a törölt virtuális gépet az esemény automatikus jóváhagyása előtt jóvá kell hagynia a befejezési ütemezett esemény előtt (időtúllépés esetén).</span><span class="sxs-lookup"><span data-stu-id="ddd30-262">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="ddd30-263">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="ddd30-263">-TerminateScheduledEvents</span></span>
<span data-ttu-id="ddd30-264">Azt adja meg, hogy engedélyezve van-e a Befejezés ütemezett esemény vagy le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="ddd30-264">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="ddd30-265">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="ddd30-265">-TimeZone</span></span>
<span data-ttu-id="ddd30-266">A Windows operációs rendszerhez használt időzónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-266">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="ddd30-267">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="ddd30-267">-UltraSSDEnabled</span></span>
<span data-ttu-id="ddd30-268">A jelölő, amely lehetővé teszi vagy tiltja egy vagy több felügyelt adatlemez egy vagy több felügyelt adatlemezének UltraSSD_LRS tárolási fiók típusát a virtuálisgép-készlet beállításakor.</span><span class="sxs-lookup"><span data-stu-id="ddd30-268">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="ddd30-269">A felügyelt lemezek tároló típusú UltraSSD_LRS csak akkor vehetők fel a VMSS, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="ddd30-269">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="ddd30-270">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="ddd30-270">-UpgradePolicyMode</span></span>
<span data-ttu-id="ddd30-271">A méretarányban a virtuális gépekre való frissítés módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-271">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="ddd30-272">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ddd30-272">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd30-273">Automatikus</span><span class="sxs-lookup"><span data-stu-id="ddd30-273">Automatic</span></span>
- <span data-ttu-id="ddd30-274">Kézi</span><span class="sxs-lookup"><span data-stu-id="ddd30-274">Manual</span></span>
- <span data-ttu-id="ddd30-275">Gördülő</span><span class="sxs-lookup"><span data-stu-id="ddd30-275">Rolling</span></span>

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

### <span data-ttu-id="ddd30-276">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="ddd30-276">-VhdContainer</span></span>
<span data-ttu-id="ddd30-277">Annak a tárolónak a tároló URL-címét adja meg, amely a VMSS operációs rendszer lemezének tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="ddd30-277">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="ddd30-278">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ddd30-278">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ddd30-279">Helyi VMSS-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ddd30-279">Specifies a local VMSS object.</span></span>
<span data-ttu-id="ddd30-280">VMSS objektum beolvasásához használja az Get-AzVmss parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ddd30-280">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="ddd30-281">Ez a virtuálisgép-objektum a VMSS frissített állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ddd30-281">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="ddd30-282">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ddd30-282">-VMScaleSetName</span></span>
<span data-ttu-id="ddd30-283">Annak a VMSS a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ddd30-283">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ddd30-284">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ddd30-284">-Confirm</span></span>
<span data-ttu-id="ddd30-285">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ddd30-285">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd30-286">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd30-286">-WhatIf</span></span>
<span data-ttu-id="ddd30-287">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ddd30-287">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd30-288">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ddd30-288">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd30-289">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd30-289">CommonParameters</span></span>
<span data-ttu-id="ddd30-290">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ddd30-290">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd30-291">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ddd30-291">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd30-292">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddd30-292">INPUTS</span></span>

### <span data-ttu-id="ddd30-293">System. String</span><span class="sxs-lookup"><span data-stu-id="ddd30-293">System.String</span></span>

### <span data-ttu-id="ddd30-294">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ddd30-294">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ddd30-295">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ddd30-295">System.Boolean</span></span>

## <span data-ttu-id="ddd30-296">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddd30-296">OUTPUTS</span></span>

### <span data-ttu-id="ddd30-297">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ddd30-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ddd30-298">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ddd30-298">NOTES</span></span>

## <span data-ttu-id="ddd30-299">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddd30-299">RELATED LINKS</span></span>

[<span data-ttu-id="ddd30-300">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd30-300">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="ddd30-301">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd30-301">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="ddd30-302">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd30-302">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="ddd30-303">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd30-303">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="ddd30-304">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd30-304">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="ddd30-305">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd30-305">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="ddd30-306">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd30-306">Stop-AzVmss</span></span>](./Stop-AzVmss.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: c8a482c4d3021e1dd5de30582d2dad501a20ed41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667150"
---
# <span data-ttu-id="d7cc2-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d7cc2-101">Update-AzVmss</span></span>

## <span data-ttu-id="d7cc2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="d7cc2-103">Frissíti egy VMSS állapotát.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="d7cc2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7cc2-104">SYNTAX</span></span>

### <span data-ttu-id="d7cc2-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7cc2-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7cc2-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7cc2-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-IdentityId <String[]>] -IdentityType <ResourceIdentityType> [-ImageReferenceId <String>]
 [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>]
 [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7cc2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7cc2-107">DESCRIPTION</span></span>
<span data-ttu-id="d7cc2-108">Az **Update-AzVmss** parancsmag a virtuálisgép-készlet (VMSS) állapotát egy helyi VMSS objektum állapotára frissíti.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="d7cc2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d7cc2-109">EXAMPLES</span></span>

### <span data-ttu-id="d7cc2-110">Példa 1: egy VMSS állapotának frissítése egy helyi VMSS-objektum állapotával.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="d7cc2-111">Ez a parancs frissíti a Group001 nevű VMSS001 nevű VMSS állapotát egy helyi VMSS objektum állapotához, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="d7cc2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7cc2-112">PARAMETERS</span></span>

### <span data-ttu-id="d7cc2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7cc2-113">-AsJob</span></span>
<span data-ttu-id="d7cc2-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d7cc2-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="d7cc2-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="d7cc2-116">Azt adja meg, hogy az operációs rendszer frissítéseit a program automatikusan alkalmazza-e a méretarányos példányokra, ha a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="d7cc2-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="d7cc2-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="d7cc2-118">A rendszerindítási diagnosztikát engedélyezni kell-e a virtuálisgép-méretarány beállításakor.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d7cc2-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="d7cc2-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="d7cc2-120">A konzol kimenetének és képernyőképének elhelyezéséhez használandó tárolási fiók URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="d7cc2-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="d7cc2-121">-CustomData</span></span>
<span data-ttu-id="d7cc2-122">Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="d7cc2-123">Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="d7cc2-124">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="d7cc2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7cc2-125">-DefaultProfile</span></span>
<span data-ttu-id="d7cc2-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7cc2-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="d7cc2-127">-DisableAutoRollback</span></span>
<span data-ttu-id="d7cc2-128">Automatikus visszagörgetés letiltása az automatikus operációs rendszer frissítési házirendjében</span><span class="sxs-lookup"><span data-stu-id="d7cc2-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="d7cc2-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="d7cc2-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="d7cc2-130">Jelzi, hogy ez a parancsmag letiltja a Linux operációs rendszerhez használt jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="d7cc2-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="d7cc2-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="d7cc2-132">Azt jelzi, hogy a VMSS engedélyezve vannak-e a Windows virtuális gépek az automatikus frissítésekhez.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="d7cc2-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="d7cc2-133">-IdentityId</span></span>
<span data-ttu-id="d7cc2-134">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="d7cc2-135">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="d7cc2-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d7cc2-136">-IdentityType</span></span>
<span data-ttu-id="d7cc2-137">A virtuálisgép-készlethez használt identitás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="d7cc2-138">Az "SystemAssignedUserAssigned" típus egy implicit módon létrehozott identitást és egy, a felhasználó által kiosztott identitást tartalmazó készletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="d7cc2-139">Ha a virtuálisgép-készletből eltávolítja az identitásokat, a "nincs" típust kell választania.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="d7cc2-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d7cc2-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7cc2-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="d7cc2-141">SystemAssigned</span></span>
- <span data-ttu-id="d7cc2-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="d7cc2-142">UserAssigned</span></span>
- <span data-ttu-id="d7cc2-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="d7cc2-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="d7cc2-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7cc2-144">None</span></span>

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

### <span data-ttu-id="d7cc2-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="d7cc2-145">-ImageReferenceId</span></span>
<span data-ttu-id="d7cc2-146">A kép hivatkozási AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="d7cc2-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="d7cc2-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="d7cc2-148">A Virtual Machine Image (VMImage) ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="d7cc2-149">Képajánlat beolvasásához használja az Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-149">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="d7cc2-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="d7cc2-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="d7cc2-151">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="d7cc2-152">Publisher beolvasásához használja az Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-152">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="d7cc2-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="d7cc2-153">-ImageReferenceSku</span></span>
<span data-ttu-id="d7cc2-154">A VMImage SKU-ot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="d7cc2-155">A SKU beolvasásához használja az Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-155">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="d7cc2-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="d7cc2-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="d7cc2-157">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="d7cc2-158">A legújabb verzió használatához adjon meg egy új értéket az adott verzió helyett.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="d7cc2-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="d7cc2-159">-ImageUri</span></span>
<span data-ttu-id="d7cc2-160">A felhasználói kép blob-URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="d7cc2-161">A VMSS létrehozza az operációs rendszer lemezét a felhasználói kép ugyanazon tárolójában.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="d7cc2-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d7cc2-162">-LicenseType</span></span>
<span data-ttu-id="d7cc2-163">Adja meg azt a licenc-típust, amely a licencek használati forgatókönyvét hozza meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="d7cc2-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d7cc2-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="d7cc2-165">A felügyelt lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="d7cc2-166">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d7cc2-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7cc2-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="d7cc2-167">StandardLRS</span></span>
- <span data-ttu-id="d7cc2-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="d7cc2-168">PremiumLRS</span></span>

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

### <span data-ttu-id="d7cc2-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d7cc2-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="d7cc2-170">Annak a virtuális gép-példányoknak a maximális százalékos aránya, amelyet a rendszer egy kötegben a folyamatos frissítéssel egyidejűleg frissít.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="d7cc2-171">Mivel az előző vagy a jövőbeli kötegekben ez a maximális, egészségtelen előfordulás, a kötegben lévő példányok százalékos arányát a nagyobb megbízhatóság érdekében is csökkentheti.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="d7cc2-172">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="d7cc2-173">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="d7cc2-173">-MaxPrice</span></span>
<span data-ttu-id="d7cc2-174">Itt adhatja meg, hogy az alacsony prioritású VM/VMSS milyen maximális árat fizessen.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-174">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="d7cc2-175">Ez az ár amerikai dollárban van.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-175">This price is in US Dollars.</span></span> <span data-ttu-id="d7cc2-176">Ezt az árat a program összehasonlítja a VM-méret jelenlegi alacsony prioritási árával.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-176">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="d7cc2-177">Az árakat az alacsony prioritású VM/VMSS létrehozásának/frissítésének időpontjában is összehasonlították, és a művelet csak akkor fog sikerülni, ha a maxPrice nagyobb, mint a jelenlegi alacsony prioritású ár.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-177">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="d7cc2-178">A maxPrice a VM/VMSS létrehozása után is az alacsony prioritású VM/VMSS eltávolítására használható, ha a jelenlegi alacsony prioritású ár túllépi a maxPrice.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-178">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="d7cc2-179">Lehetséges értékek: bármely nullánál nagyobb decimális érték.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-179">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="d7cc2-180">Példa: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-180">Example: 0.01538.</span></span>  <span data-ttu-id="d7cc2-181">-1 – azt jelzi, hogy az alacsony prioritású VM/VMSS nem szabad az árak miatt kizárni.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-181">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="d7cc2-182">Az alapértelmezett Max ár is-1, ha az nem az Ön által megadott.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-182">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="d7cc2-183">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d7cc2-183">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="d7cc2-184">A teljes virtuálisgép-példányok maximális százalékos aránya a készletben, amely egyidejű egészségtelen lehet, akár a frissítés során, akár a virtuálisgép-állapot ellenőrzésekor, a frissítés megszakítása előtt.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-184">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="d7cc2-185">Ezt a korlátozást a program minden köteg kezdése előtt ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-185">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="d7cc2-186">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-186">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="d7cc2-187">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d7cc2-187">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="d7cc2-188">A frissített virtuálisgép-példányok maximális százaléka, amely egészségtelen állapotban található.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-188">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="d7cc2-189">Ez az ellenőrzés minden köteg frissítésekor megtörténik.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-189">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="d7cc2-190">Ha a százalékos érték túllépve, a gördülési frissítés leáll.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-190">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="d7cc2-191">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-191">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="d7cc2-192">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="d7cc2-192">-OsDiskCaching</span></span>
<span data-ttu-id="d7cc2-193">Az operációs rendszer lemezének gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-193">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="d7cc2-194">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d7cc2-194">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7cc2-195">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7cc2-195">None</span></span>
- <span data-ttu-id="d7cc2-196">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d7cc2-196">ReadOnly</span></span>
- <span data-ttu-id="d7cc2-197">ReadWrite: az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-197">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="d7cc2-198">Ha módosítja a gyorsítótár értékét, akkor a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-198">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="d7cc2-199">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-199">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="d7cc2-200">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="d7cc2-200">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="d7cc2-201">Megadja, hogy az operációs rendszer merevlemezén engedélyezni vagy tiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-201">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="d7cc2-202">-Túlszabályozás</span><span class="sxs-lookup"><span data-stu-id="d7cc2-202">-Overprovision</span></span>
<span data-ttu-id="d7cc2-203">Azt jelzi, hogy a parancsmag túla VMSS-e.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-203">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="d7cc2-204">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="d7cc2-204">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="d7cc2-205">Az egy kötegben lévő összes virtuális gép frissítésének várakozási ideje, és a következő köteg indítása.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-205">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="d7cc2-206">Az időtartamot az ISO 8601-formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-206">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="d7cc2-207">Az alapértelmezett érték a 0 másodperc (PT0S).</span><span class="sxs-lookup"><span data-stu-id="d7cc2-207">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="d7cc2-208">-PlanName</span><span class="sxs-lookup"><span data-stu-id="d7cc2-208">-PlanName</span></span>
<span data-ttu-id="d7cc2-209">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-209">Specifies the plan name.</span></span>

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

### <span data-ttu-id="d7cc2-210">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="d7cc2-210">-PlanProduct</span></span>
<span data-ttu-id="d7cc2-211">A csomag terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-211">Specifies the plan product.</span></span>

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

### <span data-ttu-id="d7cc2-212">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="d7cc2-212">-PlanPromotionCode</span></span>
<span data-ttu-id="d7cc2-213">A csomag-előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-213">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="d7cc2-214">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="d7cc2-214">-PlanPublisher</span></span>
<span data-ttu-id="d7cc2-215">A terv közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-215">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="d7cc2-216">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="d7cc2-216">-ProvisionVMAgent</span></span>
<span data-ttu-id="d7cc2-217">Azt jelzi, hogy a virtuális gép ügynöknek kiépítve kell-e lennie a Windows virtuális gépeken a VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-217">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="d7cc2-218">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7cc2-218">-ResourceGroupName</span></span>
<span data-ttu-id="d7cc2-219">Annak a csoportnak a neve, amelyhez a VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-219">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="d7cc2-220">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d7cc2-220">-SinglePlacementGroup</span></span>
<span data-ttu-id="d7cc2-221">Az egyetlen elhelyezés csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-221">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="d7cc2-222">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d7cc2-222">-SkuCapacity</span></span>
<span data-ttu-id="d7cc2-223">A VMSS példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-223">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="d7cc2-224">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d7cc2-224">-SkuName</span></span>
<span data-ttu-id="d7cc2-225">A VMSS összes példányának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-225">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="d7cc2-226">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d7cc2-226">-SkuTier</span></span>
<span data-ttu-id="d7cc2-227">A VMSS küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-227">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="d7cc2-228">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d7cc2-228">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7cc2-229">Standard</span><span class="sxs-lookup"><span data-stu-id="d7cc2-229">Standard</span></span>
- <span data-ttu-id="d7cc2-230">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="d7cc2-230">Basic</span></span>

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

### <span data-ttu-id="d7cc2-231">-Címke</span><span class="sxs-lookup"><span data-stu-id="d7cc2-231">-Tag</span></span>
<span data-ttu-id="d7cc2-232">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-232">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d7cc2-233">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="d7cc2-233">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d7cc2-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d7cc2-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="d7cc2-235">Konfigurálható időtartam (percben) a törölt virtuális gépet az esemény automatikus jóváhagyása előtt jóvá kell hagynia a befejezési ütemezett esemény előtt (időtúllépés esetén).</span><span class="sxs-lookup"><span data-stu-id="d7cc2-235">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="d7cc2-236">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="d7cc2-236">-TerminateScheduledEvents</span></span>
<span data-ttu-id="d7cc2-237">Azt adja meg, hogy engedélyezve van-e a Befejezés ütemezett esemény vagy le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-237">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="d7cc2-238">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="d7cc2-238">-TimeZone</span></span>
<span data-ttu-id="d7cc2-239">A Windows operációs rendszerhez használt időzónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-239">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="d7cc2-240">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="d7cc2-240">-UltraSSDEnabled</span></span>
<span data-ttu-id="d7cc2-241">A jelölő, amely lehetővé teszi vagy tiltja egy vagy több felügyelt adatlemez egy vagy több felügyelt adatlemezének UltraSSD_LRS tárolási fiók típusát a virtuálisgép-készlet beállításakor.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-241">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="d7cc2-242">A felügyelt lemezek tároló típusú UltraSSD_LRS csak akkor vehetők fel a VMSS, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-242">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="d7cc2-243">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="d7cc2-243">-UpgradePolicyMode</span></span>
<span data-ttu-id="d7cc2-244">A méretarányban a virtuális gépekre való frissítés módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-244">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="d7cc2-245">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d7cc2-245">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7cc2-246">Automatikus</span><span class="sxs-lookup"><span data-stu-id="d7cc2-246">Automatic</span></span>
- <span data-ttu-id="d7cc2-247">Kézi</span><span class="sxs-lookup"><span data-stu-id="d7cc2-247">Manual</span></span>
- <span data-ttu-id="d7cc2-248">Gördülő</span><span class="sxs-lookup"><span data-stu-id="d7cc2-248">Rolling</span></span>

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

### <span data-ttu-id="d7cc2-249">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="d7cc2-249">-VhdContainer</span></span>
<span data-ttu-id="d7cc2-250">Annak a tárolónak a tároló URL-címét adja meg, amely a VMSS operációs rendszer lemezének tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-250">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="d7cc2-251">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d7cc2-251">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d7cc2-252">Helyi VMSS-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-252">Specifies a local VMSS object.</span></span>
<span data-ttu-id="d7cc2-253">VMSS objektum beolvasásához használja az Get-AzVmss parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-253">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="d7cc2-254">Ez a virtuálisgép-objektum a VMSS frissített állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-254">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="d7cc2-255">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d7cc2-255">-VMScaleSetName</span></span>
<span data-ttu-id="d7cc2-256">Annak a VMSS a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-256">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d7cc2-257">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7cc2-257">-Confirm</span></span>
<span data-ttu-id="d7cc2-258">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-258">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7cc2-259">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7cc2-259">-WhatIf</span></span>
<span data-ttu-id="d7cc2-260">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-260">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7cc2-261">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-261">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7cc2-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7cc2-262">CommonParameters</span></span>
<span data-ttu-id="d7cc2-263">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7cc2-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7cc2-264">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d7cc2-264">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7cc2-265">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7cc2-265">INPUTS</span></span>

### <span data-ttu-id="d7cc2-266">System. String</span><span class="sxs-lookup"><span data-stu-id="d7cc2-266">System.String</span></span>

### <span data-ttu-id="d7cc2-267">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d7cc2-267">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d7cc2-268">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7cc2-268">System.Boolean</span></span>

## <span data-ttu-id="d7cc2-269">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7cc2-269">OUTPUTS</span></span>

### <span data-ttu-id="d7cc2-270">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d7cc2-270">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d7cc2-271">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7cc2-271">NOTES</span></span>

## <span data-ttu-id="d7cc2-272">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7cc2-272">RELATED LINKS</span></span>

[<span data-ttu-id="d7cc2-273">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d7cc2-273">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="d7cc2-274">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="d7cc2-274">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="d7cc2-275">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d7cc2-275">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="d7cc2-276">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="d7cc2-276">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="d7cc2-277">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d7cc2-277">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="d7cc2-278">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d7cc2-278">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="d7cc2-279">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d7cc2-279">Stop-AzVmss</span></span>](./Stop-AzVmss.md)



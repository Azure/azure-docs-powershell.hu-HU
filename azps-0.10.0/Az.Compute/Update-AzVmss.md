---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 5e3bafbc667cc0e26eb6469e681ca9355b4f307f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844165"
---
# <span data-ttu-id="e7951-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e7951-101">Update-AzVmss</span></span>

## <span data-ttu-id="e7951-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7951-102">SYNOPSIS</span></span>
<span data-ttu-id="e7951-103">Frissíti egy VMSS állapotát.</span><span class="sxs-lookup"><span data-stu-id="e7951-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="e7951-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7951-104">SYNTAX</span></span>

### <span data-ttu-id="e7951-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7951-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7951-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7951-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] -IdentityType <ResourceIdentityType>
 [-SkuName <String>] [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>]
 [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>]
 [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7951-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7951-107">DESCRIPTION</span></span>
<span data-ttu-id="e7951-108">Az **Update-AzVmss** parancsmag a virtuálisgép-készlet (VMSS) állapotát egy helyi VMSS objektum állapotára frissíti.</span><span class="sxs-lookup"><span data-stu-id="e7951-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="e7951-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e7951-109">EXAMPLES</span></span>

### <span data-ttu-id="e7951-110">Példa 1: egy VMSS állapotának frissítése egy helyi VMSS-objektum állapotával.</span><span class="sxs-lookup"><span data-stu-id="e7951-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="e7951-111">Ez a parancs frissíti a Group001 nevű VMSS001 nevű VMSS állapotát egy helyi VMSS objektum állapotához, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="e7951-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="e7951-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7951-112">PARAMETERS</span></span>

### <span data-ttu-id="e7951-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7951-113">-AsJob</span></span>
<span data-ttu-id="e7951-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="e7951-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="e7951-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="e7951-116">Azt adja meg, hogy az operációs rendszer frissítéseit a program automatikusan alkalmazza-e a méretarányos példányokra, ha a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="e7951-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="e7951-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="e7951-118">A rendszerindítási diagnosztikát engedélyezni kell-e a virtuálisgép-méretarány beállításakor.</span><span class="sxs-lookup"><span data-stu-id="e7951-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="e7951-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="e7951-120">A konzol kimenetének és képernyőképének elhelyezéséhez használandó tárolási fiók URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e7951-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="e7951-121">-CustomData</span></span>
<span data-ttu-id="e7951-122">Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="e7951-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="e7951-123">Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.</span><span class="sxs-lookup"><span data-stu-id="e7951-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="e7951-124">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="e7951-124">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7951-125">-DefaultProfile</span></span>
<span data-ttu-id="e7951-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7951-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-127">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="e7951-127">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="e7951-128">Jelzi, hogy ez a parancsmag letiltja a Linux operációs rendszerhez használt jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="e7951-128">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-129">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="e7951-129">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="e7951-130">Azt jelzi, hogy a VMSS engedélyezve vannak-e a Windows virtuális gépek az automatikus frissítésekhez.</span><span class="sxs-lookup"><span data-stu-id="e7951-130">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-131">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="e7951-131">-IdentityId</span></span>
<span data-ttu-id="e7951-132">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-132">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="e7951-133">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="e7951-133">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-134">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e7951-134">-IdentityType</span></span>
<span data-ttu-id="e7951-135">A virtuálisgép-készlethez használt identitás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-135">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="e7951-136">Az "SystemAssignedUserAssigned" típus egy implicit módon létrehozott identitást és egy, a felhasználó által kiosztott identitást tartalmazó készletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e7951-136">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="e7951-137">Ha a virtuálisgép-készletből eltávolítja az identitásokat, a "nincs" típust kell választania.</span><span class="sxs-lookup"><span data-stu-id="e7951-137">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="e7951-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e7951-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7951-139">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="e7951-139">SystemAssigned</span></span>
- <span data-ttu-id="e7951-140">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="e7951-140">UserAssigned</span></span>
- <span data-ttu-id="e7951-141">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="e7951-141">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="e7951-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="e7951-142">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-143">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="e7951-143">-ImageReferenceId</span></span>
<span data-ttu-id="e7951-144">A kép hivatkozási AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-144">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-145">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="e7951-145">-ImageReferenceOffer</span></span>
<span data-ttu-id="e7951-146">A Virtual Machine Image (VMImage) ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-146">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="e7951-147">Képajánlat beolvasásához használja az Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e7951-147">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-148">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="e7951-148">-ImageReferencePublisher</span></span>
<span data-ttu-id="e7951-149">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-149">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="e7951-150">Publisher beolvasásához használja az Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e7951-150">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-151">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="e7951-151">-ImageReferenceSku</span></span>
<span data-ttu-id="e7951-152">A VMImage SKU-ot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-152">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="e7951-153">A SKU beolvasásához használja az Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e7951-153">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-154">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="e7951-154">-ImageReferenceVersion</span></span>
<span data-ttu-id="e7951-155">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-155">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="e7951-156">A legújabb verzió használatához adjon meg egy új értéket az adott verzió helyett.</span><span class="sxs-lookup"><span data-stu-id="e7951-156">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-157">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="e7951-157">-ImageUri</span></span>
<span data-ttu-id="e7951-158">A felhasználói kép blob-URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-158">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="e7951-159">A VMSS létrehozza az operációs rendszer lemezét a felhasználói kép ugyanazon tárolójában.</span><span class="sxs-lookup"><span data-stu-id="e7951-159">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-160">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e7951-160">-LicenseType</span></span>
<span data-ttu-id="e7951-161">Adja meg azt a licenc-típust, amely a licencek használati forgatókönyvét hozza meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-161">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-162">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e7951-162">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="e7951-163">A felügyelt lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-163">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="e7951-164">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e7951-164">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7951-165">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="e7951-165">StandardLRS</span></span>
- <span data-ttu-id="e7951-166">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="e7951-166">PremiumLRS</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-167">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="e7951-167">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="e7951-168">Annak a virtuális gép-példányoknak a maximális százalékos aránya, amelyet a rendszer egy kötegben a folyamatos frissítéssel egyidejűleg frissít.</span><span class="sxs-lookup"><span data-stu-id="e7951-168">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="e7951-169">Mivel az előző vagy a jövőbeli kötegekben ez a maximális, egészségtelen előfordulás, a kötegben lévő példányok százalékos arányát a nagyobb megbízhatóság érdekében is csökkentheti.</span><span class="sxs-lookup"><span data-stu-id="e7951-169">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="e7951-170">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="e7951-170">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-171">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="e7951-171">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="e7951-172">A teljes virtuálisgép-példányok maximális százalékos aránya a készletben, amely egyidejű egészségtelen lehet, akár a frissítés során, akár a virtuálisgép-állapot ellenőrzésekor, a frissítés megszakítása előtt.</span><span class="sxs-lookup"><span data-stu-id="e7951-172">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="e7951-173">Ezt a korlátozást a program minden köteg kezdése előtt ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="e7951-173">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="e7951-174">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="e7951-174">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-175">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="e7951-175">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="e7951-176">A frissített virtuálisgép-példányok maximális százaléka, amely egészségtelen állapotban található.</span><span class="sxs-lookup"><span data-stu-id="e7951-176">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="e7951-177">Ez az ellenőrzés minden köteg frissítésekor megtörténik.</span><span class="sxs-lookup"><span data-stu-id="e7951-177">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="e7951-178">Ha a százalékos érték túllépve, a gördülési frissítés leáll.</span><span class="sxs-lookup"><span data-stu-id="e7951-178">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="e7951-179">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="e7951-179">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-180">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="e7951-180">-OsDiskCaching</span></span>
<span data-ttu-id="e7951-181">Az operációs rendszer lemezének gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-181">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="e7951-182">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e7951-182">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7951-183">Nincs</span><span class="sxs-lookup"><span data-stu-id="e7951-183">None</span></span>
- <span data-ttu-id="e7951-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="e7951-184">ReadOnly</span></span>
- <span data-ttu-id="e7951-185">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e7951-185">ReadWrite</span></span>

<span data-ttu-id="e7951-186">Az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="e7951-186">The default value is ReadWrite.</span></span>
<span data-ttu-id="e7951-187">Ha módosítja a gyorsítótár értékét, akkor a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="e7951-187">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="e7951-188">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="e7951-188">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-189">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e7951-189">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="e7951-190">Megadja, hogy az operációs rendszer merevlemezén engedélyezni vagy tiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="e7951-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-191">-Túlszabályozás</span><span class="sxs-lookup"><span data-stu-id="e7951-191">-Overprovision</span></span>
<span data-ttu-id="e7951-192">Azt jelzi, hogy a parancsmag túla VMSS-e.</span><span class="sxs-lookup"><span data-stu-id="e7951-192">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-193">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="e7951-193">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="e7951-194">Az egy kötegben lévő összes virtuális gép frissítésének várakozási ideje, és a következő köteg indítása.</span><span class="sxs-lookup"><span data-stu-id="e7951-194">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="e7951-195">Az időtartamot az ISO 8601-formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="e7951-195">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="e7951-196">Az alapértelmezett érték a 0 másodperc (PT0S).</span><span class="sxs-lookup"><span data-stu-id="e7951-196">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-197">-PlanName</span><span class="sxs-lookup"><span data-stu-id="e7951-197">-PlanName</span></span>
<span data-ttu-id="e7951-198">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-198">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-199">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="e7951-199">-PlanProduct</span></span>
<span data-ttu-id="e7951-200">A csomag terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-200">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-201">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="e7951-201">-PlanPromotionCode</span></span>
<span data-ttu-id="e7951-202">A csomag-előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-202">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-203">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="e7951-203">-PlanPublisher</span></span>
<span data-ttu-id="e7951-204">A terv közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-204">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-205">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="e7951-205">-ProvisionVMAgent</span></span>
<span data-ttu-id="e7951-206">Azt jelzi, hogy a virtuális gép ügynöknek kiépítve kell-e lennie a Windows virtuális gépeken a VMSS.</span><span class="sxs-lookup"><span data-stu-id="e7951-206">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7951-207">-ResourceGroupName</span></span>
<span data-ttu-id="e7951-208">Annak a csoportnak a neve, amelyhez a VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="e7951-208">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-209">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e7951-209">-SinglePlacementGroup</span></span>
<span data-ttu-id="e7951-210">Az egyetlen elhelyezés csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-210">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-211">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e7951-211">-SkuCapacity</span></span>
<span data-ttu-id="e7951-212">A VMSS példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-212">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-213">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e7951-213">-SkuName</span></span>
<span data-ttu-id="e7951-214">A VMSS összes példányának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-214">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-215">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e7951-215">-SkuTier</span></span>
<span data-ttu-id="e7951-216">A VMSS küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-216">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="e7951-217">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e7951-217">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7951-218">Standard</span><span class="sxs-lookup"><span data-stu-id="e7951-218">Standard</span></span>
- <span data-ttu-id="e7951-219">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="e7951-219">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-220">-Címke</span><span class="sxs-lookup"><span data-stu-id="e7951-220">-Tag</span></span>
<span data-ttu-id="e7951-221">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="e7951-221">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e7951-222">Példa:</span><span class="sxs-lookup"><span data-stu-id="e7951-222">For example:</span></span>

<span data-ttu-id="e7951-223">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="e7951-223">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-224">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="e7951-224">-TimeZone</span></span>
<span data-ttu-id="e7951-225">A Windows operációs rendszerhez használt időzónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-225">Specifies the time zone for Windows OS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-226">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="e7951-226">-UpgradePolicyMode</span></span>
<span data-ttu-id="e7951-227">A méretarányban a virtuális gépekre való frissítés módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-227">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="e7951-228">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e7951-228">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7951-229">Automatikus</span><span class="sxs-lookup"><span data-stu-id="e7951-229">Automatic</span></span>
- <span data-ttu-id="e7951-230">Kézi</span><span class="sxs-lookup"><span data-stu-id="e7951-230">Manual</span></span>
- <span data-ttu-id="e7951-231">Gördülő</span><span class="sxs-lookup"><span data-stu-id="e7951-231">Rolling</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-232">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="e7951-232">-VhdContainer</span></span>
<span data-ttu-id="e7951-233">Annak a tárolónak a tároló URL-címét adja meg, amely a VMSS operációs rendszer lemezének tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="e7951-233">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e7951-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e7951-235">Helyi VMSS-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e7951-235">Specifies a local VMSS object.</span></span>
<span data-ttu-id="e7951-236">VMSS objektum beolvasásához használja az Get-AzVmss parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e7951-236">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="e7951-237">Ez a virtuálisgép-objektum a VMSS frissített állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e7951-237">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-238">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e7951-238">-VMScaleSetName</span></span>
<span data-ttu-id="e7951-239">Annak a VMSS a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e7951-239">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-240">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7951-240">-Confirm</span></span>
<span data-ttu-id="e7951-241">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7951-241">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-242">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7951-242">-WhatIf</span></span>
<span data-ttu-id="e7951-243">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e7951-243">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e7951-244">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7951-244">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7951-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7951-245">CommonParameters</span></span>
<span data-ttu-id="e7951-246">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7951-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7951-247">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7951-247">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7951-248">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7951-248">INPUTS</span></span>

### <span data-ttu-id="e7951-249">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e7951-249">VirtualMachineScaleSet</span></span>
<span data-ttu-id="e7951-250">A ' VirtualMachineScaleSet ' paraméter az "VirtualMachineScaleSet" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e7951-250">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="e7951-251">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7951-251">OUTPUTS</span></span>

### <span data-ttu-id="e7951-252">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e7951-252">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e7951-253">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7951-253">NOTES</span></span>

## <span data-ttu-id="e7951-254">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7951-254">RELATED LINKS</span></span>

[<span data-ttu-id="e7951-255">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e7951-255">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="e7951-256">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="e7951-256">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="e7951-257">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e7951-257">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="e7951-258">Újraindítás – AzVmss</span><span class="sxs-lookup"><span data-stu-id="e7951-258">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="e7951-259">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e7951-259">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="e7951-260">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e7951-260">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="e7951-261">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e7951-261">Stop-AzVmss</span></span>](./Stop-AzVmss.md)



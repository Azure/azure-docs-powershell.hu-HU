---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: d2ecc5799319dcbc9b2e3710c186ffd7ebc09c64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499651"
---
# <span data-ttu-id="25324-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="25324-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="25324-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25324-102">SYNOPSIS</span></span>
<span data-ttu-id="25324-103">Frissíti egy VMSS állapotát.</span><span class="sxs-lookup"><span data-stu-id="25324-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25324-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25324-104">SYNTAX</span></span>

### <span data-ttu-id="25324-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25324-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>]
 [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>]
 [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25324-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="25324-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>]
 -IdentityType <ResourceIdentityType> [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25324-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="25324-107">DESCRIPTION</span></span>
<span data-ttu-id="25324-108">Az **Update-AzureRmVmss** parancsmag a virtuálisgép-készlet (VMSS) állapotát egy helyi VMSS objektum állapotára frissíti.</span><span class="sxs-lookup"><span data-stu-id="25324-108">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="25324-109">Példák</span><span class="sxs-lookup"><span data-stu-id="25324-109">EXAMPLES</span></span>

### <span data-ttu-id="25324-110">Példa 1: egy VMSS állapotának frissítése egy helyi VMSS-objektum állapotával.</span><span class="sxs-lookup"><span data-stu-id="25324-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="25324-111">Ez a parancs frissíti a Group001 nevű VMSS001 nevű VMSS állapotát egy helyi VMSS objektum állapotához, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="25324-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="25324-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25324-112">PARAMETERS</span></span>

### <span data-ttu-id="25324-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25324-113">-AsJob</span></span>
<span data-ttu-id="25324-114">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="25324-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="25324-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="25324-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="25324-116">Azt adja meg, hogy az operációs rendszer frissítéseit a program automatikusan alkalmazza-e a méretarányos példányokra, ha a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="25324-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="25324-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="25324-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="25324-118">A rendszerindítási diagnosztikát engedélyezni kell-e a virtuálisgép-méretarány beállításakor.</span><span class="sxs-lookup"><span data-stu-id="25324-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="25324-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="25324-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="25324-120">A konzol kimenetének és képernyőképének elhelyezéséhez használandó tárolási fiók URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="25324-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="25324-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="25324-121">-CustomData</span></span>
<span data-ttu-id="25324-122">Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="25324-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="25324-123">Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.</span><span class="sxs-lookup"><span data-stu-id="25324-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="25324-124">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="25324-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="25324-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25324-125">-DefaultProfile</span></span>
<span data-ttu-id="25324-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25324-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25324-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="25324-127">-DisableAutoRollback</span></span>
<span data-ttu-id="25324-128">Automatikus visszagörgetés letiltása az automatikus operációs rendszer frissítési házirendjében</span><span class="sxs-lookup"><span data-stu-id="25324-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="25324-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="25324-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="25324-130">Jelzi, hogy ez a parancsmag letiltja a Linux operációs rendszerhez használt jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="25324-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="25324-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="25324-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="25324-132">Azt jelzi, hogy a VMSS engedélyezve vannak-e a Windows virtuális gépek az automatikus frissítésekhez.</span><span class="sxs-lookup"><span data-stu-id="25324-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="25324-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="25324-133">-IdentityId</span></span>
<span data-ttu-id="25324-134">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="25324-135">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="25324-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="25324-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="25324-136">-IdentityType</span></span>
<span data-ttu-id="25324-137">A virtuálisgép-készlethez használt identitás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="25324-138">Az "SystemAssignedUserAssigned" típus egy implicit módon létrehozott identitást és egy, a felhasználó által kiosztott identitást tartalmazó készletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="25324-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="25324-139">Ha a virtuálisgép-készletből eltávolítja az identitásokat, a "nincs" típust kell választania.</span><span class="sxs-lookup"><span data-stu-id="25324-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="25324-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="25324-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25324-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="25324-141">SystemAssigned</span></span>
- <span data-ttu-id="25324-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="25324-142">UserAssigned</span></span>
- <span data-ttu-id="25324-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="25324-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="25324-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="25324-144">None</span></span>

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

### <span data-ttu-id="25324-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="25324-145">-ImageReferenceId</span></span>
<span data-ttu-id="25324-146">A kép hivatkozási AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="25324-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="25324-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="25324-148">A Virtual Machine Image (VMImage) ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="25324-149">Képajánlat beolvasásához használja az Get-AzureRmVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="25324-149">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="25324-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="25324-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="25324-151">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="25324-152">Publisher beolvasásához használja az Get-AzureRmVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="25324-152">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="25324-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="25324-153">-ImageReferenceSku</span></span>
<span data-ttu-id="25324-154">A VMImage SKU-ot adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="25324-155">A SKU beolvasásához használja az Get-AzureRmVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="25324-155">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="25324-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="25324-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="25324-157">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="25324-158">A legújabb verzió használatához adjon meg egy új értéket az adott verzió helyett.</span><span class="sxs-lookup"><span data-stu-id="25324-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="25324-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="25324-159">-ImageUri</span></span>
<span data-ttu-id="25324-160">A felhasználói kép blob-URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="25324-161">A VMSS létrehozza az operációs rendszer lemezét a felhasználói kép ugyanazon tárolójában.</span><span class="sxs-lookup"><span data-stu-id="25324-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="25324-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="25324-162">-LicenseType</span></span>
<span data-ttu-id="25324-163">Adja meg azt a licenc-típust, amely a licencek használati forgatókönyvét hozza meg.</span><span class="sxs-lookup"><span data-stu-id="25324-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="25324-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="25324-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="25324-165">A felügyelt lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="25324-166">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="25324-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25324-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="25324-167">StandardLRS</span></span>
- <span data-ttu-id="25324-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="25324-168">PremiumLRS</span></span>

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

### <span data-ttu-id="25324-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="25324-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="25324-170">Annak a virtuális gép-példányoknak a maximális százalékos aránya, amelyet a rendszer egy kötegben a folyamatos frissítéssel egyidejűleg frissít.</span><span class="sxs-lookup"><span data-stu-id="25324-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="25324-171">Mivel az előző vagy a jövőbeli kötegekben ez a maximális, egészségtelen előfordulás, a kötegben lévő példányok százalékos arányát a nagyobb megbízhatóság érdekében is csökkentheti.</span><span class="sxs-lookup"><span data-stu-id="25324-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="25324-172">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="25324-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="25324-173">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="25324-173">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="25324-174">A teljes virtuálisgép-példányok maximális százalékos aránya a készletben, amely egyidejű egészségtelen lehet, akár a frissítés során, akár a virtuálisgép-állapot ellenőrzésekor, a frissítés megszakítása előtt.</span><span class="sxs-lookup"><span data-stu-id="25324-174">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="25324-175">Ezt a korlátozást a program minden köteg kezdése előtt ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="25324-175">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="25324-176">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="25324-176">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="25324-177">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="25324-177">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="25324-178">A frissített virtuálisgép-példányok maximális százaléka, amely egészségtelen állapotban található.</span><span class="sxs-lookup"><span data-stu-id="25324-178">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="25324-179">Ez az ellenőrzés minden köteg frissítésekor megtörténik.</span><span class="sxs-lookup"><span data-stu-id="25324-179">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="25324-180">Ha a százalékos érték túllépve, a gördülési frissítés leáll.</span><span class="sxs-lookup"><span data-stu-id="25324-180">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="25324-181">Ha az érték nincs megadva, az érték 20 értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="25324-181">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="25324-182">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="25324-182">-OsDiskCaching</span></span>
<span data-ttu-id="25324-183">Az operációs rendszer lemezének gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-183">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="25324-184">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="25324-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25324-185">Nincs</span><span class="sxs-lookup"><span data-stu-id="25324-185">None</span></span>
- <span data-ttu-id="25324-186">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="25324-186">ReadOnly</span></span>
- <span data-ttu-id="25324-187">ReadWrite: az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="25324-187">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="25324-188">Ha módosítja a gyorsítótár értékét, akkor a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="25324-188">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="25324-189">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="25324-189">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="25324-190">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="25324-190">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="25324-191">Megadja, hogy az operációs rendszer merevlemezén engedélyezni vagy tiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="25324-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="25324-192">-Túlszabályozás</span><span class="sxs-lookup"><span data-stu-id="25324-192">-Overprovision</span></span>
<span data-ttu-id="25324-193">Azt jelzi, hogy a parancsmag túla VMSS-e.</span><span class="sxs-lookup"><span data-stu-id="25324-193">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="25324-194">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="25324-194">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="25324-195">Az egy kötegben lévő összes virtuális gép frissítésének várakozási ideje, és a következő köteg indítása.</span><span class="sxs-lookup"><span data-stu-id="25324-195">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="25324-196">Az időtartamot az ISO 8601-formátumban kell megadni.</span><span class="sxs-lookup"><span data-stu-id="25324-196">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="25324-197">Az alapértelmezett érték a 0 másodperc (PT0S).</span><span class="sxs-lookup"><span data-stu-id="25324-197">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="25324-198">-PlanName</span><span class="sxs-lookup"><span data-stu-id="25324-198">-PlanName</span></span>
<span data-ttu-id="25324-199">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-199">Specifies the plan name.</span></span>

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

### <span data-ttu-id="25324-200">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="25324-200">-PlanProduct</span></span>
<span data-ttu-id="25324-201">A csomag terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-201">Specifies the plan product.</span></span>

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

### <span data-ttu-id="25324-202">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="25324-202">-PlanPromotionCode</span></span>
<span data-ttu-id="25324-203">A csomag-előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-203">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="25324-204">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="25324-204">-PlanPublisher</span></span>
<span data-ttu-id="25324-205">A terv közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-205">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="25324-206">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="25324-206">-ProvisionVMAgent</span></span>
<span data-ttu-id="25324-207">Azt jelzi, hogy a virtuális gép ügynöknek kiépítve kell-e lennie a Windows virtuális gépeken a VMSS.</span><span class="sxs-lookup"><span data-stu-id="25324-207">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="25324-208">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25324-208">-ResourceGroupName</span></span>
<span data-ttu-id="25324-209">Annak a csoportnak a neve, amelyhez a VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="25324-209">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25324-210">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="25324-210">-SinglePlacementGroup</span></span>
<span data-ttu-id="25324-211">Az egyetlen elhelyezés csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-211">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="25324-212">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="25324-212">-SkuCapacity</span></span>
<span data-ttu-id="25324-213">A VMSS példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-213">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="25324-214">-SkuName</span><span class="sxs-lookup"><span data-stu-id="25324-214">-SkuName</span></span>
<span data-ttu-id="25324-215">A VMSS összes példányának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-215">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="25324-216">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="25324-216">-SkuTier</span></span>
<span data-ttu-id="25324-217">A VMSS küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-217">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="25324-218">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="25324-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25324-219">Standard</span><span class="sxs-lookup"><span data-stu-id="25324-219">Standard</span></span>
- <span data-ttu-id="25324-220">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="25324-220">Basic</span></span>

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

### <span data-ttu-id="25324-221">-Címke</span><span class="sxs-lookup"><span data-stu-id="25324-221">-Tag</span></span>
<span data-ttu-id="25324-222">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="25324-222">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="25324-223">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="25324-223">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="25324-224">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="25324-224">-TimeZone</span></span>
<span data-ttu-id="25324-225">A Windows operációs rendszerhez használt időzónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-225">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="25324-226">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="25324-226">-UltraSSDEnabled</span></span>
<span data-ttu-id="25324-227">A jelölő, amely lehetővé teszi vagy tiltja egy vagy több felügyelt adatlemez egy vagy több felügyelt adatlemezének UltraSSD_LRS tárolási fiók típusát a virtuálisgép-készlet beállításakor.</span><span class="sxs-lookup"><span data-stu-id="25324-227">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="25324-228">A felügyelt lemezek tároló típusú UltraSSD_LRS csak akkor vehetők fel a VMSS, ha a tulajdonság engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="25324-228">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="25324-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="25324-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="25324-230">A méretarányban a virtuális gépekre való frissítés módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="25324-230">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="25324-231">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="25324-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25324-232">Automatikus</span><span class="sxs-lookup"><span data-stu-id="25324-232">Automatic</span></span>
- <span data-ttu-id="25324-233">Kézi</span><span class="sxs-lookup"><span data-stu-id="25324-233">Manual</span></span>
- <span data-ttu-id="25324-234">Gördülő</span><span class="sxs-lookup"><span data-stu-id="25324-234">Rolling</span></span>

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

### <span data-ttu-id="25324-235">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="25324-235">-VhdContainer</span></span>
<span data-ttu-id="25324-236">Annak a tárolónak a tároló URL-címét adja meg, amely a VMSS operációs rendszer lemezének tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="25324-236">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="25324-237">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="25324-237">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="25324-238">Helyi VMSS-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="25324-238">Specifies a local VMSS object.</span></span>
<span data-ttu-id="25324-239">VMSS objektum beolvasásához használja az Get-AzureRmVmss parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="25324-239">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="25324-240">Ez a virtuálisgép-objektum a VMSS frissített állapotát tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="25324-240">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25324-241">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="25324-241">-VMScaleSetName</span></span>
<span data-ttu-id="25324-242">Annak a VMSS a nevét adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="25324-242">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25324-243">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="25324-243">-Confirm</span></span>
<span data-ttu-id="25324-244">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="25324-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25324-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25324-245">-WhatIf</span></span>
<span data-ttu-id="25324-246">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="25324-246">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25324-247">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25324-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25324-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25324-248">CommonParameters</span></span>
<span data-ttu-id="25324-249">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25324-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25324-250">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25324-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25324-251">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25324-251">INPUTS</span></span>

### <span data-ttu-id="25324-252">System. String</span><span class="sxs-lookup"><span data-stu-id="25324-252">System.String</span></span>

### <span data-ttu-id="25324-253">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="25324-253">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="25324-254">Paraméterek: VirtualMachineScaleSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="25324-254">Parameters: VirtualMachineScaleSet (ByValue)</span></span>

## <span data-ttu-id="25324-255">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25324-255">OUTPUTS</span></span>

### <span data-ttu-id="25324-256">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="25324-256">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="25324-257">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25324-257">NOTES</span></span>

## <span data-ttu-id="25324-258">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25324-258">RELATED LINKS</span></span>

[<span data-ttu-id="25324-259">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="25324-259">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="25324-260">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="25324-260">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="25324-261">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="25324-261">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="25324-262">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="25324-262">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="25324-263">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="25324-263">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="25324-264">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="25324-264">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="25324-265">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="25324-265">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)



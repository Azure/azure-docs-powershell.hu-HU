---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: c407ce7147d3eb175fc181b76b140605e463d9a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844450"
---
# <span data-ttu-id="91479-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="91479-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="91479-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91479-102">SYNOPSIS</span></span>
<span data-ttu-id="91479-103">Létrehozza a VMSS konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="91479-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="91479-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91479-104">SYNTAX</span></span>

### <span data-ttu-id="91479-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91479-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91479-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="91479-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91479-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="91479-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91479-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="91479-108">DESCRIPTION</span></span>
<span data-ttu-id="91479-109">A **New-AzVmssConfig** parancsmag létrehoz egy konfigurálható helyi Virtual Manager Scale set (VMSS) objektumot.</span><span class="sxs-lookup"><span data-stu-id="91479-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="91479-110">A VMSS objektum konfigurálásához további parancsmagokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="91479-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="91479-111">Ezek a parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="91479-111">These cmdlets are:</span></span>

- <span data-ttu-id="91479-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="91479-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="91479-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="91479-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="91479-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="91479-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="91479-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="91479-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="91479-116">Példák</span><span class="sxs-lookup"><span data-stu-id="91479-116">EXAMPLES</span></span>

### <span data-ttu-id="91479-117">Példa 1: VMSS konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="91479-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="91479-118">Ebben a példában egy VMSS-konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="91479-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="91479-119">Az első parancs a **New-AzVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="91479-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="91479-120">A második parancs a **New-AzVmss** parancsmagot használja az első parancsban létrehozott VMSS konfigurációs OBJEKTUMOT használó VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="91479-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="91479-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91479-121">PARAMETERS</span></span>

### <span data-ttu-id="91479-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="91479-122">-AssignIdentity</span></span>
<span data-ttu-id="91479-123">Adja meg a virtuálisgép-készlethez tartozó rendszerhez rendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="91479-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91479-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="91479-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="91479-125">Azt adja meg, hogy az operációs rendszer frissítéseit a program automatikusan alkalmazza-e a méretarányos példányokra, ha a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="91479-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="91479-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="91479-126">-BootDiagnostic</span></span>
<span data-ttu-id="91479-127">A virtuálisgép-készlet indítási diagnosztikai profilját adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: BootDiagnostics
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91479-128">-DefaultProfile</span></span>
<span data-ttu-id="91479-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91479-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91479-130">-Extension (kiterjesztés)</span><span class="sxs-lookup"><span data-stu-id="91479-130">-Extension</span></span>
<span data-ttu-id="91479-131">A VMSS kiegészítő információs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-131">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="91479-132">Ezt az objektumot az **Add-AzVmssExtension** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-132">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-133">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="91479-133">-HealthProbeId</span></span>
<span data-ttu-id="91479-134">A virtuálisgép-készletben lévő példány állapotának meghatározásához használt terheléselosztó szonda AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-134">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="91479-135">A HealthProbeId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}" formában jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="91479-135">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-136">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="91479-136">-IdentityId</span></span>
<span data-ttu-id="91479-137">A virtuálisgép-készlethez társított felhasználói identitások listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-137">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="91479-138">A felhasználói identitás hivatkozásai az űrlapon az "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" típusú erőforrás-azonosítók lesznek.</span><span class="sxs-lookup"><span data-stu-id="91479-138">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-139">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="91479-139">-IdentityType</span></span>
<span data-ttu-id="91479-140">A virtuálisgép-készlethez használt identitás típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-140">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="91479-141">Az "SystemAssignedUserAssigned" típus egy implicit módon létrehozott identitást és egy, a felhasználó által kiosztott identitást tartalmazó készletet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="91479-141">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="91479-142">Ha a virtuálisgép-készletből eltávolítja az identitásokat, a "nincs" típust kell választania.</span><span class="sxs-lookup"><span data-stu-id="91479-142">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="91479-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="91479-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91479-144">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="91479-144">SystemAssigned</span></span>
- <span data-ttu-id="91479-145">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="91479-145">UserAssigned</span></span>
- <span data-ttu-id="91479-146">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="91479-146">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="91479-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="91479-147">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="91479-148">-LicenseType</span></span>
<span data-ttu-id="91479-149">Adja meg azt a licenc-típust, amely a licencek használati forgatókönyvét hozza meg.</span><span class="sxs-lookup"><span data-stu-id="91479-149">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-150">-Hely</span><span class="sxs-lookup"><span data-stu-id="91479-150">-Location</span></span>
<span data-ttu-id="91479-151">Az az Azure-hely, ahol létrejön a VMSS.</span><span class="sxs-lookup"><span data-stu-id="91479-151">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-152">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="91479-152">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="91479-153">Megadja a VMSS konfigurációjának hálózati tulajdonságait tartalmazó hálózati profil objektumot.</span><span class="sxs-lookup"><span data-stu-id="91479-153">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="91479-154">Ezt az objektumot az **Add-AzVmssNetworkInterfaceConfiguration** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-154">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-155">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="91479-155">-OsProfile</span></span>
<span data-ttu-id="91479-156">Annak az operációs rendszernek a profil-objektumát adja meg, amely az VMSS-konfiguráció operációs rendszerének tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="91479-156">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="91479-157">Az objektum beállításához a **set-AzVmssOsProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="91479-157">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-158">-Túlszabályozás</span><span class="sxs-lookup"><span data-stu-id="91479-158">-Overprovision</span></span>
<span data-ttu-id="91479-159">Azt jelzi, hogy a parancsmag túla VMSS-e.</span><span class="sxs-lookup"><span data-stu-id="91479-159">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-160">-PlanName</span><span class="sxs-lookup"><span data-stu-id="91479-160">-PlanName</span></span>
<span data-ttu-id="91479-161">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-161">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-162">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="91479-162">-PlanProduct</span></span>
<span data-ttu-id="91479-163">A csomag terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-163">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-164">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="91479-164">-PlanPromotionCode</span></span>
<span data-ttu-id="91479-165">A csomag-előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-165">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-166">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="91479-166">-PlanPublisher</span></span>
<span data-ttu-id="91479-167">A terv közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-167">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-168">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="91479-168">-Priority</span></span>
<span data-ttu-id="91479-169">A beállított méretarányban a virtuális gépek prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-169">Specifies the priority for the virtual machines in the scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-170">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="91479-170">-RollingUpgradePolicy</span></span>
<span data-ttu-id="91479-171">A folyamatos frissítés szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-171">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: RollingUpgradePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-172">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="91479-172">-SinglePlacementGroup</span></span>
<span data-ttu-id="91479-173">Az egyetlen elhelyezés csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-173">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-174">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="91479-174">-SkuCapacity</span></span>
<span data-ttu-id="91479-175">A VMSS példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-175">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-176">-SkuName</span><span class="sxs-lookup"><span data-stu-id="91479-176">-SkuName</span></span>
<span data-ttu-id="91479-177">A VMSS összes példányának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-177">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-178">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="91479-178">-SkuTier</span></span>
<span data-ttu-id="91479-179">A VMSS küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-179">Specifies the tier of VMSS.</span></span> <span data-ttu-id="91479-180">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="91479-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91479-181">Standard</span><span class="sxs-lookup"><span data-stu-id="91479-181">Standard</span></span>
- <span data-ttu-id="91479-182">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="91479-182">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-183">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="91479-183">-StorageProfile</span></span>
<span data-ttu-id="91479-184">A VMSS-konfigurációban a lemez tulajdonságait tartalmazó Storage profil objektum.</span><span class="sxs-lookup"><span data-stu-id="91479-184">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="91479-185">Az objektum beállításához a **set-AzVmssStorageProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="91479-185">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-186">-Címke</span><span class="sxs-lookup"><span data-stu-id="91479-186">-Tag</span></span>
<span data-ttu-id="91479-187">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="91479-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="91479-188">Példa:</span><span class="sxs-lookup"><span data-stu-id="91479-188">For example:</span></span>

<span data-ttu-id="91479-189">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="91479-189">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-190">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="91479-190">-UpgradePolicyMode</span></span>
<span data-ttu-id="91479-191">A méretarányban a virtuális gépekre való frissítés módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-191">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="91479-192">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="91479-192">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91479-193">Automatikus</span><span class="sxs-lookup"><span data-stu-id="91479-193">Automatic</span></span>
- <span data-ttu-id="91479-194">Kézi</span><span class="sxs-lookup"><span data-stu-id="91479-194">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-195">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="91479-195">-Zone</span></span>
<span data-ttu-id="91479-196">A virtuálisgép-készlethez tartozó zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="91479-196">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91479-197">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="91479-197">-Confirm</span></span>
<span data-ttu-id="91479-198">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91479-198">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91479-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91479-199">-WhatIf</span></span>
<span data-ttu-id="91479-200">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="91479-200">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91479-201">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91479-201">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91479-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91479-202">CommonParameters</span></span>
<span data-ttu-id="91479-203">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91479-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91479-204">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91479-204">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91479-205">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91479-205">INPUTS</span></span>

### <span data-ttu-id="91479-206">Nincs</span><span class="sxs-lookup"><span data-stu-id="91479-206">None</span></span>
<span data-ttu-id="91479-207">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="91479-207">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="91479-208">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91479-208">OUTPUTS</span></span>

### <span data-ttu-id="91479-209">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="91479-209">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="91479-210">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91479-210">NOTES</span></span>

## <span data-ttu-id="91479-211">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91479-211">RELATED LINKS</span></span>

[<span data-ttu-id="91479-212">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="91479-212">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="91479-213">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="91479-213">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="91479-214">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="91479-214">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="91479-215">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="91479-215">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="91479-216">Új – AzVmss</span><span class="sxs-lookup"><span data-stu-id="91479-216">New-AzVmss</span></span>](./New-AzVmss.md)

---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 3229f1e09cca1b32b62e5b7233806b20ed8ed78e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680282"
---
# <span data-ttu-id="51997-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="51997-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="51997-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51997-102">SYNOPSIS</span></span>
<span data-ttu-id="51997-103">Létrehozza a VMSS konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="51997-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51997-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51997-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-AssignIdentity]
 [-IdentityType <ResourceIdentityType>] [-RecoveryPolicyMode <RecoveryMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51997-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="51997-105">DESCRIPTION</span></span>
<span data-ttu-id="51997-106">A **New-AzureRmVmssConfig** parancsmag létrehoz egy konfigurálható helyi Virtual Manager Scale set (VMSS) objektumot.</span><span class="sxs-lookup"><span data-stu-id="51997-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="51997-107">A VMSS objektum konfigurálásához további parancsmagokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="51997-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="51997-108">Ezek a parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="51997-108">These cmdlets are:</span></span>

- <span data-ttu-id="51997-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="51997-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="51997-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="51997-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="51997-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="51997-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="51997-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="51997-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="51997-113">Példák</span><span class="sxs-lookup"><span data-stu-id="51997-113">EXAMPLES</span></span>

### <span data-ttu-id="51997-114">Példa 1: VMSS konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="51997-114">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="51997-115">Ebben a példában egy VMSS-konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="51997-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="51997-116">Az első parancs a **New-AzureRmVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="51997-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="51997-117">A második parancs a **New-AzureRmVmss** parancsmagot használja az első parancsban létrehozott VMSS konfigurációs OBJEKTUMOT használó VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="51997-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="51997-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51997-118">PARAMETERS</span></span>

### <span data-ttu-id="51997-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="51997-119">-AssignIdentity</span></span>
<span data-ttu-id="51997-120">Adja meg a virtuálisgép-készlethez tartozó rendszerhez rendelt identitást.</span><span class="sxs-lookup"><span data-stu-id="51997-120">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51997-121">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="51997-121">-AutoOSUpgrade</span></span>
<span data-ttu-id="51997-122">Azt adja meg, hogy az operációs rendszer frissítéseit a program automatikusan alkalmazza-e a méretarányos példányokra, ha a kép újabb verziója elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="51997-122">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51997-123">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="51997-123">-BootDiagnostic</span></span>
<span data-ttu-id="51997-124">A virtuálisgép-készlet indítási diagnosztikai profilját adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-124">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="51997-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51997-125">-DefaultProfile</span></span>
<span data-ttu-id="51997-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51997-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51997-127">-Extension (kiterjesztés)</span><span class="sxs-lookup"><span data-stu-id="51997-127">-Extension</span></span>
<span data-ttu-id="51997-128">A VMSS kiegészítő információs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-128">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="51997-129">Ezt az objektumot az **Add-AzureRmVmssExtension** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-129">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="51997-130">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="51997-130">-HealthProbeId</span></span>
<span data-ttu-id="51997-131">Adja meg a virtuálisgép-készletben lévő példány állapotának meghatározásához használt terheléselosztó szonda AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="51997-131">Specify the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span> <span data-ttu-id="51997-132">A HealthProbeId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}" formában jelenik meg.</span><span class="sxs-lookup"><span data-stu-id="51997-132">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="51997-133">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="51997-133">-IdentityType</span></span>
<span data-ttu-id="51997-134">Adja meg a virtuálisgép-készlet azonosítóját, ha be van állítva.</span><span class="sxs-lookup"><span data-stu-id="51997-134">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51997-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="51997-135">-LicenseType</span></span>
<span data-ttu-id="51997-136">Adja meg azt a licenc-típust, amely a licencek használati forgatókönyvét hozza meg.</span><span class="sxs-lookup"><span data-stu-id="51997-136">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="51997-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="51997-137">-Location</span></span>
<span data-ttu-id="51997-138">Az az Azure-hely, ahol létrejön a VMSS.</span><span class="sxs-lookup"><span data-stu-id="51997-138">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="51997-139">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="51997-139">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="51997-140">Megadja a VMSS konfigurációjának hálózati tulajdonságait tartalmazó hálózati profil objektumot.</span><span class="sxs-lookup"><span data-stu-id="51997-140">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="51997-141">Ezt az objektumot az **Add-AzureRmVmssNetworkInterfaceConfiguration** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-141">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="51997-142">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="51997-142">-OsProfile</span></span>
<span data-ttu-id="51997-143">Annak az operációs rendszernek a profil-objektumát adja meg, amely az VMSS-konfiguráció operációs rendszerének tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="51997-143">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="51997-144">Az objektum beállításához a **set-AzureRmVmssOsProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="51997-144">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="51997-145">-Túlszabályozás</span><span class="sxs-lookup"><span data-stu-id="51997-145">-Overprovision</span></span>
<span data-ttu-id="51997-146">Azt jelzi, hogy a parancsmag túla VMSS-e.</span><span class="sxs-lookup"><span data-stu-id="51997-146">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="51997-147">-PlanName</span><span class="sxs-lookup"><span data-stu-id="51997-147">-PlanName</span></span>
<span data-ttu-id="51997-148">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-148">Specifies the plan name.</span></span>

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

### <span data-ttu-id="51997-149">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="51997-149">-PlanProduct</span></span>
<span data-ttu-id="51997-150">A csomag terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-150">Specifies the plan product.</span></span>

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

### <span data-ttu-id="51997-151">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="51997-151">-PlanPromotionCode</span></span>
<span data-ttu-id="51997-152">A csomag-előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-152">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="51997-153">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="51997-153">-PlanPublisher</span></span>
<span data-ttu-id="51997-154">A terv közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-154">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="51997-155">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="51997-155">-RecoveryPolicyMode</span></span>
<span data-ttu-id="51997-156">Adja meg a helyreállítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="51997-156">Specify the recovery policy.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Compute.Automation.RecoveryMode]
Parameter Sets: (All)
Aliases: 
Accepted values: None, OverProvision, Reprovision

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51997-157">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="51997-157">-RollingUpgradePolicy</span></span>
<span data-ttu-id="51997-158">A folyamatos frissítés szabályát adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-158">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="51997-159">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="51997-159">-SinglePlacementGroup</span></span>
<span data-ttu-id="51997-160">Az egyetlen elhelyezés csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-160">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="51997-161">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="51997-161">-SkuCapacity</span></span>
<span data-ttu-id="51997-162">A VMSS példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-162">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51997-163">-SkuName</span><span class="sxs-lookup"><span data-stu-id="51997-163">-SkuName</span></span>
<span data-ttu-id="51997-164">A VMSS összes példányának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-164">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="51997-165">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="51997-165">-SkuTier</span></span>
<span data-ttu-id="51997-166">A VMSS küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-166">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="51997-167">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="51997-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51997-168">Standard</span><span class="sxs-lookup"><span data-stu-id="51997-168">Standard</span></span>
- <span data-ttu-id="51997-169">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="51997-169">Basic</span></span>

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

### <span data-ttu-id="51997-170">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="51997-170">-StorageProfile</span></span>
<span data-ttu-id="51997-171">A VMSS-konfigurációban a lemez tulajdonságait tartalmazó Storage profil objektum.</span><span class="sxs-lookup"><span data-stu-id="51997-171">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="51997-172">Az objektum beállításához a **set-AzureRmVmssStorageProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="51997-172">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="51997-173">-Címke</span><span class="sxs-lookup"><span data-stu-id="51997-173">-Tag</span></span>
<span data-ttu-id="51997-174">A VMSS hozzárendelendő címkéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-174">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="51997-175">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="51997-175">-UpgradePolicyMode</span></span>
<span data-ttu-id="51997-176">A méretarányban a virtuális gépekre való frissítés módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-176">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="51997-177">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="51997-177">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51997-178">Automatikus</span><span class="sxs-lookup"><span data-stu-id="51997-178">Automatic</span></span>
- <span data-ttu-id="51997-179">Kézi</span><span class="sxs-lookup"><span data-stu-id="51997-179">Manual</span></span>

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

### <span data-ttu-id="51997-180">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="51997-180">-Zone</span></span>
<span data-ttu-id="51997-181">A virtuálisgép-készlethez tartozó zóna listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="51997-181">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="51997-182">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51997-182">-Confirm</span></span>
<span data-ttu-id="51997-183">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51997-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51997-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51997-184">-WhatIf</span></span>
<span data-ttu-id="51997-185">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51997-185">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51997-186">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51997-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51997-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51997-187">CommonParameters</span></span>
<span data-ttu-id="51997-188">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51997-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51997-189">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51997-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51997-190">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51997-190">INPUTS</span></span>

## <span data-ttu-id="51997-191">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51997-191">OUTPUTS</span></span>

### <span data-ttu-id="51997-192">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="51997-192">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="51997-193">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51997-193">NOTES</span></span>

## <span data-ttu-id="51997-194">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51997-194">RELATED LINKS</span></span>

[<span data-ttu-id="51997-195">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="51997-195">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="51997-196">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="51997-196">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="51997-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="51997-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="51997-198">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="51997-198">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="51997-199">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="51997-199">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)



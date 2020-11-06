---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 4b87c121368232769672c24bc5005f3a50bfd39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494551"
---
# <span data-ttu-id="8f52c-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8f52c-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="8f52c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f52c-102">SYNOPSIS</span></span>
<span data-ttu-id="8f52c-103">Létrehozza a VMSS konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="8f52c-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f52c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f52c-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-PlanName <String>]
 [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RecoveryPolicyMode <RecoveryMode>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-IdentityType <ResourceIdentityType>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f52c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f52c-105">DESCRIPTION</span></span>
<span data-ttu-id="8f52c-106">A **New-AzureRmVmssConfig** parancsmag létrehoz egy konfigurálható helyi Virtual Manager Scale set (VMSS) objektumot.</span><span class="sxs-lookup"><span data-stu-id="8f52c-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="8f52c-107">A VMSS objektum konfigurálásához további parancsmagokra van szükség.</span><span class="sxs-lookup"><span data-stu-id="8f52c-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="8f52c-108">Ezek a parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="8f52c-108">These cmdlets are:</span></span>

- <span data-ttu-id="8f52c-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="8f52c-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="8f52c-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="8f52c-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="8f52c-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f52c-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="8f52c-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8f52c-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="8f52c-113">Példák</span><span class="sxs-lookup"><span data-stu-id="8f52c-113">EXAMPLES</span></span>

### <span data-ttu-id="8f52c-114">Példa 1: VMSS konfigurációs objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="8f52c-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="8f52c-115">Ebben a példában egy VMSS-konfigurációs objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8f52c-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="8f52c-116">Az első parancs a **New-AzureRmVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8f52c-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="8f52c-117">A második parancs a **New-AzureRmVmss** parancsmagot használja az első parancsban létrehozott VMSS konfigurációs OBJEKTUMOT használó VMSS létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="8f52c-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="8f52c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f52c-118">PARAMETERS</span></span>

### <span data-ttu-id="8f52c-119">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8f52c-119">-BootDiagnostic</span></span>
<span data-ttu-id="8f52c-120">A virtuálisgép-készlet indítási diagnosztikai profilját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-120">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="8f52c-121">-Extension (kiterjesztés)</span><span class="sxs-lookup"><span data-stu-id="8f52c-121">-Extension</span></span>
<span data-ttu-id="8f52c-122">A VMSS kiegészítő információs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-122">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="8f52c-123">Ezt az objektumot az **Add-AzureRmVmssExtension** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-123">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="8f52c-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8f52c-124">-IdentityType</span></span>
<span data-ttu-id="8f52c-125">Adja meg a virtuálisgép-készlet azonosítóját, ha be van állítva.</span><span class="sxs-lookup"><span data-stu-id="8f52c-125">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f52c-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8f52c-126">-LicenseType</span></span>
<span data-ttu-id="8f52c-127">Adja meg azt a licenc-típust, amely a licencek használati forgatókönyvét hozza meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-127">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="8f52c-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="8f52c-128">-Location</span></span>
<span data-ttu-id="8f52c-129">Az az Azure-hely, ahol létrejön a VMSS.</span><span class="sxs-lookup"><span data-stu-id="8f52c-129">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="8f52c-130">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f52c-130">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="8f52c-131">Megadja a VMSS konfigurációjának hálózati tulajdonságait tartalmazó hálózati profil objektumot.</span><span class="sxs-lookup"><span data-stu-id="8f52c-131">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="8f52c-132">Ezt az objektumot az **Add-AzureRmVmssNetworkInterfaceConfiguration** parancsmaggal adhatja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-132">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="8f52c-133">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="8f52c-133">-OsProfile</span></span>
<span data-ttu-id="8f52c-134">Annak az operációs rendszernek a profil-objektumát adja meg, amely az VMSS-konfiguráció operációs rendszerének tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8f52c-134">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="8f52c-135">Az objektum beállításához a **set-AzureRmVmssOsProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="8f52c-135">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="8f52c-136">-Túlszabályozás</span><span class="sxs-lookup"><span data-stu-id="8f52c-136">-Overprovision</span></span>
<span data-ttu-id="8f52c-137">Azt jelzi, hogy a parancsmag túla VMSS-e.</span><span class="sxs-lookup"><span data-stu-id="8f52c-137">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="8f52c-138">-PlanName</span><span class="sxs-lookup"><span data-stu-id="8f52c-138">-PlanName</span></span>
<span data-ttu-id="8f52c-139">A terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-139">Specifies the plan name.</span></span>

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

### <span data-ttu-id="8f52c-140">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="8f52c-140">-PlanProduct</span></span>
<span data-ttu-id="8f52c-141">A csomag terméket adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-141">Specifies the plan product.</span></span>

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

### <span data-ttu-id="8f52c-142">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="8f52c-142">-PlanPromotionCode</span></span>
<span data-ttu-id="8f52c-143">A csomag-előléptetési kódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-143">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="8f52c-144">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="8f52c-144">-PlanPublisher</span></span>
<span data-ttu-id="8f52c-145">A terv közzétevőjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-145">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="8f52c-146">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="8f52c-146">-RecoveryPolicyMode</span></span>
<span data-ttu-id="8f52c-147">Adja meg a helyreállítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="8f52c-147">Specify the recovery policy.</span></span>

```yaml
Type: RecoveryMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f52c-148">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8f52c-148">-SinglePlacementGroup</span></span>
<span data-ttu-id="8f52c-149">Az egyetlen elhelyezés csoportot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-149">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="8f52c-150">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="8f52c-150">-SkuCapacity</span></span>
<span data-ttu-id="8f52c-151">A VMSS példányainak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-151">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f52c-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8f52c-152">-SkuName</span></span>
<span data-ttu-id="8f52c-153">A VMSS összes példányának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-153">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="8f52c-154">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8f52c-154">-SkuTier</span></span>
<span data-ttu-id="8f52c-155">A VMSS küszöbértékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-155">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="8f52c-156">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8f52c-156">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8f52c-157">Standard</span><span class="sxs-lookup"><span data-stu-id="8f52c-157">Standard</span></span>
- <span data-ttu-id="8f52c-158">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="8f52c-158">Basic</span></span>

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

### <span data-ttu-id="8f52c-159">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="8f52c-159">-StorageProfile</span></span>
<span data-ttu-id="8f52c-160">A VMSS-konfigurációban a lemez tulajdonságait tartalmazó Storage profil objektum.</span><span class="sxs-lookup"><span data-stu-id="8f52c-160">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="8f52c-161">Az objektum beállításához a **set-AzureRmVmssStorageProfile** parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="8f52c-161">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="8f52c-162">-Címke</span><span class="sxs-lookup"><span data-stu-id="8f52c-162">-Tag</span></span>
<span data-ttu-id="8f52c-163">A VMSS hozzárendelendő címkéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-163">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="8f52c-164">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="8f52c-164">-UpgradePolicyMode</span></span>
<span data-ttu-id="8f52c-165">A méretarányban a virtuális gépekre való frissítés módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f52c-165">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="8f52c-166">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8f52c-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8f52c-167">Automatikus</span><span class="sxs-lookup"><span data-stu-id="8f52c-167">Automatic</span></span>
- <span data-ttu-id="8f52c-168">Kézi</span><span class="sxs-lookup"><span data-stu-id="8f52c-168">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f52c-169">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f52c-169">-Confirm</span></span>
<span data-ttu-id="8f52c-170">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f52c-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f52c-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f52c-171">-WhatIf</span></span>
<span data-ttu-id="8f52c-172">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f52c-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f52c-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f52c-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f52c-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f52c-174">CommonParameters</span></span>
<span data-ttu-id="8f52c-175">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f52c-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f52c-176">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f52c-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f52c-177">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f52c-177">INPUTS</span></span>

### <span data-ttu-id="8f52c-178">Nincs</span><span class="sxs-lookup"><span data-stu-id="8f52c-178">None</span></span>
<span data-ttu-id="8f52c-179">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8f52c-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f52c-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f52c-180">OUTPUTS</span></span>

### <span data-ttu-id="8f52c-181">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8f52c-181">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8f52c-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f52c-182">NOTES</span></span>

## <span data-ttu-id="8f52c-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f52c-183">RELATED LINKS</span></span>

[<span data-ttu-id="8f52c-184">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="8f52c-184">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="8f52c-185">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="8f52c-185">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="8f52c-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f52c-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="8f52c-187">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8f52c-187">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="8f52c-188">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8f52c-188">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)



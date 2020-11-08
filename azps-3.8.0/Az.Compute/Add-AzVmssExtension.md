---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 87ea9af1980948f28477a9f483b3c6429df98d12
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014898"
---
# <span data-ttu-id="91445-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="91445-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="91445-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91445-102">SYNOPSIS</span></span>
<span data-ttu-id="91445-103">Hozzáad egy bővítményt a VMSS.</span><span class="sxs-lookup"><span data-stu-id="91445-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="91445-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91445-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91445-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="91445-105">DESCRIPTION</span></span>
<span data-ttu-id="91445-106">Az **Add-AzVmssExtension** parancsmag bővítményt ad a virtuálisgép-készlethez (VMSS).</span><span class="sxs-lookup"><span data-stu-id="91445-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="91445-107">Példák</span><span class="sxs-lookup"><span data-stu-id="91445-107">EXAMPLES</span></span>

### <span data-ttu-id="91445-108">1. példa: bővítmény felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="91445-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="91445-109">Ez a parancs bővítményt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="91445-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="91445-110">2. példa: bővítmény felvétele a VMSS beállításokkal és védett beállításokkal</span><span class="sxs-lookup"><span data-stu-id="91445-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="91445-111">Ez a parancs hozzáad egy bővítményt a VMSS, amelyben egy minta bash-parancsfájl van a blob-tárolóban, a védett beállítások párbeszédpanelen adja meg a blob-tároló és a végrehajtható parancsok URL-címét.</span><span class="sxs-lookup"><span data-stu-id="91445-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="91445-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91445-112">PARAMETERS</span></span>

### <span data-ttu-id="91445-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="91445-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="91445-114">Azt jelzi, hogy a kiterjesztési verziót automatikusan egy újabb alverzióra kell-e frissíteni.</span><span class="sxs-lookup"><span data-stu-id="91445-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91445-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91445-115">-DefaultProfile</span></span>
<span data-ttu-id="91445-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91445-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91445-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="91445-117">-ForceUpdateTag</span></span>
<span data-ttu-id="91445-118">Ha egy érték meg van jelenítve, és eltér az előző értéktől, akkor a bővítmény akkor is kénytelen frissülni, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="91445-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="91445-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91445-119">-Name</span></span>
<span data-ttu-id="91445-120">Itt adhatja meg annak a bővítménynek a nevét, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="91445-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="91445-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="91445-121">-ProtectedSetting</span></span>
<span data-ttu-id="91445-122">A bővítmény privát konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="91445-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="91445-123">Ez a parancsmag titkosítja a magánjellegű konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="91445-123">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91445-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="91445-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="91445-125">Azoknak a bővítményeknek a gyűjteménye, amelyekhez ezt a kiterjesztést ki kell kiépíteni.</span><span class="sxs-lookup"><span data-stu-id="91445-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="91445-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="91445-126">-Publisher</span></span>
<span data-ttu-id="91445-127">A bővítmény közzétevőének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91445-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="91445-128">A Publisher olyan nevet ad, amikor a Publisher a bővítményt regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="91445-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="91445-129">Ez a [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) parancsmagot használhatja a közzétevő beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="91445-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91445-130">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="91445-130">-Setting</span></span>
<span data-ttu-id="91445-131">Megadja a kiterjesztéshez tartozó nyilvános konfigurációt karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="91445-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="91445-132">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="91445-132">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91445-133">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="91445-133">-Type</span></span>
<span data-ttu-id="91445-134">A bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="91445-134">Specifies the extension type.</span></span>
<span data-ttu-id="91445-135">A [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) parancsmaggal lekérheti a bővítmény típusát.</span><span class="sxs-lookup"><span data-stu-id="91445-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91445-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="91445-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="91445-137">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="91445-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="91445-138">A [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) parancsmaggal lekérheti a bővítmény verzióját.</span><span class="sxs-lookup"><span data-stu-id="91445-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="91445-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="91445-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="91445-140">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="91445-140">Specify the VMSS object.</span></span>
<span data-ttu-id="91445-141">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="91445-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91445-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="91445-142">-Confirm</span></span>
<span data-ttu-id="91445-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91445-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91445-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91445-144">-WhatIf</span></span>
<span data-ttu-id="91445-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="91445-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91445-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91445-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91445-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91445-147">CommonParameters</span></span>
<span data-ttu-id="91445-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91445-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91445-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="91445-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91445-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91445-150">INPUTS</span></span>

### <span data-ttu-id="91445-151">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="91445-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="91445-152">System. String</span><span class="sxs-lookup"><span data-stu-id="91445-152">System.String</span></span>

### <span data-ttu-id="91445-153">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="91445-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="91445-154">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="91445-154">System.Object</span></span>

## <span data-ttu-id="91445-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91445-155">OUTPUTS</span></span>

### <span data-ttu-id="91445-156">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="91445-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="91445-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91445-157">NOTES</span></span>

## <span data-ttu-id="91445-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91445-158">RELATED LINKS</span></span>

[<span data-ttu-id="91445-159">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="91445-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="91445-160">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="91445-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="91445-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="91445-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="91445-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="91445-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="91445-163">Új – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="91445-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

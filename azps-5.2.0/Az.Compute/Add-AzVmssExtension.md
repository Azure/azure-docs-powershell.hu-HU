---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 87ea9af1980948f28477a9f483b3c6429df98d12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370774"
---
# <span data-ttu-id="36bec-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="36bec-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="36bec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36bec-102">SYNOPSIS</span></span>
<span data-ttu-id="36bec-103">Bővítmény hozzáadása a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="36bec-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="36bec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36bec-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36bec-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36bec-105">DESCRIPTION</span></span>
<span data-ttu-id="36bec-106">Az **Add-AzVmssExtension** parancsmag hozzáad egy bővítményt a virtuális gép mérethalmazhoz (VMSS).</span><span class="sxs-lookup"><span data-stu-id="36bec-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="36bec-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36bec-107">EXAMPLES</span></span>

### <span data-ttu-id="36bec-108">1. példa: Bővítmény hozzáadása a VMSS-hez</span><span class="sxs-lookup"><span data-stu-id="36bec-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="36bec-109">Ez a parancs bővítményt ad a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="36bec-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="36bec-110">2. példa: Bővítmény hozzáadása a VMSS-hez a beállításokkal és a védett beállításokkal</span><span class="sxs-lookup"><span data-stu-id="36bec-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="36bec-111">Ez a parancs hozzáad egy bővítményt a VMSS-hez egy blobtároló minta bash parancsprogrammal, megadja a blobtároló és a végrehajtható parancs URL-címét a beállításokban és a biztonsági hozzáférésben a védett beállításokban.</span><span class="sxs-lookup"><span data-stu-id="36bec-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="36bec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36bec-112">PARAMETERS</span></span>

### <span data-ttu-id="36bec-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="36bec-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="36bec-114">Azt jelzi, hogy a bővítményverzió automatikusan frissül-e egy újabb alverzióra.</span><span class="sxs-lookup"><span data-stu-id="36bec-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="36bec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36bec-115">-DefaultProfile</span></span>
<span data-ttu-id="36bec-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36bec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36bec-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="36bec-117">-ForceUpdateTag</span></span>
<span data-ttu-id="36bec-118">Ha egy megadott érték eltér az előző értéktől, a bővítménykezelőt akkor is frissítenie kell, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="36bec-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="36bec-119">-Name</span><span class="sxs-lookup"><span data-stu-id="36bec-119">-Name</span></span>
<span data-ttu-id="36bec-120">Megadja annak a kiterjesztésnek a nevét, amelybe a parancsmag hozzáadja.</span><span class="sxs-lookup"><span data-stu-id="36bec-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="36bec-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="36bec-121">-ProtectedSetting</span></span>
<span data-ttu-id="36bec-122">A bővítmény magánjellegű konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="36bec-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="36bec-123">Ez a parancsmag titkosítja a privát konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="36bec-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="36bec-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="36bec-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="36bec-125">Azoknak a kiterjesztésneveknek a gyűjteménye, amelyek után ki kellépítenünk ezt a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="36bec-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="36bec-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="36bec-126">-Publisher</span></span>
<span data-ttu-id="36bec-127">A bővítmény közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36bec-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="36bec-128">A közzétevő nevet ad, amikor a közzétevő regisztrál egy bővítményt.</span><span class="sxs-lookup"><span data-stu-id="36bec-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="36bec-129">Ez a [parancsmag a Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) parancsmag használatával tudja behozni a közzétevőt.</span><span class="sxs-lookup"><span data-stu-id="36bec-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="36bec-130">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="36bec-130">-Setting</span></span>
<span data-ttu-id="36bec-131">A bővítmény nyilvános konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="36bec-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="36bec-132">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="36bec-132">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="36bec-133">-Type</span><span class="sxs-lookup"><span data-stu-id="36bec-133">-Type</span></span>
<span data-ttu-id="36bec-134">A bővítmény típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="36bec-134">Specifies the extension type.</span></span>
<span data-ttu-id="36bec-135">A bővítménytípus használhatja a [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="36bec-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="36bec-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="36bec-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="36bec-137">A bővítménynek a virtuális géphez használt verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="36bec-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="36bec-138">A [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) parancsmag használatával le tudja szerezni a bővítmény verzióját.</span><span class="sxs-lookup"><span data-stu-id="36bec-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="36bec-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36bec-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="36bec-140">Adja meg a VMSS-objektumot.</span><span class="sxs-lookup"><span data-stu-id="36bec-140">Specify the VMSS object.</span></span>
<span data-ttu-id="36bec-141">Az objektumot a [New-AzVmssConfig](./New-AzVmssConfig.md) segítségével hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="36bec-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="36bec-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36bec-142">-Confirm</span></span>
<span data-ttu-id="36bec-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="36bec-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36bec-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36bec-144">-WhatIf</span></span>
<span data-ttu-id="36bec-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="36bec-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36bec-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36bec-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36bec-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36bec-147">CommonParameters</span></span>
<span data-ttu-id="36bec-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36bec-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36bec-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36bec-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36bec-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36bec-150">INPUTS</span></span>

### <span data-ttu-id="36bec-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36bec-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="36bec-152">System.String</span><span class="sxs-lookup"><span data-stu-id="36bec-152">System.String</span></span>

### <span data-ttu-id="36bec-153">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="36bec-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="36bec-154">System.Object</span><span class="sxs-lookup"><span data-stu-id="36bec-154">System.Object</span></span>

## <span data-ttu-id="36bec-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36bec-155">OUTPUTS</span></span>

### <span data-ttu-id="36bec-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36bec-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="36bec-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36bec-157">NOTES</span></span>

## <span data-ttu-id="36bec-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36bec-158">RELATED LINKS</span></span>

[<span data-ttu-id="36bec-159">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="36bec-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="36bec-160">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="36bec-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="36bec-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="36bec-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="36bec-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="36bec-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="36bec-163">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="36bec-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

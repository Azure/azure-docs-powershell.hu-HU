---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 774fb61f2394c5634c8415a7a18ce63f4e696a3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938905"
---
# <span data-ttu-id="06ff4-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="06ff4-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="06ff4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="06ff4-103">Bővítmény hozzáadása a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="06ff4-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="06ff4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="06ff4-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06ff4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="06ff4-105">DESCRIPTION</span></span>
<span data-ttu-id="06ff4-106">Az **Add-AzVmssExtension** parancsmag hozzáad egy bővítményt a virtuális gép mérethalmazhoz (VMSS).</span><span class="sxs-lookup"><span data-stu-id="06ff4-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="06ff4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="06ff4-107">EXAMPLES</span></span>

### <span data-ttu-id="06ff4-108">1. példa: Bővítmény hozzáadása a VMSS-hez</span><span class="sxs-lookup"><span data-stu-id="06ff4-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="06ff4-109">Ez a parancs bővítményt ad a VMSS-hez.</span><span class="sxs-lookup"><span data-stu-id="06ff4-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="06ff4-110">2. példa: Bővítmény hozzáadása a VMSS-hez a beállításokkal és a védett beállításokkal</span><span class="sxs-lookup"><span data-stu-id="06ff4-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="06ff4-111">Ez a parancs hozzáad egy bővítményt a VMSS-hez egy blobtároló minta bash parancsprogrammal, megadja a blobtároló és a végrehajtható parancsok URL-címét a beállításokban és a biztonsági hozzáférésben a védett beállításokban.</span><span class="sxs-lookup"><span data-stu-id="06ff4-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="06ff4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06ff4-112">PARAMETERS</span></span>

### <span data-ttu-id="06ff4-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="06ff4-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="06ff4-114">Azt jelzi, hogy a bővítményverziót automatikusan egy újabb alverzióra kell-e frissíteni.</span><span class="sxs-lookup"><span data-stu-id="06ff4-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="06ff4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ff4-115">-DefaultProfile</span></span>
<span data-ttu-id="06ff4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06ff4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06ff4-117">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="06ff4-117">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="06ff4-118">Azt jelzi, hogy a platformnak automatikusan frissítenie kell-e a bővítményt, ha elérhető a bővítmény újabb verziója.</span><span class="sxs-lookup"><span data-stu-id="06ff4-118">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ff4-119">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="06ff4-119">-ForceUpdateTag</span></span>
<span data-ttu-id="06ff4-120">Ha egy megadott érték eltér az előző értéktől, a bővítménykezelőt akkor is frissítenie kell, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="06ff4-120">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="06ff4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="06ff4-121">-Name</span></span>
<span data-ttu-id="06ff4-122">Megadja annak a kiterjesztésnek a nevét, amelybe a parancsmag hozzáadja.</span><span class="sxs-lookup"><span data-stu-id="06ff4-122">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="06ff4-123">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="06ff4-123">-ProtectedSetting</span></span>
<span data-ttu-id="06ff4-124">A bővítmény magánjellegű konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="06ff4-124">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="06ff4-125">Ez a parancsmag titkosítja a privát konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="06ff4-125">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="06ff4-126">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="06ff4-126">-ProvisionAfterExtension</span></span>
<span data-ttu-id="06ff4-127">Azoknak a kiterjesztésneveknek a gyűjteménye, amelyek után ki kellépítenünk ezt a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="06ff4-127">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="06ff4-128">-Publisher</span><span class="sxs-lookup"><span data-stu-id="06ff4-128">-Publisher</span></span>
<span data-ttu-id="06ff4-129">A bővítmény közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06ff4-129">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="06ff4-130">A közzétevő nevet ad, amikor a közzétevő regisztrál egy bővítményt.</span><span class="sxs-lookup"><span data-stu-id="06ff4-130">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="06ff4-131">Ez a [parancsmag a Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) parancsmag használatával tudja behozni a közzétevőt.</span><span class="sxs-lookup"><span data-stu-id="06ff4-131">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="06ff4-132">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="06ff4-132">-Setting</span></span>
<span data-ttu-id="06ff4-133">A bővítmény nyilvános konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="06ff4-133">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="06ff4-134">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="06ff4-134">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="06ff4-135">-Type</span><span class="sxs-lookup"><span data-stu-id="06ff4-135">-Type</span></span>
<span data-ttu-id="06ff4-136">A bővítmény típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="06ff4-136">Specifies the extension type.</span></span>
<span data-ttu-id="06ff4-137">A bővítmény típusát a [Get-AzVMExtensionImageType parancsmag](./Get-AzVMExtensionImageType.md) használatával is le tudja szerezni.</span><span class="sxs-lookup"><span data-stu-id="06ff4-137">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="06ff4-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="06ff4-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="06ff4-139">A bővítménynek a virtuális géphez használt verzióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="06ff4-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="06ff4-140">A [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) parancsmag használatával le tudja szerezni a bővítmény verzióját.</span><span class="sxs-lookup"><span data-stu-id="06ff4-140">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="06ff4-141">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="06ff4-141">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="06ff4-142">Adja meg a VMSS-objektumot.</span><span class="sxs-lookup"><span data-stu-id="06ff4-142">Specify the VMSS object.</span></span>
<span data-ttu-id="06ff4-143">Az objektumot a [New-AzVmssConfig](./New-AzVmssConfig.md) segítségével hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="06ff4-143">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="06ff4-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06ff4-144">-Confirm</span></span>
<span data-ttu-id="06ff4-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="06ff4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06ff4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06ff4-146">-WhatIf</span></span>
<span data-ttu-id="06ff4-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="06ff4-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06ff4-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06ff4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06ff4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ff4-149">CommonParameters</span></span>
<span data-ttu-id="06ff4-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06ff4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ff4-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06ff4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ff4-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06ff4-152">INPUTS</span></span>

### <span data-ttu-id="06ff4-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="06ff4-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="06ff4-154">System.String</span><span class="sxs-lookup"><span data-stu-id="06ff4-154">System.String</span></span>

### <span data-ttu-id="06ff4-155">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="06ff4-155">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="06ff4-156">System.Object</span><span class="sxs-lookup"><span data-stu-id="06ff4-156">System.Object</span></span>

## <span data-ttu-id="06ff4-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06ff4-157">OUTPUTS</span></span>

### <span data-ttu-id="06ff4-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="06ff4-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="06ff4-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="06ff4-159">NOTES</span></span>

## <span data-ttu-id="06ff4-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06ff4-160">RELATED LINKS</span></span>

[<span data-ttu-id="06ff4-161">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="06ff4-161">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="06ff4-162">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="06ff4-162">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="06ff4-163">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="06ff4-163">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="06ff4-164">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="06ff4-164">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="06ff4-165">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="06ff4-165">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

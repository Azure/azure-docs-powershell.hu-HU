---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 97c8824bca395ddd8fb23ebb4750ab35931c5d51
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844710"
---
# <span data-ttu-id="54252-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="54252-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="54252-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54252-102">SYNOPSIS</span></span>
<span data-ttu-id="54252-103">Hozzáad egy bővítményt a VMSS.</span><span class="sxs-lookup"><span data-stu-id="54252-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="54252-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54252-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54252-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="54252-105">DESCRIPTION</span></span>
<span data-ttu-id="54252-106">Az **Add-AzVmssExtension** parancsmag bővítményt ad a virtuálisgép-készlethez (VMSS).</span><span class="sxs-lookup"><span data-stu-id="54252-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="54252-107">Példák</span><span class="sxs-lookup"><span data-stu-id="54252-107">EXAMPLES</span></span>

### <span data-ttu-id="54252-108">1. példa: bővítmény felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="54252-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="54252-109">Ez a parancs bővítményt ad a VMMS.</span><span class="sxs-lookup"><span data-stu-id="54252-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="54252-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54252-110">PARAMETERS</span></span>

### <span data-ttu-id="54252-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="54252-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="54252-112">Azt jelzi, hogy a kiterjesztési verziót automatikusan egy újabb alverzióra kell-e frissíteni.</span><span class="sxs-lookup"><span data-stu-id="54252-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54252-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54252-113">-DefaultProfile</span></span>
<span data-ttu-id="54252-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54252-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54252-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="54252-115">-ForceUpdateTag</span></span>
<span data-ttu-id="54252-116">Ha egy érték meg van jelenítve, és eltér az előző értéktől, akkor a bővítmény akkor is kénytelen frissülni, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="54252-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="54252-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="54252-117">-Name</span></span>
<span data-ttu-id="54252-118">Itt adhatja meg annak a bővítménynek a nevét, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="54252-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="54252-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="54252-119">-ProtectedSetting</span></span>
<span data-ttu-id="54252-120">A bővítmény privát konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="54252-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="54252-121">Ez a parancsmag titkosítja a magánjellegű konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="54252-121">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54252-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="54252-122">-Publisher</span></span>
<span data-ttu-id="54252-123">A bővítmény közzétevőének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54252-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="54252-124">A Publisher olyan nevet ad, amikor a Publisher a bővítményt regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="54252-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="54252-125">Ez a [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) parancsmagot használhatja a közzétevő beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="54252-125">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54252-126">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="54252-126">-Setting</span></span>
<span data-ttu-id="54252-127">Megadja a kiterjesztéshez tartozó nyilvános konfigurációt karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="54252-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="54252-128">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="54252-128">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54252-129">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="54252-129">-Type</span></span>
<span data-ttu-id="54252-130">A bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="54252-130">Specifies the extension type.</span></span>
<span data-ttu-id="54252-131">A [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) parancsmaggal lekérheti a bővítmény típusát.</span><span class="sxs-lookup"><span data-stu-id="54252-131">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54252-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="54252-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="54252-133">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="54252-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="54252-134">A [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) parancsmaggal lekérheti a bővítmény verzióját.</span><span class="sxs-lookup"><span data-stu-id="54252-134">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="54252-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="54252-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="54252-136">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="54252-136">Specify the VMSS object.</span></span>
<span data-ttu-id="54252-137">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="54252-137">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54252-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54252-138">-Confirm</span></span>
<span data-ttu-id="54252-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54252-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54252-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54252-140">-WhatIf</span></span>
<span data-ttu-id="54252-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54252-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54252-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54252-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54252-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54252-143">CommonParameters</span></span>
<span data-ttu-id="54252-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54252-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54252-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54252-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54252-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54252-146">INPUTS</span></span>

### <span data-ttu-id="54252-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="54252-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="54252-148">A ' VirtualMachineScaleSet ' paraméter az "VirtualMachineScaleSet" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="54252-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="54252-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54252-149">OUTPUTS</span></span>

###  
<span data-ttu-id="54252-150">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="54252-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="54252-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54252-151">NOTES</span></span>

## <span data-ttu-id="54252-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54252-152">RELATED LINKS</span></span>

[<span data-ttu-id="54252-153">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="54252-153">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="54252-154">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="54252-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="54252-155">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="54252-155">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="54252-156">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="54252-156">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="54252-157">Új – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="54252-157">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

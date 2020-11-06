---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: fbf9d8c38c10465c565e40a284171b3232ba2949
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501927"
---
# <span data-ttu-id="f3795-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f3795-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="f3795-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3795-102">SYNOPSIS</span></span>
<span data-ttu-id="f3795-103">Hozzáad egy bővítményt a VMSS.</span><span class="sxs-lookup"><span data-stu-id="f3795-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3795-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3795-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3795-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3795-105">DESCRIPTION</span></span>
<span data-ttu-id="f3795-106">Az **Add-AzureRmVmssExtension** parancsmag bővítményt ad a virtuálisgép-készlethez (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f3795-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f3795-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f3795-107">EXAMPLES</span></span>

### <span data-ttu-id="f3795-108">1. példa: bővítmény felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="f3795-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="f3795-109">Ez a parancs bővítményt ad a VMMS.</span><span class="sxs-lookup"><span data-stu-id="f3795-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="f3795-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3795-110">PARAMETERS</span></span>

### <span data-ttu-id="f3795-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f3795-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f3795-112">Azt jelzi, hogy a kiterjesztési verziót automatikusan egy újabb alverzióra kell-e frissíteni.</span><span class="sxs-lookup"><span data-stu-id="f3795-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="f3795-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3795-113">-DefaultProfile</span></span>
<span data-ttu-id="f3795-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3795-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3795-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="f3795-115">-ForceUpdateTag</span></span>
<span data-ttu-id="f3795-116">Ha egy érték meg van jelenítve, és eltér az előző értéktől, akkor a bővítmény akkor is kénytelen frissülni, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="f3795-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="f3795-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3795-117">-Name</span></span>
<span data-ttu-id="f3795-118">Itt adhatja meg annak a bővítménynek a nevét, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="f3795-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f3795-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="f3795-119">-ProtectedSetting</span></span>
<span data-ttu-id="f3795-120">A bővítmény privát konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="f3795-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="f3795-121">Ez a parancsmag titkosítja a magánjellegű konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f3795-121">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="f3795-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f3795-122">-Publisher</span></span>
<span data-ttu-id="f3795-123">A bővítmény közzétevőének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3795-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="f3795-124">A Publisher olyan nevet ad, amikor a Publisher a bővítményt regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="f3795-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="f3795-125">Ez a [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) parancsmagot használhatja a közzétevő beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="f3795-125">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="f3795-126">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="f3795-126">-Setting</span></span>
<span data-ttu-id="f3795-127">Megadja a kiterjesztéshez tartozó nyilvános konfigurációt karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="f3795-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="f3795-128">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f3795-128">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="f3795-129">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="f3795-129">-Type</span></span>
<span data-ttu-id="f3795-130">A bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3795-130">Specifies the extension type.</span></span>
<span data-ttu-id="f3795-131">A [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) parancsmaggal lekérheti a bővítmény típusát.</span><span class="sxs-lookup"><span data-stu-id="f3795-131">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="f3795-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f3795-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="f3795-133">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="f3795-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="f3795-134">A [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) parancsmaggal lekérheti a bővítmény verzióját.</span><span class="sxs-lookup"><span data-stu-id="f3795-134">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="f3795-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f3795-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f3795-136">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="f3795-136">Specify the VMSS object.</span></span>
<span data-ttu-id="f3795-137">Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="f3795-137">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="f3795-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f3795-138">-Confirm</span></span>
<span data-ttu-id="f3795-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f3795-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3795-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3795-140">-WhatIf</span></span>
<span data-ttu-id="f3795-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f3795-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3795-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3795-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3795-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3795-143">CommonParameters</span></span>
<span data-ttu-id="f3795-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3795-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3795-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3795-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3795-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3795-146">INPUTS</span></span>

## <span data-ttu-id="f3795-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3795-147">OUTPUTS</span></span>

###  
<span data-ttu-id="f3795-148">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f3795-148">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f3795-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3795-149">NOTES</span></span>

## <span data-ttu-id="f3795-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3795-150">RELATED LINKS</span></span>

[<span data-ttu-id="f3795-151">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f3795-151">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="f3795-152">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f3795-152">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="f3795-153">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="f3795-153">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="f3795-154">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="f3795-154">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="f3795-155">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f3795-155">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

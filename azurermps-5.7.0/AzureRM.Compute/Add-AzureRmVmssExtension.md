---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492390"
---
# <span data-ttu-id="abdf6-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="abdf6-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="abdf6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abdf6-102">SYNOPSIS</span></span>
<span data-ttu-id="abdf6-103">Hozzáad egy bővítményt a VMSS.</span><span class="sxs-lookup"><span data-stu-id="abdf6-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abdf6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abdf6-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abdf6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="abdf6-105">DESCRIPTION</span></span>
<span data-ttu-id="abdf6-106">Az **Add-AzureRmVmssExtension** parancsmag bővítményt ad a virtuálisgép-készlethez (VMSS).</span><span class="sxs-lookup"><span data-stu-id="abdf6-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="abdf6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="abdf6-107">EXAMPLES</span></span>

### <span data-ttu-id="abdf6-108">1. példa: bővítmény felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="abdf6-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="abdf6-109">Ez a parancs bővítményt ad a VMMS.</span><span class="sxs-lookup"><span data-stu-id="abdf6-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="abdf6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abdf6-110">PARAMETERS</span></span>

### <span data-ttu-id="abdf6-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="abdf6-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="abdf6-112">Azt jelzi, hogy a kiterjesztési verziót automatikusan egy újabb alverzióra kell-e frissíteni.</span><span class="sxs-lookup"><span data-stu-id="abdf6-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="abdf6-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="abdf6-113">-Name</span></span>
<span data-ttu-id="abdf6-114">Itt adhatja meg annak a bővítménynek a nevét, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="abdf6-114">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="abdf6-115">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="abdf6-115">-ProtectedSetting</span></span>
<span data-ttu-id="abdf6-116">A bővítmény privát konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="abdf6-116">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="abdf6-117">Ez a parancsmag titkosítja a magánjellegű konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="abdf6-117">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="abdf6-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="abdf6-118">-Publisher</span></span>
<span data-ttu-id="abdf6-119">A bővítmény közzétevőének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="abdf6-119">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="abdf6-120">A Publisher olyan nevet ad, amikor a Publisher a bővítményt regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="abdf6-120">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="abdf6-121">Ez a [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) parancsmagot használhatja a közzétevő beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="abdf6-121">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="abdf6-122">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="abdf6-122">-Setting</span></span>
<span data-ttu-id="abdf6-123">Megadja a kiterjesztéshez tartozó nyilvános konfigurációt karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="abdf6-123">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="abdf6-124">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="abdf6-124">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="abdf6-125">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="abdf6-125">-Type</span></span>
<span data-ttu-id="abdf6-126">A bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="abdf6-126">Specifies the extension type.</span></span>
<span data-ttu-id="abdf6-127">A [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) parancsmaggal lekérheti a bővítmény típusát.</span><span class="sxs-lookup"><span data-stu-id="abdf6-127">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="abdf6-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="abdf6-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="abdf6-129">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="abdf6-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="abdf6-130">A [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) parancsmaggal lekérheti a bővítmény verzióját.</span><span class="sxs-lookup"><span data-stu-id="abdf6-130">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="abdf6-131">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="abdf6-131">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="abdf6-132">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="abdf6-132">Specify the VMSS object.</span></span>
<span data-ttu-id="abdf6-133">Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="abdf6-133">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abdf6-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="abdf6-134">-Confirm</span></span>
<span data-ttu-id="abdf6-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abdf6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abdf6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abdf6-136">-WhatIf</span></span>
<span data-ttu-id="abdf6-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="abdf6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abdf6-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abdf6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abdf6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abdf6-139">CommonParameters</span></span>
<span data-ttu-id="abdf6-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abdf6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abdf6-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abdf6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abdf6-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abdf6-142">INPUTS</span></span>

### <span data-ttu-id="abdf6-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="abdf6-143">None</span></span>
<span data-ttu-id="abdf6-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="abdf6-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="abdf6-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abdf6-145">OUTPUTS</span></span>

###  
<span data-ttu-id="abdf6-146">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="abdf6-146">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="abdf6-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abdf6-147">NOTES</span></span>

## <span data-ttu-id="abdf6-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abdf6-148">RELATED LINKS</span></span>

[<span data-ttu-id="abdf6-149">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="abdf6-149">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="abdf6-150">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="abdf6-150">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="abdf6-151">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="abdf6-151">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="abdf6-152">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="abdf6-152">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="abdf6-153">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="abdf6-153">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

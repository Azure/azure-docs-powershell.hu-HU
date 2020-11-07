---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssextension
schema: 2.0.0
ms.openlocfilehash: f69b8901b2bc2c07bdf158da4c92deba0330109d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848341"
---
# <span data-ttu-id="64956-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="64956-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="64956-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64956-102">SYNOPSIS</span></span>
<span data-ttu-id="64956-103">Hozzáad egy bővítményt a VMSS.</span><span class="sxs-lookup"><span data-stu-id="64956-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64956-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64956-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64956-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64956-105">DESCRIPTION</span></span>
<span data-ttu-id="64956-106">Az **Add-AzureRmVmssExtension** parancsmag bővítményt ad a virtuálisgép-készlethez (VMSS).</span><span class="sxs-lookup"><span data-stu-id="64956-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="64956-107">Példák</span><span class="sxs-lookup"><span data-stu-id="64956-107">EXAMPLES</span></span>

### <span data-ttu-id="64956-108">1. példa: bővítmény felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="64956-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="64956-109">Ez a parancs bővítményt ad a VMMS.</span><span class="sxs-lookup"><span data-stu-id="64956-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="64956-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64956-110">PARAMETERS</span></span>

### <span data-ttu-id="64956-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="64956-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="64956-112">Azt jelzi, hogy a kiterjesztési verziót automatikusan egy újabb alverzióra kell-e frissíteni.</span><span class="sxs-lookup"><span data-stu-id="64956-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="64956-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64956-113">-DefaultProfile</span></span>
<span data-ttu-id="64956-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64956-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64956-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="64956-115">-ForceUpdateTag</span></span>
<span data-ttu-id="64956-116">Ha egy érték meg van jelenítve, és eltér az előző értéktől, akkor a bővítmény akkor is kénytelen frissülni, ha a bővítmény konfigurációja nem változott.</span><span class="sxs-lookup"><span data-stu-id="64956-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="64956-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64956-117">-Name</span></span>
<span data-ttu-id="64956-118">Itt adhatja meg annak a bővítménynek a nevét, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="64956-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="64956-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="64956-119">-ProtectedSetting</span></span>
<span data-ttu-id="64956-120">A bővítmény privát konfigurációját adja meg karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="64956-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="64956-121">Ez a parancsmag titkosítja a magánjellegű konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="64956-121">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="64956-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="64956-122">-Publisher</span></span>
<span data-ttu-id="64956-123">A bővítmény közzétevőének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64956-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="64956-124">A Publisher olyan nevet ad, amikor a Publisher a bővítményt regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="64956-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="64956-125">Ez a [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) parancsmagot használhatja a közzétevő beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="64956-125">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="64956-126">-Beállítás</span><span class="sxs-lookup"><span data-stu-id="64956-126">-Setting</span></span>
<span data-ttu-id="64956-127">Megadja a kiterjesztéshez tartozó nyilvános konfigurációt karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="64956-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="64956-128">Ez a parancsmag nem titkosítja a nyilvános konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="64956-128">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="64956-129">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="64956-129">-Type</span></span>
<span data-ttu-id="64956-130">A bővítmény típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="64956-130">Specifies the extension type.</span></span>
<span data-ttu-id="64956-131">A [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) parancsmaggal lekérheti a bővítmény típusát.</span><span class="sxs-lookup"><span data-stu-id="64956-131">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="64956-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="64956-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="64956-133">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="64956-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="64956-134">A [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) parancsmaggal lekérheti a bővítmény verzióját.</span><span class="sxs-lookup"><span data-stu-id="64956-134">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="64956-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="64956-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="64956-136">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="64956-136">Specify the VMSS object.</span></span>
<span data-ttu-id="64956-137">Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="64956-137">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="64956-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64956-138">-Confirm</span></span>
<span data-ttu-id="64956-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64956-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64956-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64956-140">-WhatIf</span></span>
<span data-ttu-id="64956-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64956-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64956-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64956-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64956-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64956-143">CommonParameters</span></span>
<span data-ttu-id="64956-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64956-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64956-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64956-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64956-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64956-146">INPUTS</span></span>

### <span data-ttu-id="64956-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="64956-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="64956-148">A ' VirtualMachineScaleSet ' paraméter az "VirtualMachineScaleSet" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="64956-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="64956-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64956-149">OUTPUTS</span></span>

###  
<span data-ttu-id="64956-150">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="64956-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="64956-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64956-151">NOTES</span></span>

## <span data-ttu-id="64956-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64956-152">RELATED LINKS</span></span>

[<span data-ttu-id="64956-153">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="64956-153">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="64956-154">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="64956-154">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="64956-155">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="64956-155">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="64956-156">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="64956-156">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="64956-157">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="64956-157">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

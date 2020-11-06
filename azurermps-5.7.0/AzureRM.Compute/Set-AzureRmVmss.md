---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: e3b053d4e8e9ccf9c68d8eb5fabe479f7f58ced1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497700"
---
# <span data-ttu-id="77970-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77970-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="77970-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77970-102">SYNOPSIS</span></span>
<span data-ttu-id="77970-103">Meghatározott műveleteket határoz meg a megadott VMSS.</span><span class="sxs-lookup"><span data-stu-id="77970-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77970-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77970-104">SYNTAX</span></span>

### <span data-ttu-id="77970-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77970-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Reimage] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77970-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="77970-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-ReimageAll] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77970-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="77970-107">DESCRIPTION</span></span>
<span data-ttu-id="77970-108">A **set-AzureRmVmss** parancsmag meghatározott műveleteket állít be a virtuálisgép-készlet (VMSS) beállításnál.</span><span class="sxs-lookup"><span data-stu-id="77970-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="77970-109">A csak a parancsmag által támogatott műveletek a Reimage.</span><span class="sxs-lookup"><span data-stu-id="77970-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="77970-110">Példák</span><span class="sxs-lookup"><span data-stu-id="77970-110">EXAMPLES</span></span>

### <span data-ttu-id="77970-111">Példa 1: VMSS</span><span class="sxs-lookup"><span data-stu-id="77970-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="77970-112">Ez a parancs a ContosoGroup nevű erőforráscsoporthoz tartozó ContosoVMSS VMSS.</span><span class="sxs-lookup"><span data-stu-id="77970-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="77970-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77970-113">PARAMETERS</span></span>

### <span data-ttu-id="77970-114">-Reimage</span><span class="sxs-lookup"><span data-stu-id="77970-114">-Reimage</span></span>
<span data-ttu-id="77970-115">Jelzi, hogy a parancsmag átadja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="77970-115">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77970-116">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="77970-116">-ReimageAll</span></span>
<span data-ttu-id="77970-117">Jelzi, hogy a parancsmag a VMSS összes lemezét átadja.</span><span class="sxs-lookup"><span data-stu-id="77970-117">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77970-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77970-118">-ResourceGroupName</span></span>
<span data-ttu-id="77970-119">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="77970-119">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77970-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="77970-120">-VMScaleSetName</span></span>
<span data-ttu-id="77970-121">Faj: annak a VMSS a neve, amelyhez a parancsmag a műveleteket állítja be.</span><span class="sxs-lookup"><span data-stu-id="77970-121">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77970-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="77970-122">-Confirm</span></span>
<span data-ttu-id="77970-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77970-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77970-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77970-124">-WhatIf</span></span>
<span data-ttu-id="77970-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="77970-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77970-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77970-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77970-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77970-127">CommonParameters</span></span>
<span data-ttu-id="77970-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77970-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77970-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77970-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77970-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77970-130">INPUTS</span></span>

### <span data-ttu-id="77970-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="77970-131">None</span></span>
<span data-ttu-id="77970-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="77970-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77970-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77970-133">OUTPUTS</span></span>

### <span data-ttu-id="77970-134">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="77970-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="77970-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77970-135">NOTES</span></span>

## <span data-ttu-id="77970-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77970-136">RELATED LINKS</span></span>

[<span data-ttu-id="77970-137">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77970-137">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="77970-138">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77970-138">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="77970-139">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77970-139">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="77970-140">Újraindítás – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77970-140">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="77970-141">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77970-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="77970-142">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77970-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="77970-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="77970-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)



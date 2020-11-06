---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 1bc6b2b3ceb7ed7f991c92e4b8f8b034c78d54d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503840"
---
# <span data-ttu-id="b0fcf-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b0fcf-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="b0fcf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="b0fcf-103">A VMSS vagy egy virtuális gép újraindítása a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="b0fcf-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0fcf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0fcf-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0fcf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0fcf-105">DESCRIPTION</span></span>
<span data-ttu-id="b0fcf-106">Az **Újraindítás-AzureRmVmss** parancsmag újraindítja a virtuálisgép-készletet (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b0fcf-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="b0fcf-107">Ez a parancsmag azt is megteheti, hogy a *InstanceId* paraméterrel az adott virtuális gép újraindítása a VMSS belül.</span><span class="sxs-lookup"><span data-stu-id="b0fcf-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="b0fcf-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b0fcf-108">EXAMPLES</span></span>

### <span data-ttu-id="b0fcf-109">Példa 1: a VMSS újraindítása</span><span class="sxs-lookup"><span data-stu-id="b0fcf-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="b0fcf-110">Ez a parancs elindítja a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS.</span><span class="sxs-lookup"><span data-stu-id="b0fcf-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="b0fcf-111">2. példa: egy adott virtuális gép újraindítása a VMSS belül</span><span class="sxs-lookup"><span data-stu-id="b0fcf-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="b0fcf-112">Ez a parancs egy olyan virtuális gépet indít elő, amely az 1-es azonosítójú példány azonosítóját tartalmazza a Group001 nevű erőforráscsoport VMSS001 tartozó VMSS.</span><span class="sxs-lookup"><span data-stu-id="b0fcf-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="b0fcf-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0fcf-113">PARAMETERS</span></span>

### <span data-ttu-id="b0fcf-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b0fcf-114">-InstanceId</span></span>
<span data-ttu-id="b0fcf-115">Karakterláncként adja meg az újraindítani kívánt példányok AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="b0fcf-115">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0fcf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0fcf-116">-ResourceGroupName</span></span>
<span data-ttu-id="b0fcf-117">A VMSS erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0fcf-117">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="b0fcf-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b0fcf-118">-VMScaleSetName</span></span>
<span data-ttu-id="b0fcf-119">Faj: annak a VMSS a neve, amelyre a parancsmag újraindult.</span><span class="sxs-lookup"><span data-stu-id="b0fcf-119">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="b0fcf-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b0fcf-120">-Confirm</span></span>
<span data-ttu-id="b0fcf-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b0fcf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0fcf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0fcf-122">-WhatIf</span></span>
<span data-ttu-id="b0fcf-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b0fcf-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0fcf-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0fcf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0fcf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0fcf-125">CommonParameters</span></span>
<span data-ttu-id="b0fcf-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0fcf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0fcf-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0fcf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0fcf-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0fcf-128">INPUTS</span></span>

### <span data-ttu-id="b0fcf-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="b0fcf-129">None</span></span>
<span data-ttu-id="b0fcf-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b0fcf-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b0fcf-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0fcf-131">OUTPUTS</span></span>

###  
<span data-ttu-id="b0fcf-132">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b0fcf-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b0fcf-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0fcf-133">NOTES</span></span>

## <span data-ttu-id="b0fcf-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0fcf-134">RELATED LINKS</span></span>

[<span data-ttu-id="b0fcf-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b0fcf-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="b0fcf-136">Új – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b0fcf-136">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="b0fcf-137">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b0fcf-137">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="b0fcf-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b0fcf-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="b0fcf-139">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b0fcf-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="b0fcf-140">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b0fcf-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="b0fcf-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b0fcf-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)



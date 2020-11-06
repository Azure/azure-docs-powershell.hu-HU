---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 89ab4ea57f5f03fbc26d33e1a9087371f215d4ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492369"
---
# <span data-ttu-id="93825-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="93825-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="93825-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93825-102">SYNOPSIS</span></span>
<span data-ttu-id="93825-103">Egy virtuális gépről eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="93825-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93825-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93825-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93825-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="93825-105">DESCRIPTION</span></span>
<span data-ttu-id="93825-106">A **Remove-AzureRmVMNetworkInterface** parancsmag egy virtuális gépről eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="93825-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="93825-107">Példák</span><span class="sxs-lookup"><span data-stu-id="93825-107">EXAMPLES</span></span>

## <span data-ttu-id="93825-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93825-108">PARAMETERS</span></span>

### <span data-ttu-id="93825-109">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="93825-109">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="93825-110">A parancsmag által eltávolított hálózati illesztőfelület-azonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93825-110">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-111">-VM</span><span class="sxs-lookup"><span data-stu-id="93825-111">-VM</span></span>
<span data-ttu-id="93825-112">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="93825-112">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="93825-113">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="93825-113">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93825-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="93825-114">-Confirm</span></span>
<span data-ttu-id="93825-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="93825-115">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93825-116">-WhatIf</span></span>
<span data-ttu-id="93825-117">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="93825-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93825-118">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93825-118">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93825-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93825-119">CommonParameters</span></span>
<span data-ttu-id="93825-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93825-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93825-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93825-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93825-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93825-122">INPUTS</span></span>

### <span data-ttu-id="93825-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="93825-123">None</span></span>
<span data-ttu-id="93825-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="93825-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93825-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93825-125">OUTPUTS</span></span>

## <span data-ttu-id="93825-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93825-126">NOTES</span></span>

## <span data-ttu-id="93825-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93825-127">RELATED LINKS</span></span>

[<span data-ttu-id="93825-128">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93825-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)



---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 0c7900d50074e185d26f4fafccd9b63756749fd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849738"
---
# <span data-ttu-id="72d55-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="72d55-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="72d55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72d55-102">SYNOPSIS</span></span>
<span data-ttu-id="72d55-103">Egy virtuális gépről eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="72d55-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72d55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72d55-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72d55-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72d55-105">DESCRIPTION</span></span>
<span data-ttu-id="72d55-106">A **Remove-AzureRmVMNetworkInterface** parancsmag egy virtuális gépről eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="72d55-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="72d55-107">Példák</span><span class="sxs-lookup"><span data-stu-id="72d55-107">EXAMPLES</span></span>

### <span data-ttu-id="72d55-108">1:</span><span class="sxs-lookup"><span data-stu-id="72d55-108">1:</span></span>
```

```

## <span data-ttu-id="72d55-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72d55-109">PARAMETERS</span></span>

### <span data-ttu-id="72d55-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d55-110">-DefaultProfile</span></span>
<span data-ttu-id="72d55-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72d55-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72d55-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="72d55-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="72d55-113">A parancsmag által eltávolított hálózati illesztőfelület-azonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72d55-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="72d55-114">-VM</span><span class="sxs-lookup"><span data-stu-id="72d55-114">-VM</span></span>
<span data-ttu-id="72d55-115">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="72d55-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="72d55-116">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="72d55-116">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="72d55-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="72d55-117">-Confirm</span></span>
<span data-ttu-id="72d55-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72d55-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="72d55-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72d55-119">-WhatIf</span></span>
<span data-ttu-id="72d55-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="72d55-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72d55-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72d55-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="72d55-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d55-122">CommonParameters</span></span>
<span data-ttu-id="72d55-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72d55-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d55-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72d55-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d55-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72d55-125">INPUTS</span></span>

### <span data-ttu-id="72d55-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="72d55-126">PSVirtualMachine</span></span>
<span data-ttu-id="72d55-127">A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="72d55-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="72d55-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72d55-128">OUTPUTS</span></span>

### <span data-ttu-id="72d55-129">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="72d55-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="72d55-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72d55-130">NOTES</span></span>

## <span data-ttu-id="72d55-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72d55-131">RELATED LINKS</span></span>

[<span data-ttu-id="72d55-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="72d55-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)



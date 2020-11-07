---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 548d576ff959dd96a6978675ca5a35c18c97e0a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844362"
---
# <span data-ttu-id="68826-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="68826-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="68826-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68826-102">SYNOPSIS</span></span>
<span data-ttu-id="68826-103">Egy virtuális gépről eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="68826-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="68826-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68826-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68826-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="68826-105">DESCRIPTION</span></span>
<span data-ttu-id="68826-106">A **Remove-AzVMNetworkInterface** parancsmag egy virtuális gépről eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="68826-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="68826-107">Példák</span><span class="sxs-lookup"><span data-stu-id="68826-107">EXAMPLES</span></span>

### <span data-ttu-id="68826-108">1:</span><span class="sxs-lookup"><span data-stu-id="68826-108">1:</span></span>
```

```

## <span data-ttu-id="68826-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68826-109">PARAMETERS</span></span>

### <span data-ttu-id="68826-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68826-110">-DefaultProfile</span></span>
<span data-ttu-id="68826-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68826-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68826-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="68826-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="68826-113">A parancsmag által eltávolított hálózati illesztőfelület-azonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68826-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="68826-114">-VM</span><span class="sxs-lookup"><span data-stu-id="68826-114">-VM</span></span>
<span data-ttu-id="68826-115">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="68826-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="68826-116">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="68826-116">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="68826-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="68826-117">-Confirm</span></span>
<span data-ttu-id="68826-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="68826-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="68826-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68826-119">-WhatIf</span></span>
<span data-ttu-id="68826-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="68826-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68826-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68826-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="68826-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68826-122">CommonParameters</span></span>
<span data-ttu-id="68826-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68826-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68826-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68826-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68826-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68826-125">INPUTS</span></span>

### <span data-ttu-id="68826-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="68826-126">PSVirtualMachine</span></span>
<span data-ttu-id="68826-127">A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="68826-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="68826-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68826-128">OUTPUTS</span></span>

### <span data-ttu-id="68826-129">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="68826-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="68826-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68826-130">NOTES</span></span>

## <span data-ttu-id="68826-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68826-131">RELATED LINKS</span></span>

[<span data-ttu-id="68826-132">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="68826-132">Get-AzVM</span></span>](./Get-AzVM.md)



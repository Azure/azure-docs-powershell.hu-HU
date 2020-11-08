---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186580"
---
# <span data-ttu-id="bf938-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bf938-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="bf938-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf938-102">SYNOPSIS</span></span>
<span data-ttu-id="bf938-103">Egy virtuális gépről eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="bf938-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="bf938-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf938-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf938-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf938-105">DESCRIPTION</span></span>
<span data-ttu-id="bf938-106">A **Remove-AzVMNetworkInterface** parancsmag egy virtuális gépről eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="bf938-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="bf938-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf938-107">EXAMPLES</span></span>

## <span data-ttu-id="bf938-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf938-108">PARAMETERS</span></span>

### <span data-ttu-id="bf938-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf938-109">-DefaultProfile</span></span>
<span data-ttu-id="bf938-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf938-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf938-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="bf938-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="bf938-112">A parancsmag által eltávolított hálózati illesztőfelület-azonosítók tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf938-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf938-113">-VM</span><span class="sxs-lookup"><span data-stu-id="bf938-113">-VM</span></span>
<span data-ttu-id="bf938-114">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="bf938-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="bf938-115">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bf938-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf938-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf938-116">-Confirm</span></span>
<span data-ttu-id="bf938-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf938-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf938-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf938-118">-WhatIf</span></span>
<span data-ttu-id="bf938-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf938-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf938-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf938-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf938-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf938-121">CommonParameters</span></span>
<span data-ttu-id="bf938-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf938-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf938-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bf938-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf938-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf938-124">INPUTS</span></span>

### <span data-ttu-id="bf938-125">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bf938-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="bf938-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf938-126">OUTPUTS</span></span>

### <span data-ttu-id="bf938-127">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bf938-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="bf938-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf938-128">NOTES</span></span>

## <span data-ttu-id="bf938-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf938-129">RELATED LINKS</span></span>

[<span data-ttu-id="bf938-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="bf938-130">Get-AzVM</span></span>](./Get-AzVM.md)


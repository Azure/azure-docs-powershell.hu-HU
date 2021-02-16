---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148787"
---
# <span data-ttu-id="e696b-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e696b-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="e696b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e696b-102">SYNOPSIS</span></span>
<span data-ttu-id="e696b-103">Eltávolítja a hálózati felületet egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="e696b-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="e696b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e696b-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e696b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e696b-105">DESCRIPTION</span></span>
<span data-ttu-id="e696b-106">A **Remove-AzVMNetworkInterface** parancsmag eltávolítja a hálózati felületet egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="e696b-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="e696b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e696b-107">EXAMPLES</span></span>

## <span data-ttu-id="e696b-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e696b-108">PARAMETERS</span></span>

### <span data-ttu-id="e696b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e696b-109">-DefaultProfile</span></span>
<span data-ttu-id="e696b-110">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e696b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e696b-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="e696b-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="e696b-112">A parancsmag által eltávolítandó hálózatifelület-kiosztási tömböt ad meg.</span><span class="sxs-lookup"><span data-stu-id="e696b-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e696b-113">-VM</span><span class="sxs-lookup"><span data-stu-id="e696b-113">-VM</span></span>
<span data-ttu-id="e696b-114">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja a hálózati felületet.</span><span class="sxs-lookup"><span data-stu-id="e696b-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="e696b-115">Virtuális gépi objektum beszerzéséhez használja a Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e696b-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="e696b-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e696b-116">-Confirm</span></span>
<span data-ttu-id="e696b-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e696b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e696b-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e696b-118">-WhatIf</span></span>
<span data-ttu-id="e696b-119">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e696b-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e696b-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e696b-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e696b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e696b-121">CommonParameters</span></span>
<span data-ttu-id="e696b-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e696b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e696b-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e696b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e696b-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e696b-124">INPUTS</span></span>

### <span data-ttu-id="e696b-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e696b-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e696b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e696b-126">OUTPUTS</span></span>

### <span data-ttu-id="e696b-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e696b-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e696b-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e696b-128">NOTES</span></span>

## <span data-ttu-id="e696b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e696b-129">RELATED LINKS</span></span>

[<span data-ttu-id="e696b-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e696b-130">Get-AzVM</span></span>](./Get-AzVM.md)



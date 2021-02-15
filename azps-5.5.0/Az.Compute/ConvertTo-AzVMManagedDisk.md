---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166571"
---
# <span data-ttu-id="98b1b-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="98b1b-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="98b1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="98b1b-103">Blob-alapú lemezeket tároló virtuális gép átalakítása felügyelt lemezeket tároló virtuális gépké.</span><span class="sxs-lookup"><span data-stu-id="98b1b-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="98b1b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="98b1b-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98b1b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="98b1b-105">DESCRIPTION</span></span>
<span data-ttu-id="98b1b-106">A **ConvertTo-AzVMManagedDisk** parancsmag egy blobalapú lemezeket tároló virtuális gépet felügyelt lemezeket tároló virtuális gépké konvertál.</span><span class="sxs-lookup"><span data-stu-id="98b1b-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="98b1b-107">A művelet meghozása előtt le kell állítani a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="98b1b-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="98b1b-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="98b1b-108">EXAMPLES</span></span>

### <span data-ttu-id="98b1b-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="98b1b-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="98b1b-110">Ez a parancs felügyelt lemezeket hoz létre az "ResourceGroup01" erőforráscsoport virtuális gép "VM01" nevű blobalapú lemezeiből.</span><span class="sxs-lookup"><span data-stu-id="98b1b-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="98b1b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98b1b-111">PARAMETERS</span></span>

### <span data-ttu-id="98b1b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98b1b-112">-AsJob</span></span>
<span data-ttu-id="98b1b-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="98b1b-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b1b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b1b-114">-DefaultProfile</span></span>
<span data-ttu-id="98b1b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98b1b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98b1b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98b1b-116">-ResourceGroupName</span></span>
<span data-ttu-id="98b1b-117">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98b1b-117">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b1b-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="98b1b-118">-VMName</span></span>
<span data-ttu-id="98b1b-119">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98b1b-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b1b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98b1b-120">-Confirm</span></span>
<span data-ttu-id="98b1b-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="98b1b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98b1b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98b1b-122">-WhatIf</span></span>
<span data-ttu-id="98b1b-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="98b1b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98b1b-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="98b1b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98b1b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b1b-125">CommonParameters</span></span>
<span data-ttu-id="98b1b-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98b1b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b1b-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98b1b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b1b-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98b1b-128">INPUTS</span></span>

### <span data-ttu-id="98b1b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="98b1b-129">System.String</span></span>

## <span data-ttu-id="98b1b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98b1b-130">OUTPUTS</span></span>

### <span data-ttu-id="98b1b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="98b1b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="98b1b-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="98b1b-132">NOTES</span></span>

## <span data-ttu-id="98b1b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98b1b-133">RELATED LINKS</span></span>

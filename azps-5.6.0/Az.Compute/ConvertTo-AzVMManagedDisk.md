---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: f73569e8e40af5111a738496ba6ad41ff03058f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927338"
---
# <span data-ttu-id="1442b-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="1442b-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="1442b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1442b-102">SYNOPSIS</span></span>
<span data-ttu-id="1442b-103">Blob-alapú lemezeket tároló virtuális gép átalakítása felügyelt lemezeket tároló virtuális gépké.</span><span class="sxs-lookup"><span data-stu-id="1442b-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="1442b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1442b-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1442b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1442b-105">DESCRIPTION</span></span>
<span data-ttu-id="1442b-106">A **ConvertTo-AzVMManagedDisk** parancsmag egy blobalapú lemezeket tároló virtuális gépet felügyelt lemezeket tároló virtuális gépké konvertál.</span><span class="sxs-lookup"><span data-stu-id="1442b-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="1442b-107">A művelet meghozása előtt le kell állítani a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="1442b-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="1442b-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1442b-108">EXAMPLES</span></span>

### <span data-ttu-id="1442b-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="1442b-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="1442b-110">Ez a parancs felügyelt lemezeket hoz létre az "ResourceGroup01" erőforráscsoport virtuális gép "VM01" nevű blobalapú lemezeiből.</span><span class="sxs-lookup"><span data-stu-id="1442b-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="1442b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1442b-111">PARAMETERS</span></span>

### <span data-ttu-id="1442b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1442b-112">-AsJob</span></span>
<span data-ttu-id="1442b-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1442b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1442b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1442b-114">-DefaultProfile</span></span>
<span data-ttu-id="1442b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1442b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1442b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1442b-116">-ResourceGroupName</span></span>
<span data-ttu-id="1442b-117">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1442b-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1442b-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="1442b-118">-VMName</span></span>
<span data-ttu-id="1442b-119">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1442b-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="1442b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1442b-120">-Confirm</span></span>
<span data-ttu-id="1442b-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1442b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1442b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1442b-122">-WhatIf</span></span>
<span data-ttu-id="1442b-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1442b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1442b-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1442b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1442b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1442b-125">CommonParameters</span></span>
<span data-ttu-id="1442b-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1442b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1442b-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1442b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1442b-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1442b-128">INPUTS</span></span>

### <span data-ttu-id="1442b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1442b-129">System.String</span></span>

## <span data-ttu-id="1442b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1442b-130">OUTPUTS</span></span>

### <span data-ttu-id="1442b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="1442b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1442b-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1442b-132">NOTES</span></span>

## <span data-ttu-id="1442b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1442b-133">RELATED LINKS</span></span>

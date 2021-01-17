---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480840"
---
# <span data-ttu-id="9d9eb-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="9d9eb-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="9d9eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d9eb-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9eb-103">Egy Azure virtuális gép újraimizálása.</span><span class="sxs-lookup"><span data-stu-id="9d9eb-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="9d9eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9d9eb-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d9eb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9d9eb-105">DESCRIPTION</span></span>
<span data-ttu-id="9d9eb-106">Az **Invoke-AzVMReimage** parancsmag újragondol egy Azure-virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="9d9eb-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="9d9eb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9d9eb-107">EXAMPLES</span></span>

### <span data-ttu-id="9d9eb-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9d9eb-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="9d9eb-109">Ez a parancs újragondolja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="9d9eb-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="9d9eb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d9eb-110">PARAMETERS</span></span>

### <span data-ttu-id="9d9eb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d9eb-111">-AsJob</span></span>
<span data-ttu-id="9d9eb-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9d9eb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d9eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d9eb-113">-DefaultProfile</span></span>
<span data-ttu-id="9d9eb-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d9eb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d9eb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d9eb-115">-ResourceGroupName</span></span>
<span data-ttu-id="9d9eb-116">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d9eb-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9d9eb-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="9d9eb-117">-TempDisk</span></span>
<span data-ttu-id="9d9eb-118">Megadja, hogy újraimálja-e a temp disket.</span><span class="sxs-lookup"><span data-stu-id="9d9eb-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="9d9eb-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="9d9eb-119">-VMName</span></span>
<span data-ttu-id="9d9eb-120">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="9d9eb-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="9d9eb-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d9eb-121">-Confirm</span></span>
<span data-ttu-id="9d9eb-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9d9eb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d9eb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d9eb-123">-WhatIf</span></span>
<span data-ttu-id="9d9eb-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9d9eb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d9eb-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9d9eb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d9eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9eb-126">CommonParameters</span></span>
<span data-ttu-id="9d9eb-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d9eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9eb-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d9eb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9eb-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d9eb-129">INPUTS</span></span>

### <span data-ttu-id="9d9eb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9d9eb-130">System.String</span></span>

## <span data-ttu-id="9d9eb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d9eb-131">OUTPUTS</span></span>

### <span data-ttu-id="9d9eb-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9d9eb-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9d9eb-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9d9eb-133">NOTES</span></span>

## <span data-ttu-id="9d9eb-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d9eb-134">RELATED LINKS</span></span>

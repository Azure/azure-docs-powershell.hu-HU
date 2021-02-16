---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144939"
---
# <span data-ttu-id="1095b-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="1095b-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="1095b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1095b-102">SYNOPSIS</span></span>
<span data-ttu-id="1095b-103">Egy Azure virtuális gép újraimizálása.</span><span class="sxs-lookup"><span data-stu-id="1095b-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="1095b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1095b-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1095b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1095b-105">DESCRIPTION</span></span>
<span data-ttu-id="1095b-106">Az **Invoke-AzVMReimage** parancsmag újragondol egy Azure-virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="1095b-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="1095b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1095b-107">EXAMPLES</span></span>

### <span data-ttu-id="1095b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1095b-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="1095b-109">Ez a parancs újragondolja a VirtualMachine07 nevű virtuális gépet a ResourceGroup11-ben.</span><span class="sxs-lookup"><span data-stu-id="1095b-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="1095b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1095b-110">PARAMETERS</span></span>

### <span data-ttu-id="1095b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1095b-111">-AsJob</span></span>
<span data-ttu-id="1095b-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1095b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1095b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1095b-113">-DefaultProfile</span></span>
<span data-ttu-id="1095b-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1095b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1095b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1095b-115">-ResourceGroupName</span></span>
<span data-ttu-id="1095b-116">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1095b-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1095b-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="1095b-117">-TempDisk</span></span>
<span data-ttu-id="1095b-118">Azt adja meg, hogy a program átvesz-e ideiglenes lemezre.</span><span class="sxs-lookup"><span data-stu-id="1095b-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="1095b-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="1095b-119">-VMName</span></span>
<span data-ttu-id="1095b-120">A virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="1095b-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="1095b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1095b-121">-Confirm</span></span>
<span data-ttu-id="1095b-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1095b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1095b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1095b-123">-WhatIf</span></span>
<span data-ttu-id="1095b-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1095b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1095b-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1095b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1095b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1095b-126">CommonParameters</span></span>
<span data-ttu-id="1095b-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1095b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1095b-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1095b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1095b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1095b-129">INPUTS</span></span>

### <span data-ttu-id="1095b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1095b-130">System.String</span></span>

## <span data-ttu-id="1095b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1095b-131">OUTPUTS</span></span>

### <span data-ttu-id="1095b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="1095b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1095b-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1095b-133">NOTES</span></span>

## <span data-ttu-id="1095b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1095b-134">RELATED LINKS</span></span>

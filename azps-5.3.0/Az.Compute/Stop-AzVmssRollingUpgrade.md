---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477626"
---
# <span data-ttu-id="c3ec5-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="c3ec5-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="c3ec5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ec5-103">Megszakítja az aktuális virtuális gép méretezéskészletének frissítését.</span><span class="sxs-lookup"><span data-stu-id="c3ec5-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="c3ec5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3ec5-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3ec5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3ec5-105">DESCRIPTION</span></span>
<span data-ttu-id="c3ec5-106">Megszakítja az aktuális virtuális gép méretezéskészletének frissítését.</span><span class="sxs-lookup"><span data-stu-id="c3ec5-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="c3ec5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3ec5-107">EXAMPLES</span></span>

### <span data-ttu-id="c3ec5-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c3ec5-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="c3ec5-109">Ez a parancs megszakítja a VM-méretarányú "VMSS001" készlet folyamatos frissítését a "Group001" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="c3ec5-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="c3ec5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3ec5-110">PARAMETERS</span></span>

### <span data-ttu-id="c3ec5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3ec5-111">-AsJob</span></span>
<span data-ttu-id="c3ec5-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c3ec5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3ec5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ec5-113">-DefaultProfile</span></span>
<span data-ttu-id="c3ec5-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3ec5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3ec5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c3ec5-115">-Force</span></span>
<span data-ttu-id="c3ec5-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="c3ec5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c3ec5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3ec5-117">-ResourceGroupName</span></span>
<span data-ttu-id="c3ec5-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c3ec5-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c3ec5-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c3ec5-119">-VMScaleSetName</span></span>
<span data-ttu-id="c3ec5-120">A VM-méretkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="c3ec5-120">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="c3ec5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3ec5-121">-Confirm</span></span>
<span data-ttu-id="c3ec5-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c3ec5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3ec5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3ec5-123">-WhatIf</span></span>
<span data-ttu-id="c3ec5-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c3ec5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3ec5-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3ec5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3ec5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ec5-126">CommonParameters</span></span>
<span data-ttu-id="c3ec5-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3ec5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ec5-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3ec5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ec5-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3ec5-129">INPUTS</span></span>

### <span data-ttu-id="c3ec5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c3ec5-130">System.String</span></span>

## <span data-ttu-id="c3ec5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3ec5-131">OUTPUTS</span></span>

### <span data-ttu-id="c3ec5-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c3ec5-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c3ec5-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3ec5-133">NOTES</span></span>

## <span data-ttu-id="c3ec5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3ec5-134">RELATED LINKS</span></span>

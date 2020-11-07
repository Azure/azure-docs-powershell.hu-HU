---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: cbe44db07cbf32195f92ebefc0a2032a5f288a1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667173"
---
# <span data-ttu-id="e75ff-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="e75ff-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="e75ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e75ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e75ff-103">A jelenlegi virtuálisgép-méretarány beállítása a folyamatos frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="e75ff-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="e75ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e75ff-104">SYNTAX</span></span>

### <span data-ttu-id="e75ff-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e75ff-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e75ff-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="e75ff-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e75ff-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e75ff-107">DESCRIPTION</span></span>
<span data-ttu-id="e75ff-108">A jelenlegi virtuálisgép-méretarány beállítása a folyamatos frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="e75ff-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="e75ff-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e75ff-109">EXAMPLES</span></span>

### <span data-ttu-id="e75ff-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e75ff-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="e75ff-111">Ez a parancs a "VMSS001" erőforráscsoport "Group001" erőforráscsoporthoz való folyamatos folyamatos frissítését lemondja.</span><span class="sxs-lookup"><span data-stu-id="e75ff-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="e75ff-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e75ff-112">PARAMETERS</span></span>

### <span data-ttu-id="e75ff-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e75ff-113">-AsJob</span></span>
<span data-ttu-id="e75ff-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e75ff-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e75ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e75ff-115">-DefaultProfile</span></span>
<span data-ttu-id="e75ff-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e75ff-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e75ff-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e75ff-117">-Force</span></span>
<span data-ttu-id="e75ff-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e75ff-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e75ff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e75ff-119">-ResourceGroupName</span></span>
<span data-ttu-id="e75ff-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e75ff-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75ff-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e75ff-121">-VMScaleSetName</span></span>
<span data-ttu-id="e75ff-122">A VM-lépték halmazának neve.</span><span class="sxs-lookup"><span data-stu-id="e75ff-122">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75ff-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e75ff-123">-Confirm</span></span>
<span data-ttu-id="e75ff-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e75ff-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e75ff-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e75ff-125">-WhatIf</span></span>
<span data-ttu-id="e75ff-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e75ff-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e75ff-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e75ff-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e75ff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e75ff-128">CommonParameters</span></span>
<span data-ttu-id="e75ff-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e75ff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e75ff-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e75ff-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e75ff-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e75ff-131">INPUTS</span></span>

### <span data-ttu-id="e75ff-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e75ff-132">System.String</span></span>

## <span data-ttu-id="e75ff-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e75ff-133">OUTPUTS</span></span>

### <span data-ttu-id="e75ff-134">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e75ff-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e75ff-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e75ff-135">NOTES</span></span>

## <span data-ttu-id="e75ff-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e75ff-136">RELATED LINKS</span></span>

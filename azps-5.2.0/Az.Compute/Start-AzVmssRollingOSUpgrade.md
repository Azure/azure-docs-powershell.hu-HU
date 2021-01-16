---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: ad5d387a0935150a66924cbfdd19ac40ed57079c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327358"
---
# <span data-ttu-id="33cce-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="33cce-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="33cce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33cce-102">SYNOPSIS</span></span>
<span data-ttu-id="33cce-103">Egy gördülékens frissítést kezd, hogy az összes virtuális gép méretaránykészlet-példánya a platform operációs rendszer legújabb elérhető verziójába oszljon át.</span><span class="sxs-lookup"><span data-stu-id="33cce-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="33cce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="33cce-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33cce-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="33cce-105">DESCRIPTION</span></span>
<span data-ttu-id="33cce-106">Egy gördülékens frissítést kezd, hogy az összes virtuális gép méretaránykészlet-példánya a platform operációs rendszer legújabb elérhető verziójába oszljon át.</span><span class="sxs-lookup"><span data-stu-id="33cce-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="33cce-107">Azok a példányok, amelyek már a legújabb elérhető operációs rendszert futtatják, nem érintik.</span><span class="sxs-lookup"><span data-stu-id="33cce-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="33cce-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="33cce-108">EXAMPLES</span></span>

### <span data-ttu-id="33cce-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="33cce-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="33cce-110">Ez a parancs elindítja a "Group001" erőforráscsoport vm scale set "VMSS001" (VMSS001) méretkészletének összes virtuális géppéldányának gördülékes frissítését.</span><span class="sxs-lookup"><span data-stu-id="33cce-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="33cce-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33cce-111">PARAMETERS</span></span>

### <span data-ttu-id="33cce-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33cce-112">-AsJob</span></span>
<span data-ttu-id="33cce-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="33cce-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33cce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33cce-114">-DefaultProfile</span></span>
<span data-ttu-id="33cce-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33cce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33cce-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33cce-116">-ResourceGroupName</span></span>
<span data-ttu-id="33cce-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="33cce-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="33cce-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="33cce-118">-VMScaleSetName</span></span>
<span data-ttu-id="33cce-119">A VM-méretkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="33cce-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="33cce-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33cce-120">-Confirm</span></span>
<span data-ttu-id="33cce-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="33cce-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33cce-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33cce-122">-WhatIf</span></span>
<span data-ttu-id="33cce-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="33cce-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33cce-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="33cce-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33cce-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33cce-125">CommonParameters</span></span>
<span data-ttu-id="33cce-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33cce-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33cce-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33cce-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33cce-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33cce-128">INPUTS</span></span>

### <span data-ttu-id="33cce-129">System.String</span><span class="sxs-lookup"><span data-stu-id="33cce-129">System.String</span></span>

## <span data-ttu-id="33cce-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33cce-130">OUTPUTS</span></span>

### <span data-ttu-id="33cce-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="33cce-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="33cce-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="33cce-132">NOTES</span></span>

## <span data-ttu-id="33cce-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33cce-133">RELATED LINKS</span></span>

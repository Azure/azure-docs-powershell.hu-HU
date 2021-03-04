---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: fb3d6f08eaa540e208830a15563b8edd8c2432ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923841"
---
# <span data-ttu-id="f74d0-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="f74d0-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="f74d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f74d0-102">SYNOPSIS</span></span>
<span data-ttu-id="f74d0-103">Egy gördülékens frissítést kezd, hogy az összes virtuális gép méretaránykészlet-példánya a platform operációs rendszer legújabb elérhető verziójába oszljon át.</span><span class="sxs-lookup"><span data-stu-id="f74d0-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="f74d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f74d0-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f74d0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f74d0-105">DESCRIPTION</span></span>
<span data-ttu-id="f74d0-106">Egy gördülékens frissítést kezd, hogy az összes virtuális gép méretaránykészlet-példánya a platform operációs rendszer legújabb elérhető verziójába oszljon át.</span><span class="sxs-lookup"><span data-stu-id="f74d0-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="f74d0-107">Azok a példányok, amelyek már a legújabb elérhető operációs rendszert futtatják, nem érintik.</span><span class="sxs-lookup"><span data-stu-id="f74d0-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="f74d0-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f74d0-108">EXAMPLES</span></span>

### <span data-ttu-id="f74d0-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="f74d0-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="f74d0-110">Ez a parancs elindítja a "Group0001" erőforráscsoport vm scale set "VMSS001" (VMSS001) méretkészletének összes virtuális géppéldányának gördülékes frissítését.</span><span class="sxs-lookup"><span data-stu-id="f74d0-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="f74d0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f74d0-111">PARAMETERS</span></span>

### <span data-ttu-id="f74d0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f74d0-112">-AsJob</span></span>
<span data-ttu-id="f74d0-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f74d0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f74d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f74d0-114">-DefaultProfile</span></span>
<span data-ttu-id="f74d0-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f74d0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f74d0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f74d0-116">-ResourceGroupName</span></span>
<span data-ttu-id="f74d0-117">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f74d0-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="f74d0-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f74d0-118">-VMScaleSetName</span></span>
<span data-ttu-id="f74d0-119">A VM-méretkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="f74d0-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="f74d0-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f74d0-120">-Confirm</span></span>
<span data-ttu-id="f74d0-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f74d0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f74d0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f74d0-122">-WhatIf</span></span>
<span data-ttu-id="f74d0-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f74d0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f74d0-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f74d0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f74d0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f74d0-125">CommonParameters</span></span>
<span data-ttu-id="f74d0-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f74d0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f74d0-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f74d0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f74d0-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f74d0-128">INPUTS</span></span>

### <span data-ttu-id="f74d0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f74d0-129">System.String</span></span>

## <span data-ttu-id="f74d0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f74d0-130">OUTPUTS</span></span>

### <span data-ttu-id="f74d0-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f74d0-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f74d0-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f74d0-132">NOTES</span></span>

## <span data-ttu-id="f74d0-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f74d0-133">RELATED LINKS</span></span>

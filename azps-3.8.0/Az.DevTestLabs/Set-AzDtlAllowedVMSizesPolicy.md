---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: d5e8b16fec390c4b4d900760d3efb60abfb7da0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012391"
---
# <span data-ttu-id="e737c-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="e737c-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="e737c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e737c-102">SYNOPSIS</span></span>
<span data-ttu-id="e737c-103">Az engedélyezett virtuálisgép-méretekre vonatkozó házirendet állítja be a DevTest Labs-ban.</span><span class="sxs-lookup"><span data-stu-id="e737c-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="e737c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e737c-104">SYNTAX</span></span>

### <span data-ttu-id="e737c-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e737c-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e737c-106">Megbénít</span><span class="sxs-lookup"><span data-stu-id="e737c-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e737c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e737c-107">DESCRIPTION</span></span>
<span data-ttu-id="e737c-108">A **set-AzDtlAllowedVMSizesPolicy** parancsmag az engedélyezett virtuálisgép-méretekre vonatkozó házirendet adja meg, amely a laboratóriumban engedélyezett virtuális gépek méreteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e737c-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="e737c-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításához.</span><span class="sxs-lookup"><span data-stu-id="e737c-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="e737c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e737c-110">EXAMPLES</span></span>

## <span data-ttu-id="e737c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e737c-111">PARAMETERS</span></span>

### <span data-ttu-id="e737c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e737c-112">-DefaultProfile</span></span>
<span data-ttu-id="e737c-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e737c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e737c-114">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="e737c-114">-Disable</span></span>
<span data-ttu-id="e737c-115">Jelzi, hogy ez a parancsmag letiltja a házirendet.</span><span class="sxs-lookup"><span data-stu-id="e737c-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e737c-116">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="e737c-116">-Enable</span></span>
<span data-ttu-id="e737c-117">Jelzi, hogy ez a parancsmag engedélyezi a házirendet.</span><span class="sxs-lookup"><span data-stu-id="e737c-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e737c-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="e737c-118">-LabName</span></span>
<span data-ttu-id="e737c-119">Annak a laboratóriumnak a neve, amelyhez a parancsmag a virtuális gép méretére vonatkozó házirendet állítja be.</span><span class="sxs-lookup"><span data-stu-id="e737c-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="e737c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e737c-120">-ResourceGroupName</span></span>
<span data-ttu-id="e737c-121">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="e737c-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e737c-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="e737c-122">-VmSizes</span></span>
<span data-ttu-id="e737c-123">Karakterláncként adja meg a laboratóriumban engedélyezett virtuális számítógép-méretek listáját.</span><span class="sxs-lookup"><span data-stu-id="e737c-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e737c-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e737c-124">-Confirm</span></span>
<span data-ttu-id="e737c-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e737c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e737c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e737c-126">-WhatIf</span></span>
<span data-ttu-id="e737c-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e737c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e737c-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e737c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e737c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e737c-129">CommonParameters</span></span>
<span data-ttu-id="e737c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e737c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e737c-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e737c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e737c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e737c-132">INPUTS</span></span>

### <span data-ttu-id="e737c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e737c-133">System.String</span></span>

## <span data-ttu-id="e737c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e737c-134">OUTPUTS</span></span>

### <span data-ttu-id="e737c-135">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="e737c-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="e737c-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e737c-136">NOTES</span></span>

## <span data-ttu-id="e737c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e737c-137">RELATED LINKS</span></span>

[<span data-ttu-id="e737c-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="e737c-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3e06b4f1236863e208a167024e9d0562dc82ca89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185540"
---
# <span data-ttu-id="4f84a-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="4f84a-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="4f84a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f84a-102">SYNOPSIS</span></span>
<span data-ttu-id="4f84a-103">A DevTest Labs-ban egy Lab virtuális számítógépekre vonatkozó házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="4f84a-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="4f84a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f84a-104">SYNTAX</span></span>

### <span data-ttu-id="4f84a-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4f84a-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f84a-106">Megbénít</span><span class="sxs-lookup"><span data-stu-id="4f84a-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f84a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f84a-107">DESCRIPTION</span></span>
<span data-ttu-id="4f84a-108">A **set-AzDtlVMsPerLabPolicy** parancsmag egy Lab virtuális számítógépeit állítja be, amely a laboratóriumban engedélyezett virtuális gépek teljes számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f84a-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="4f84a-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításához.</span><span class="sxs-lookup"><span data-stu-id="4f84a-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="4f84a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4f84a-110">EXAMPLES</span></span>

## <span data-ttu-id="4f84a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f84a-111">PARAMETERS</span></span>

### <span data-ttu-id="4f84a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f84a-112">-DefaultProfile</span></span>
<span data-ttu-id="4f84a-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4f84a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f84a-114">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="4f84a-114">-Disable</span></span>
<span data-ttu-id="4f84a-115">Jelzi, hogy ez a parancsmag letiltja a Lab házirendjét.</span><span class="sxs-lookup"><span data-stu-id="4f84a-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="4f84a-116">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="4f84a-116">-Enable</span></span>
<span data-ttu-id="4f84a-117">Jelzi, hogy ez a parancsmag engedélyezi a Lab házirendjét.</span><span class="sxs-lookup"><span data-stu-id="4f84a-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="4f84a-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="4f84a-118">-LabName</span></span>
<span data-ttu-id="4f84a-119">Annak a laboratóriumnak a nevét adja meg, amelynek a parancsmagja a virtuális gépeket egy Lab-házirend szerint állítja be.</span><span class="sxs-lookup"><span data-stu-id="4f84a-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="4f84a-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="4f84a-120">-MaxVMs</span></span>
<span data-ttu-id="4f84a-121">A laboratóriumban létrehozható virtuális gépek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f84a-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f84a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f84a-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f84a-123">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="4f84a-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="4f84a-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4f84a-124">-Confirm</span></span>
<span data-ttu-id="4f84a-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4f84a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f84a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f84a-126">-WhatIf</span></span>
<span data-ttu-id="4f84a-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4f84a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f84a-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4f84a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f84a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f84a-129">CommonParameters</span></span>
<span data-ttu-id="4f84a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f84a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f84a-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f84a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f84a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f84a-132">INPUTS</span></span>

### <span data-ttu-id="4f84a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4f84a-133">System.String</span></span>

## <span data-ttu-id="4f84a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f84a-134">OUTPUTS</span></span>

### <span data-ttu-id="4f84a-135">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="4f84a-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="4f84a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f84a-136">NOTES</span></span>

## <span data-ttu-id="4f84a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f84a-137">RELATED LINKS</span></span>

[<span data-ttu-id="4f84a-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="4f84a-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)



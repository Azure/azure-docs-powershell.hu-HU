---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 48f9e2a91923fa123b54b5ebf09abbb7cd64a1dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024019"
---
# <span data-ttu-id="32652-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="32652-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="32652-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32652-102">SYNOPSIS</span></span>
<span data-ttu-id="32652-103">A DevTest Labs-ban egy Lab virtuális gép felhasználónként házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="32652-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="32652-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32652-104">SYNTAX</span></span>

### <span data-ttu-id="32652-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="32652-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32652-106">Megbénít</span><span class="sxs-lookup"><span data-stu-id="32652-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32652-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="32652-107">DESCRIPTION</span></span>
<span data-ttu-id="32652-108">A **set-AzDtlVMsPerUserPolicy** parancsmag egy Lab virtuális gép felhasználónként való beállítását állítja be, amely a felhasználónként engedélyezett virtuális gépek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="32652-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="32652-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításához.</span><span class="sxs-lookup"><span data-stu-id="32652-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="32652-110">Példák</span><span class="sxs-lookup"><span data-stu-id="32652-110">EXAMPLES</span></span>

## <span data-ttu-id="32652-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32652-111">PARAMETERS</span></span>

### <span data-ttu-id="32652-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32652-112">-DefaultProfile</span></span>
<span data-ttu-id="32652-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="32652-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32652-114">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="32652-114">-Disable</span></span>
<span data-ttu-id="32652-115">Jelzi, hogy ez a parancsmag letiltja a Lab házirendet.</span><span class="sxs-lookup"><span data-stu-id="32652-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="32652-116">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="32652-116">-Enable</span></span>
<span data-ttu-id="32652-117">Azt jelzi, hogy ez a parancsmag engedélyezi a Lab házirendet.</span><span class="sxs-lookup"><span data-stu-id="32652-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="32652-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="32652-118">-LabName</span></span>
<span data-ttu-id="32652-119">Annak a laboratóriumnak a nevét adja meg, amelynek a parancsmagja a virtuális gépek felhasználónkénti házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="32652-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="32652-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="32652-120">-MaxVMs</span></span>
<span data-ttu-id="32652-121">A laboratóriumban létrehozható virtuális gépek maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="32652-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="32652-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32652-122">-ResourceGroupName</span></span>
<span data-ttu-id="32652-123">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="32652-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="32652-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="32652-124">-Confirm</span></span>
<span data-ttu-id="32652-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="32652-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32652-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32652-126">-WhatIf</span></span>
<span data-ttu-id="32652-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="32652-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32652-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="32652-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32652-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32652-129">CommonParameters</span></span>
<span data-ttu-id="32652-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32652-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32652-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32652-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32652-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32652-132">INPUTS</span></span>

### <span data-ttu-id="32652-133">System. String</span><span class="sxs-lookup"><span data-stu-id="32652-133">System.String</span></span>

## <span data-ttu-id="32652-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32652-134">OUTPUTS</span></span>

### <span data-ttu-id="32652-135">Microsoft. Azure. Command. DevTestLabs. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="32652-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="32652-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32652-136">NOTES</span></span>

## <span data-ttu-id="32652-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32652-137">RELATED LINKS</span></span>

[<span data-ttu-id="32652-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="32652-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)



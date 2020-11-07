---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 4b15f20f9399df277fc2d2a76f7e51c2a7d57d84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666603"
---
# <span data-ttu-id="c3080-101">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="c3080-101">Set-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="c3080-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3080-102">SYNOPSIS</span></span>
<span data-ttu-id="c3080-103">A Lab DevTest Labs automatikus leállítási házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="c3080-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

## <span data-ttu-id="c3080-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3080-104">SYNTAX</span></span>

### <span data-ttu-id="c3080-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3080-105">Enable (Default)</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3080-106">Megbénít</span><span class="sxs-lookup"><span data-stu-id="c3080-106">Disable</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3080-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3080-107">DESCRIPTION</span></span>
<span data-ttu-id="c3080-108">A **set-AzDtlAutoShutdownPolicy** parancsmag egy Lab automatikus leállítási házirendjét állítja be, amely a nap adott időpontjában automatikusan kikapcsolja a laboratóriumban lévő összes virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="c3080-108">The **Set-AzDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="c3080-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításához.</span><span class="sxs-lookup"><span data-stu-id="c3080-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="c3080-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c3080-110">EXAMPLES</span></span>

## <span data-ttu-id="c3080-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3080-111">PARAMETERS</span></span>

### <span data-ttu-id="c3080-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3080-112">-DefaultProfile</span></span>
<span data-ttu-id="c3080-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c3080-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3080-114">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="c3080-114">-Disable</span></span>
<span data-ttu-id="c3080-115">Azt jelzi, hogy a parancsmag letiltja a házirendet a laboratóriumban.</span><span class="sxs-lookup"><span data-stu-id="c3080-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

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

### <span data-ttu-id="c3080-116">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="c3080-116">-Enable</span></span>
<span data-ttu-id="c3080-117">Azt jelzi, hogy a parancsmag engedélyezi a házirendet a laboratóriumban.</span><span class="sxs-lookup"><span data-stu-id="c3080-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

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

### <span data-ttu-id="c3080-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="c3080-118">-LabName</span></span>
<span data-ttu-id="c3080-119">Annak a laboratóriumnak a neve, amelyhez ez a parancsmag állítja be az automatikus leállítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="c3080-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="c3080-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3080-120">-ResourceGroupName</span></span>
<span data-ttu-id="c3080-121">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="c3080-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="c3080-122">-Idő</span><span class="sxs-lookup"><span data-stu-id="c3080-122">-Time</span></span>
<span data-ttu-id="c3080-123">Itt adhatja meg **datetime** -objektumként azt az időpontot, amikor a laboratóriumban lévő virtuális gépeket le kell állítani.</span><span class="sxs-lookup"><span data-stu-id="c3080-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3080-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3080-124">-Confirm</span></span>
<span data-ttu-id="c3080-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3080-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3080-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3080-126">-WhatIf</span></span>
<span data-ttu-id="c3080-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3080-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3080-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3080-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3080-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3080-129">CommonParameters</span></span>
<span data-ttu-id="c3080-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3080-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3080-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3080-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3080-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3080-132">INPUTS</span></span>

### <span data-ttu-id="c3080-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c3080-133">System.String</span></span>

## <span data-ttu-id="c3080-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3080-134">OUTPUTS</span></span>

### <span data-ttu-id="c3080-135">Microsoft. Azure. Command. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="c3080-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="c3080-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3080-136">NOTES</span></span>

## <span data-ttu-id="c3080-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3080-137">RELATED LINKS</span></span>

[<span data-ttu-id="c3080-138">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="c3080-138">Get-AzDtlAutoShutdownPolicy</span></span>](./Get-AzDtlAutoShutdownPolicy.md)



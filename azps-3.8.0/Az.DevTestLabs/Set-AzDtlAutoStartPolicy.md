---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 7031aaa5a0e5655f933beadbb51569aba0adbef1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012387"
---
# <span data-ttu-id="daac7-101">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="daac7-101">Set-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="daac7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="daac7-102">SYNOPSIS</span></span>
<span data-ttu-id="daac7-103">Egy Lab automatikus indítási házirendjét állítja be a DevTest Labs-ban.</span><span class="sxs-lookup"><span data-stu-id="daac7-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="daac7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="daac7-104">SYNTAX</span></span>

### <span data-ttu-id="daac7-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="daac7-105">Enable (Default)</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="daac7-106">Megbénít</span><span class="sxs-lookup"><span data-stu-id="daac7-106">Disable</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="daac7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="daac7-107">DESCRIPTION</span></span>
<span data-ttu-id="daac7-108">A **set-AzDtlAutoStartPolicy** parancsmag egy Lab automatikus indítási házirendjét állítja be, amely lehetővé teszi, hogy a laboratóriumban futó virtuális gépek az automatikus indításra legyenek ütemezve.</span><span class="sxs-lookup"><span data-stu-id="daac7-108">The **Set-AzDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="daac7-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításához.</span><span class="sxs-lookup"><span data-stu-id="daac7-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="daac7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="daac7-110">EXAMPLES</span></span>

## <span data-ttu-id="daac7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="daac7-111">PARAMETERS</span></span>

### <span data-ttu-id="daac7-112">-Days</span><span class="sxs-lookup"><span data-stu-id="daac7-112">-Days</span></span>
<span data-ttu-id="daac7-113">A hét azon napjait adja meg tömbként, amikor a Lab virtuális számítógépeit el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="daac7-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daac7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daac7-114">-DefaultProfile</span></span>
<span data-ttu-id="daac7-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="daac7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="daac7-116">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="daac7-116">-Disable</span></span>
<span data-ttu-id="daac7-117">Jelzi, hogy ez a parancsmag letiltja a tesztkörnyezetben a virtuális gépekre vonatkozó házirendet.</span><span class="sxs-lookup"><span data-stu-id="daac7-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="daac7-118">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="daac7-118">-Enable</span></span>
<span data-ttu-id="daac7-119">Jelzi, hogy ez a parancsmag engedélyezi a tesztkörnyezetben a virtuális gépek házirendjét.</span><span class="sxs-lookup"><span data-stu-id="daac7-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="daac7-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="daac7-120">-LabName</span></span>
<span data-ttu-id="daac7-121">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag állítja be az automatikus indítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="daac7-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="daac7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daac7-122">-ResourceGroupName</span></span>
<span data-ttu-id="daac7-123">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="daac7-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="daac7-124">-Idő</span><span class="sxs-lookup"><span data-stu-id="daac7-124">-Time</span></span>
<span data-ttu-id="daac7-125">Meghatározza, hogy mikor kell elindítani a Lab virtuális számítógépeit.</span><span class="sxs-lookup"><span data-stu-id="daac7-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="daac7-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="daac7-126">-Confirm</span></span>
<span data-ttu-id="daac7-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="daac7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daac7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daac7-128">-WhatIf</span></span>
<span data-ttu-id="daac7-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="daac7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daac7-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="daac7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daac7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daac7-131">CommonParameters</span></span>
<span data-ttu-id="daac7-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="daac7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daac7-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daac7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daac7-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="daac7-134">INPUTS</span></span>

### <span data-ttu-id="daac7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="daac7-135">System.String</span></span>

## <span data-ttu-id="daac7-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="daac7-136">OUTPUTS</span></span>

### <span data-ttu-id="daac7-137">Microsoft. Azure. Command. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="daac7-137">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="daac7-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="daac7-138">NOTES</span></span>

## <span data-ttu-id="daac7-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="daac7-139">RELATED LINKS</span></span>

[<span data-ttu-id="daac7-140">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="daac7-140">Get-AzDtlAutoStartPolicy</span></span>](./Get-AzDtlAutoStartPolicy.md)



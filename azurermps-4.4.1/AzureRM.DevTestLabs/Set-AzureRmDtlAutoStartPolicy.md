---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: a1efa9159bbe318a1de0360a3f70f197660db535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679445"
---
# <span data-ttu-id="2ab40-101">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="2ab40-101">Set-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="2ab40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ab40-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab40-103">Egy Lab automatikus indítási házirendjét állítja be a DevTest Labs-ban.</span><span class="sxs-lookup"><span data-stu-id="2ab40-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ab40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ab40-104">SYNTAX</span></span>

### <span data-ttu-id="2ab40-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ab40-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ab40-106">Megbénít</span><span class="sxs-lookup"><span data-stu-id="2ab40-106">Disable</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ab40-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ab40-107">DESCRIPTION</span></span>
<span data-ttu-id="2ab40-108">A **set-AzureRmDtlAutoStartPolicy** parancsmag egy Lab automatikus indítási házirendjét állítja be, amely lehetővé teszi, hogy a laboratóriumban futó virtuális gépek az automatikus indításra legyenek ütemezve.</span><span class="sxs-lookup"><span data-stu-id="2ab40-108">The **Set-AzureRmDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="2ab40-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításához.</span><span class="sxs-lookup"><span data-stu-id="2ab40-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="2ab40-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2ab40-110">EXAMPLES</span></span>

## <span data-ttu-id="2ab40-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ab40-111">PARAMETERS</span></span>

### <span data-ttu-id="2ab40-112">-Days</span><span class="sxs-lookup"><span data-stu-id="2ab40-112">-Days</span></span>
<span data-ttu-id="2ab40-113">A hét azon napjait adja meg tömbként, amikor a Lab virtuális számítógépeit el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="2ab40-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="2ab40-114">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="2ab40-114">-Disable</span></span>
<span data-ttu-id="2ab40-115">Jelzi, hogy ez a parancsmag letiltja a tesztkörnyezetben a virtuális gépekre vonatkozó házirendet.</span><span class="sxs-lookup"><span data-stu-id="2ab40-115">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="2ab40-116">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="2ab40-116">-Enable</span></span>
<span data-ttu-id="2ab40-117">Jelzi, hogy ez a parancsmag engedélyezi a tesztkörnyezetben a virtuális gépek házirendjét.</span><span class="sxs-lookup"><span data-stu-id="2ab40-117">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="2ab40-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="2ab40-118">-LabName</span></span>
<span data-ttu-id="2ab40-119">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag állítja be az automatikus indítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="2ab40-119">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="2ab40-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ab40-120">-ResourceGroupName</span></span>
<span data-ttu-id="2ab40-121">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="2ab40-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="2ab40-122">-Idő</span><span class="sxs-lookup"><span data-stu-id="2ab40-122">-Time</span></span>
<span data-ttu-id="2ab40-123">Meghatározza, hogy mikor kell elindítani a Lab virtuális számítógépeit.</span><span class="sxs-lookup"><span data-stu-id="2ab40-123">Specifies the time when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="2ab40-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2ab40-124">-Confirm</span></span>
<span data-ttu-id="2ab40-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ab40-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ab40-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ab40-126">-WhatIf</span></span>
<span data-ttu-id="2ab40-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2ab40-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ab40-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ab40-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ab40-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab40-129">-DefaultProfile</span></span>
<span data-ttu-id="2ab40-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ab40-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab40-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab40-131">CommonParameters</span></span>
<span data-ttu-id="2ab40-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ab40-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab40-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ab40-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab40-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ab40-134">INPUTS</span></span>

## <span data-ttu-id="2ab40-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ab40-135">OUTPUTS</span></span>

### <span data-ttu-id="2ab40-136">Microsoft. Azure. Command. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="2ab40-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="2ab40-137">Ez a parancsmag azt az ütemtervet adja eredményül, amely meghatározza, hogy mikor kell elindítani a Lab virtuális számítógépeit.</span><span class="sxs-lookup"><span data-stu-id="2ab40-137">This cmdlet returns the schedule that specifies when the virtual machines of the lab must be started.</span></span>

## <span data-ttu-id="2ab40-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ab40-138">NOTES</span></span>

## <span data-ttu-id="2ab40-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ab40-139">RELATED LINKS</span></span>

[<span data-ttu-id="2ab40-140">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="2ab40-140">Get-AzureRmDtlAutoStartPolicy</span></span>](./Get-AzureRmDtlAutoStartPolicy.md)



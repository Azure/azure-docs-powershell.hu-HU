---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: 000c9f2748bd1f80559d9fc80c206e4f1c9bf0c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678994"
---
# <span data-ttu-id="b9d52-101">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="b9d52-101">Set-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="b9d52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9d52-102">SYNOPSIS</span></span>
<span data-ttu-id="b9d52-103">Egy Lab automatikus indítási házirendjét állítja be a DevTest Labs-ban.</span><span class="sxs-lookup"><span data-stu-id="b9d52-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9d52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9d52-104">SYNTAX</span></span>

### <span data-ttu-id="b9d52-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b9d52-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9d52-106">Megbénít</span><span class="sxs-lookup"><span data-stu-id="b9d52-106">Disable</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9d52-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9d52-107">DESCRIPTION</span></span>
<span data-ttu-id="b9d52-108">A **set-AzureRmDtlAutoStartPolicy** parancsmag egy Lab automatikus indítási házirendjét állítja be, amely lehetővé teszi, hogy a laboratóriumban futó virtuális gépek az automatikus indításra legyenek ütemezve.</span><span class="sxs-lookup"><span data-stu-id="b9d52-108">The **Set-AzureRmDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="b9d52-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításához.</span><span class="sxs-lookup"><span data-stu-id="b9d52-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="b9d52-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b9d52-110">EXAMPLES</span></span>

## <span data-ttu-id="b9d52-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9d52-111">PARAMETERS</span></span>

### <span data-ttu-id="b9d52-112">-Days</span><span class="sxs-lookup"><span data-stu-id="b9d52-112">-Days</span></span>
<span data-ttu-id="b9d52-113">A hét azon napjait adja meg tömbként, amikor a Lab virtuális számítógépeit el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="b9d52-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: DayOfWeek[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9d52-114">-DefaultProfile</span></span>
<span data-ttu-id="b9d52-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b9d52-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d52-116">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="b9d52-116">-Disable</span></span>
<span data-ttu-id="b9d52-117">Jelzi, hogy ez a parancsmag letiltja a tesztkörnyezetben a virtuális gépekre vonatkozó házirendet.</span><span class="sxs-lookup"><span data-stu-id="b9d52-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d52-118">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="b9d52-118">-Enable</span></span>
<span data-ttu-id="b9d52-119">Jelzi, hogy ez a parancsmag engedélyezi a tesztkörnyezetben a virtuális gépek házirendjét.</span><span class="sxs-lookup"><span data-stu-id="b9d52-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d52-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="b9d52-120">-LabName</span></span>
<span data-ttu-id="b9d52-121">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag állítja be az automatikus indítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="b9d52-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d52-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9d52-122">-ResourceGroupName</span></span>
<span data-ttu-id="b9d52-123">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="b9d52-123">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9d52-124">-Idő</span><span class="sxs-lookup"><span data-stu-id="b9d52-124">-Time</span></span>
<span data-ttu-id="b9d52-125">Meghatározza, hogy mikor kell elindítani a Lab virtuális számítógépeit.</span><span class="sxs-lookup"><span data-stu-id="b9d52-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d52-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9d52-126">-Confirm</span></span>
<span data-ttu-id="b9d52-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9d52-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d52-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9d52-128">-WhatIf</span></span>
<span data-ttu-id="b9d52-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9d52-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9d52-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9d52-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d52-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9d52-131">CommonParameters</span></span>
<span data-ttu-id="b9d52-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9d52-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9d52-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9d52-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9d52-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9d52-134">INPUTS</span></span>

### <span data-ttu-id="b9d52-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="b9d52-135">None</span></span>
<span data-ttu-id="b9d52-136">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b9d52-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9d52-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9d52-137">OUTPUTS</span></span>

### <span data-ttu-id="b9d52-138">Microsoft. Azure. Command. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="b9d52-138">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="b9d52-139">Ez a parancsmag azt az ütemtervet adja eredményül, amely meghatározza, hogy mikor kell elindítani a Lab virtuális számítógépeit.</span><span class="sxs-lookup"><span data-stu-id="b9d52-139">This cmdlet returns the schedule that specifies when the virtual machines of the lab must be started.</span></span>

## <span data-ttu-id="b9d52-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9d52-140">NOTES</span></span>

## <span data-ttu-id="b9d52-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9d52-141">RELATED LINKS</span></span>

[<span data-ttu-id="b9d52-142">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="b9d52-142">Get-AzureRmDtlAutoStartPolicy</span></span>](./Get-AzureRmDtlAutoStartPolicy.md)



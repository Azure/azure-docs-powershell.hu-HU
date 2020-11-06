---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: d812d66911c31297a2aaf4a32fd73562bc4ae9b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501880"
---
# <span data-ttu-id="5876a-101">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="5876a-101">Set-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="5876a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5876a-102">SYNOPSIS</span></span>
<span data-ttu-id="5876a-103">A Lab DevTest Labs automatikus leállítási házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="5876a-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5876a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5876a-104">SYNTAX</span></span>

### <span data-ttu-id="5876a-105">Engedélyezés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5876a-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5876a-106">Megbénít</span><span class="sxs-lookup"><span data-stu-id="5876a-106">Disable</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5876a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5876a-107">DESCRIPTION</span></span>
<span data-ttu-id="5876a-108">A **set-AzureRmDtlAutoShutdownPolicy** parancsmag egy Lab automatikus leállítási házirendjét állítja be, amely a nap adott időpontjában automatikusan kikapcsolja a laboratóriumban lévő összes virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="5876a-108">The **Set-AzureRmDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="5876a-109">A parancsmag a megadott erőforráscsoportot és a laboratórium nevét használja a házirend beállításához.</span><span class="sxs-lookup"><span data-stu-id="5876a-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="5876a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5876a-110">EXAMPLES</span></span>

## <span data-ttu-id="5876a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5876a-111">PARAMETERS</span></span>

### <span data-ttu-id="5876a-112">-Letiltása</span><span class="sxs-lookup"><span data-stu-id="5876a-112">-Disable</span></span>
<span data-ttu-id="5876a-113">Azt jelzi, hogy a parancsmag letiltja a házirendet a laboratóriumban.</span><span class="sxs-lookup"><span data-stu-id="5876a-113">Indicates that the cmdlet disables the policy in the lab.</span></span>

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

### <span data-ttu-id="5876a-114">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="5876a-114">-Enable</span></span>
<span data-ttu-id="5876a-115">Azt jelzi, hogy a parancsmag engedélyezi a házirendet a laboratóriumban.</span><span class="sxs-lookup"><span data-stu-id="5876a-115">Indicates that the cmdlet enables the policy in the lab.</span></span>

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

### <span data-ttu-id="5876a-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="5876a-116">-LabName</span></span>
<span data-ttu-id="5876a-117">Annak a laboratóriumnak a neve, amelyhez ez a parancsmag állítja be az automatikus leállítási házirendet.</span><span class="sxs-lookup"><span data-stu-id="5876a-117">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="5876a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5876a-118">-ResourceGroupName</span></span>
<span data-ttu-id="5876a-119">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="5876a-119">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="5876a-120">-Idő</span><span class="sxs-lookup"><span data-stu-id="5876a-120">-Time</span></span>
<span data-ttu-id="5876a-121">Itt adhatja meg **datetime** -objektumként azt az időpontot, amikor a laboratóriumban lévő virtuális gépeket le kell állítani.</span><span class="sxs-lookup"><span data-stu-id="5876a-121">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

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

### <span data-ttu-id="5876a-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5876a-122">-Confirm</span></span>
<span data-ttu-id="5876a-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5876a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5876a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5876a-124">-WhatIf</span></span>
<span data-ttu-id="5876a-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5876a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5876a-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5876a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5876a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5876a-127">-DefaultProfile</span></span>
<span data-ttu-id="5876a-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5876a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5876a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5876a-129">CommonParameters</span></span>
<span data-ttu-id="5876a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5876a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5876a-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5876a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5876a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5876a-132">INPUTS</span></span>

## <span data-ttu-id="5876a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5876a-133">OUTPUTS</span></span>

### <span data-ttu-id="5876a-134">Microsoft. Azure. Command. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="5876a-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="5876a-135">Ez a parancsmag azt az ütemezést adja eredményül, amely meghatározza, hogy a laboratóriumban milyen virtuális gépeket kell leállítani.</span><span class="sxs-lookup"><span data-stu-id="5876a-135">This cmdlet returns the schedule which specifies when the virtual machines in the lab must shut down.</span></span>

## <span data-ttu-id="5876a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5876a-136">NOTES</span></span>

## <span data-ttu-id="5876a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5876a-137">RELATED LINKS</span></span>

[<span data-ttu-id="5876a-138">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="5876a-138">Get-AzureRmDtlAutoShutdownPolicy</span></span>](./Get-AzureRmDtlAutoShutdownPolicy.md)



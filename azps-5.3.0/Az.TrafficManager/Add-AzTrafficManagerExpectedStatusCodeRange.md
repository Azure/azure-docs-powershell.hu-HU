---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: ee249b7e3d811a527a9322e09ba65075883e73b6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382954"
---
# <span data-ttu-id="cc079-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="cc079-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="cc079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc079-102">SYNOPSIS</span></span>
<span data-ttu-id="cc079-103">Egy várható állapotkód-tartomány hozzáadása egy helyi Traffic Manager-profilobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="cc079-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="cc079-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cc079-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc079-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cc079-105">DESCRIPTION</span></span>
<span data-ttu-id="cc079-106">Az **Add-AzTrafficManagerExpectedStatusCodeRange** parancsmag egy várható állapotkód-tartományt ad egy helyi Azure Traffic Manager-profilobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="cc079-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="cc079-107">A profilt a New-AzTrafficManagerProfile vagy Get-AzTrafficManagerProfile használhatja.</span><span class="sxs-lookup"><span data-stu-id="cc079-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="cc079-108">Ez a parancsmag a helyi profilobjektumon működik.</span><span class="sxs-lookup"><span data-stu-id="cc079-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="cc079-109">A Forgalomkezelőben a módosításokat a Set-AzTrafficManagerProfile el.</span><span class="sxs-lookup"><span data-stu-id="cc079-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="cc079-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cc079-110">EXAMPLES</span></span>

### <span data-ttu-id="cc079-111">1. példa: Várt állapotkód-tartomány hozzáadása profilhoz</span><span class="sxs-lookup"><span data-stu-id="cc079-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="cc079-112">Az első parancs a **Get-AzTrafficManagerProfile** parancsmag használatával kap egy Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="cc079-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="cc079-113">A parancs a helyi profilt a $TrafficManagerProfile tárolja.</span><span class="sxs-lookup"><span data-stu-id="cc079-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="cc079-114">A második parancs egy várt állapotkód-tartományt ad hozzá a $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="cc079-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="cc079-115">Az utolsó parancs frissíti a Traffic Managerben a profilt úgy, hogy megfeleljen a helyi $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="cc079-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="cc079-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc079-116">PARAMETERS</span></span>

### <span data-ttu-id="cc079-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc079-117">-DefaultProfile</span></span>
<span data-ttu-id="cc079-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc079-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc079-119">-Max</span><span class="sxs-lookup"><span data-stu-id="cc079-119">-Max</span></span>
<span data-ttu-id="cc079-120">A hozzáadható állapotkód-tartomány legmagasabb értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc079-120">Specifies the highest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc079-121">-Min</span><span class="sxs-lookup"><span data-stu-id="cc079-121">-Min</span></span>
<span data-ttu-id="cc079-122">A hozzáadható állapotkód-tartomány legalacsonyabb értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc079-122">Specifies the lowest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc079-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cc079-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="cc079-124">Helyi **TrafficManagerProfile objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="cc079-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="cc079-125">Ez a parancsmag módosítja ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="cc079-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="cc079-126">A **TrafficManagerProfile** objektum beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cc079-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc079-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc079-127">-Confirm</span></span>
<span data-ttu-id="cc079-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cc079-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc079-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc079-129">-WhatIf</span></span>
<span data-ttu-id="cc079-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cc079-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc079-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc079-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc079-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc079-132">CommonParameters</span></span>
<span data-ttu-id="cc079-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc079-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc079-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc079-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc079-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc079-135">INPUTS</span></span>

### <span data-ttu-id="cc079-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cc079-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="cc079-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc079-137">OUTPUTS</span></span>

### <span data-ttu-id="cc079-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cc079-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="cc079-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cc079-139">NOTES</span></span>

## <span data-ttu-id="cc079-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc079-140">RELATED LINKS</span></span>

[<span data-ttu-id="cc079-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="cc079-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="cc079-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cc079-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="cc079-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cc079-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

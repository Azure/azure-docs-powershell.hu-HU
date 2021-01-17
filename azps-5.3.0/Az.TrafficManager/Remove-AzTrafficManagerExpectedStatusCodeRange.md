---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: fdada94847fdf2f83141f7cca63da61ead6fcd2c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382786"
---
# <span data-ttu-id="78684-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="78684-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="78684-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78684-102">SYNOPSIS</span></span>
<span data-ttu-id="78684-103">Eltávolít egy várható állapotkód-tartományt egy helyi Traffic Manager-profilobjektumból.</span><span class="sxs-lookup"><span data-stu-id="78684-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="78684-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="78684-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78684-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="78684-105">DESCRIPTION</span></span>
<span data-ttu-id="78684-106">A **Remove-AzTrafficManagerExpectedStatusCodeRange** parancsmag eltávolítja a várt állapotkódok tartományát egy helyi Azure Traffic Manager-profilobjektumból.</span><span class="sxs-lookup"><span data-stu-id="78684-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="78684-107">A profilt a New-AzTrafficManagerProfile vagy Get-AzTrafficManagerProfile használhatja.</span><span class="sxs-lookup"><span data-stu-id="78684-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="78684-108">Ez a parancsmag a helyi profilobjektumon működik.</span><span class="sxs-lookup"><span data-stu-id="78684-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="78684-109">A Forgalomkezelőben a módosításokat a Set-AzTrafficManagerProfile el.</span><span class="sxs-lookup"><span data-stu-id="78684-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="78684-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="78684-110">EXAMPLES</span></span>

### <span data-ttu-id="78684-111">1. példa: Egy várt állapotkód-tartomány eltávolítása egy profilból</span><span class="sxs-lookup"><span data-stu-id="78684-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="78684-112">Az első parancs a **Get-AzTrafficManagerProfile** parancsmag használatával kap egy Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="78684-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="78684-113">A második parancs eltávolítja a várt állapotkód-tartományt a $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="78684-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="78684-114">Az utolsó parancs frissíti a Traffic Managerben a profilt úgy, hogy megfeleljen a helyi $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="78684-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="78684-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78684-115">PARAMETERS</span></span>

### <span data-ttu-id="78684-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78684-116">-DefaultProfile</span></span>
<span data-ttu-id="78684-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78684-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78684-118">-Min</span><span class="sxs-lookup"><span data-stu-id="78684-118">-Min</span></span>
<span data-ttu-id="78684-119">Az eltávolítható állapotkód-tartomány legalacsonyabb értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78684-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="78684-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78684-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="78684-121">Helyi **TrafficManagerProfile objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="78684-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="78684-122">Ez a parancsmag módosítja ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="78684-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="78684-123">A **TrafficManagerProfile** objektum beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="78684-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="78684-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78684-124">-Confirm</span></span>
<span data-ttu-id="78684-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="78684-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78684-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78684-126">-WhatIf</span></span>
<span data-ttu-id="78684-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="78684-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78684-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78684-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78684-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78684-129">CommonParameters</span></span>
<span data-ttu-id="78684-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78684-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78684-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78684-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78684-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78684-132">INPUTS</span></span>

### <span data-ttu-id="78684-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78684-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="78684-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78684-134">OUTPUTS</span></span>

### <span data-ttu-id="78684-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78684-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="78684-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="78684-136">NOTES</span></span>

## <span data-ttu-id="78684-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78684-137">RELATED LINKS</span></span>

[<span data-ttu-id="78684-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="78684-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="78684-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78684-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="78684-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78684-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

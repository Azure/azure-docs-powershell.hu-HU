---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: 62dbdfe69feddcbd942a51c05c65e486653a2405
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382800"
---
# <span data-ttu-id="1f94e-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="1f94e-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="1f94e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f94e-102">SYNOPSIS</span></span>
<span data-ttu-id="1f94e-103">Eltávolítja az egyéni fejlécadatokat egy helyi Traffic Manager-profilobjektumból.</span><span class="sxs-lookup"><span data-stu-id="1f94e-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="1f94e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1f94e-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f94e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1f94e-105">DESCRIPTION</span></span>
<span data-ttu-id="1f94e-106">A **Remove-AzTrafficManagerCustomHeaderFromProfile** parancsmag eltávolítja az egyéni fejlécadatokat a helyi Azure Traffic Manager-profilobjektumból.</span><span class="sxs-lookup"><span data-stu-id="1f94e-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="1f94e-107">A profilt a New-AzTrafficManagerProfile vagy Get-AzTrafficManagerProfile használhatja.</span><span class="sxs-lookup"><span data-stu-id="1f94e-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="1f94e-108">Ez a parancsmag a helyi profilobjektumon működik.</span><span class="sxs-lookup"><span data-stu-id="1f94e-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="1f94e-109">A Forgalomkezelőben a módosításokat a Set-AzTrafficManagerProfile el.</span><span class="sxs-lookup"><span data-stu-id="1f94e-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="1f94e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1f94e-110">EXAMPLES</span></span>

### <span data-ttu-id="1f94e-111">1. példa: Egyéni fejlécinformációk eltávolítása egy profilból</span><span class="sxs-lookup"><span data-stu-id="1f94e-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="1f94e-112">Az első parancs a **Get-AzTrafficManagerProfile** parancsmag használatával kap egy Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="1f94e-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="1f94e-113">A második parancs eltávolítja az egyéni fejlécadatokat a $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1f94e-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="1f94e-114">Az utolsó parancs frissíti a Traffic Managerben a profilt úgy, hogy megfeleljen a helyi $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1f94e-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="1f94e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f94e-115">PARAMETERS</span></span>

### <span data-ttu-id="1f94e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f94e-116">-DefaultProfile</span></span>
<span data-ttu-id="1f94e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f94e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f94e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1f94e-118">-Name</span></span>
<span data-ttu-id="1f94e-119">Az eltávolítható egyéni fejlécinformációk nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f94e-119">Specifies the name of the custom header information to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f94e-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f94e-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="1f94e-121">Helyi **TrafficManagerProfile objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="1f94e-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="1f94e-122">Ez a parancsmag módosítja ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="1f94e-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="1f94e-123">A **TrafficManagerProfile** objektum beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1f94e-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="1f94e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f94e-124">-Confirm</span></span>
<span data-ttu-id="1f94e-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1f94e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f94e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f94e-126">-WhatIf</span></span>
<span data-ttu-id="1f94e-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1f94e-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f94e-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1f94e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f94e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f94e-129">CommonParameters</span></span>
<span data-ttu-id="1f94e-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f94e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f94e-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f94e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f94e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f94e-132">INPUTS</span></span>

### <span data-ttu-id="1f94e-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f94e-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="1f94e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f94e-134">OUTPUTS</span></span>

### <span data-ttu-id="1f94e-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f94e-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="1f94e-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1f94e-136">NOTES</span></span>

## <span data-ttu-id="1f94e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f94e-137">RELATED LINKS</span></span>

[<span data-ttu-id="1f94e-138">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="1f94e-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="1f94e-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f94e-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="1f94e-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1f94e-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

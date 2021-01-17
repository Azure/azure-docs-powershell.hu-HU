---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: b90e83a403be59f5c454c0c055f0fe4719c3116f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382982"
---
# <span data-ttu-id="36f0b-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="36f0b-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="36f0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="36f0b-103">Egyéni fejlécadatokat ad hozzá egy helyi Traffic Manager-profilobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="36f0b-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="36f0b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36f0b-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36f0b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36f0b-105">DESCRIPTION</span></span>
<span data-ttu-id="36f0b-106">Az **Add-AzTrafficManagerCustomHeaderToProfile** parancsmag egyéni fejlécadatokat ad a helyi Azure Traffic Manager-profilobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="36f0b-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="36f0b-107">A profilt a New-AzTrafficManagerProfile vagy Get-AzTrafficManagerProfile használhatja.</span><span class="sxs-lookup"><span data-stu-id="36f0b-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="36f0b-108">Ez a parancsmag a helyi profilobjektumon működik.</span><span class="sxs-lookup"><span data-stu-id="36f0b-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="36f0b-109">A Forgalomkezelőben a módosításokat a Set-AzTrafficManagerProfile el.</span><span class="sxs-lookup"><span data-stu-id="36f0b-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="36f0b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36f0b-110">EXAMPLES</span></span>

### <span data-ttu-id="36f0b-111">1. példa: Egyéni fejléc-információk hozzáadása egy profilhoz</span><span class="sxs-lookup"><span data-stu-id="36f0b-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="36f0b-112">Az első parancs a **Get-AzTrafficManagerProfile** parancsmag használatával kap egy Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="36f0b-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="36f0b-113">A parancs a helyi profilt a $TrafficManagerProfile tárolja.</span><span class="sxs-lookup"><span data-stu-id="36f0b-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="36f0b-114">A második parancs egyéni fejlécadatokat ad hozzá a $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="36f0b-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="36f0b-115">Az utolsó parancs frissíti a Traffic Managerben a profilt úgy, hogy megfeleljen a helyi $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="36f0b-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="36f0b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36f0b-116">PARAMETERS</span></span>

### <span data-ttu-id="36f0b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f0b-117">-DefaultProfile</span></span>
<span data-ttu-id="36f0b-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36f0b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36f0b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="36f0b-119">-Name</span></span>
<span data-ttu-id="36f0b-120">A hozzáadni szükséges egyéni fejléc-információ nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36f0b-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="36f0b-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="36f0b-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="36f0b-122">Helyi **TrafficManagerProfile objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="36f0b-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="36f0b-123">Ez a parancsmag módosítja ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="36f0b-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="36f0b-124">A **TrafficManagerProfile** objektum beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="36f0b-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="36f0b-125">-Érték</span><span class="sxs-lookup"><span data-stu-id="36f0b-125">-Value</span></span>
<span data-ttu-id="36f0b-126">A hozzáadható egyéni fejléc-információ értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36f0b-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="36f0b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36f0b-127">-Confirm</span></span>
<span data-ttu-id="36f0b-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="36f0b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36f0b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36f0b-129">-WhatIf</span></span>
<span data-ttu-id="36f0b-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="36f0b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36f0b-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36f0b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36f0b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f0b-132">CommonParameters</span></span>
<span data-ttu-id="36f0b-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36f0b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f0b-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36f0b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f0b-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36f0b-135">INPUTS</span></span>

### <span data-ttu-id="36f0b-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="36f0b-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="36f0b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36f0b-137">OUTPUTS</span></span>

### <span data-ttu-id="36f0b-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="36f0b-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="36f0b-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36f0b-139">NOTES</span></span>

## <span data-ttu-id="36f0b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36f0b-140">RELATED LINKS</span></span>

[<span data-ttu-id="36f0b-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="36f0b-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="36f0b-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="36f0b-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="36f0b-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="36f0b-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

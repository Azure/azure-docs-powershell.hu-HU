---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 1dac991645d6f57ba4fe30a82955531b7fdb3f5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936457"
---
# <span data-ttu-id="9d77d-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="9d77d-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="9d77d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d77d-102">SYNOPSIS</span></span>
<span data-ttu-id="9d77d-103">Eltávolít egy végpontot egy helyi Traffic Manager-profilobjektumból.</span><span class="sxs-lookup"><span data-stu-id="9d77d-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="9d77d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9d77d-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d77d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9d77d-105">DESCRIPTION</span></span>
<span data-ttu-id="9d77d-106">A **Remove-AzTrafficManagerEndpointConfig** parancsmag eltávolít egy végpontot egy helyi Azure Traffic Manager-profilobjektumból.</span><span class="sxs-lookup"><span data-stu-id="9d77d-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="9d77d-107">A profilt a Get-AzTrafficManagerProfile használhatja.</span><span class="sxs-lookup"><span data-stu-id="9d77d-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="9d77d-108">Ez a parancsmag a helyi profilobjektumon működik.</span><span class="sxs-lookup"><span data-stu-id="9d77d-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="9d77d-109">A Forgalomkezelőben a módosításokat a Set-AzTrafficManagerProfile el.</span><span class="sxs-lookup"><span data-stu-id="9d77d-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="9d77d-110">Egy végpont eltávolításához és a módosítások egyetlen műveletben való véglegesítéshez használja a Remove-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9d77d-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="9d77d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9d77d-111">EXAMPLES</span></span>

### <span data-ttu-id="9d77d-112">1. példa: Végpont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9d77d-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="9d77d-113">Az első parancs a **Get-AzTrafficManagerProfile** parancsmag használatával kap egy Azure Traffic Manager-profilt.</span><span class="sxs-lookup"><span data-stu-id="9d77d-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="9d77d-114">A parancs a helyi profilt a $TrafficManagerProfile tárolja.</span><span class="sxs-lookup"><span data-stu-id="9d77d-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="9d77d-115">A második parancs eltávolítja a contoso nevű Azure-végpontot a $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9d77d-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="9d77d-116">Ez a parancs csak a helyi objektumot módosítja.</span><span class="sxs-lookup"><span data-stu-id="9d77d-116">This command changes only the local object.</span></span>

<span data-ttu-id="9d77d-117">Az utolsó parancs frissíti a ContosoProfile nevű Forgalomkezelő-profilt, hogy megfeleljen a helyi $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9d77d-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="9d77d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d77d-118">PARAMETERS</span></span>

### <span data-ttu-id="9d77d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d77d-119">-DefaultProfile</span></span>
<span data-ttu-id="9d77d-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d77d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d77d-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9d77d-121">-EndpointName</span></span>
<span data-ttu-id="9d77d-122">Annak a Traffic Manager-végpontnak a nevét adja meg, amelyről a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="9d77d-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9d77d-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9d77d-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="9d77d-124">Helyi **TrafficManagerProfile objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="9d77d-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="9d77d-125">Ez a parancsmag módosítja ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="9d77d-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="9d77d-126">A **TrafficManagerProfile** objektum beszerzéséhez használja a Get-AzTrafficManagerProfile parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9d77d-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="9d77d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d77d-127">CommonParameters</span></span>
<span data-ttu-id="9d77d-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d77d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d77d-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d77d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d77d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d77d-130">INPUTS</span></span>

### <span data-ttu-id="9d77d-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9d77d-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9d77d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d77d-132">OUTPUTS</span></span>

### <span data-ttu-id="9d77d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9d77d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9d77d-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9d77d-134">NOTES</span></span>

## <span data-ttu-id="9d77d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d77d-135">RELATED LINKS</span></span>

[<span data-ttu-id="9d77d-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="9d77d-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="9d77d-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9d77d-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="9d77d-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d77d-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9d77d-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9d77d-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)



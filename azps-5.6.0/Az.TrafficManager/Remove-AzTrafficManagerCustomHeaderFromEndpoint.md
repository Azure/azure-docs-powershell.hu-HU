---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: f0d179c82292ffb9300791337f40436c4d4c5f36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936466"
---
# <span data-ttu-id="91c21-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="91c21-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="91c21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91c21-102">SYNOPSIS</span></span>
<span data-ttu-id="91c21-103">Eltávolítja az egyéni fejlécadatokat egy helyi Traffic Manager-végpontobjektumból.</span><span class="sxs-lookup"><span data-stu-id="91c21-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="91c21-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="91c21-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91c21-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="91c21-105">DESCRIPTION</span></span>
<span data-ttu-id="91c21-106">A **Remove-AzTrafficManagerCustomHeaderFromEndpoint** parancsmag eltávolítja az egyéni fejlécadatokat egy helyi Azure Traffic Manager-végpontobjektumból.</span><span class="sxs-lookup"><span data-stu-id="91c21-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="91c21-107">Végpontot a New-AzTrafficManagerEndpoint parancsmagok Get-AzTrafficManagerEndpoint le.</span><span class="sxs-lookup"><span data-stu-id="91c21-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="91c21-108">Ez a parancsmag a helyi végpontobjektumon működik.</span><span class="sxs-lookup"><span data-stu-id="91c21-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="91c21-109">A Módosítások véglegesítése a Forgalomkezelő végpontjára a Set-AzTrafficManagerEndpoint parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="91c21-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="91c21-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="91c21-110">EXAMPLES</span></span>

### <span data-ttu-id="91c21-111">1. példa: Egyéni alhálózati adatok eltávolítása egy végpontról</span><span class="sxs-lookup"><span data-stu-id="91c21-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="91c21-112">Az első parancs a Contoso nevű Azure-végpontot a ResourceGroup11 nevű erőforráscsoport ContosoProfile nevű profiljából kapja meg, majd az objektumot a $TrafficManagerEndpoint tárolja.</span><span class="sxs-lookup"><span data-stu-id="91c21-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="91c21-113">A második parancs eltávolítja az egyéni fejlécadatokat a $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="91c21-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="91c21-114">Az utolsó parancs frissíti a Traffic Managerben a végpontot úgy, hogy megfeleljen a helyi $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="91c21-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="91c21-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91c21-115">PARAMETERS</span></span>

### <span data-ttu-id="91c21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c21-116">-DefaultProfile</span></span>
<span data-ttu-id="91c21-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91c21-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91c21-118">-Name</span><span class="sxs-lookup"><span data-stu-id="91c21-118">-Name</span></span>
<span data-ttu-id="91c21-119">Az eltávolítható egyéni fejlécinformációk nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="91c21-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="91c21-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91c21-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="91c21-121">Helyi **TrafficManagerEndpoint-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="91c21-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="91c21-122">Ez a parancsmag módosítja ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="91c21-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="91c21-123">A **TrafficManagerEndpoint** objektum beszerzéséhez használja a Get-AzTrafficManagerEndpoint vagy New-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="91c21-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91c21-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91c21-124">-Confirm</span></span>
<span data-ttu-id="91c21-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="91c21-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91c21-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91c21-126">-WhatIf</span></span>
<span data-ttu-id="91c21-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="91c21-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91c21-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91c21-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91c21-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c21-129">CommonParameters</span></span>
<span data-ttu-id="91c21-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c21-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c21-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91c21-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c21-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91c21-132">INPUTS</span></span>

### <span data-ttu-id="91c21-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91c21-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="91c21-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91c21-134">OUTPUTS</span></span>

### <span data-ttu-id="91c21-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91c21-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="91c21-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="91c21-136">NOTES</span></span>

## <span data-ttu-id="91c21-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91c21-137">RELATED LINKS</span></span>

[<span data-ttu-id="91c21-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="91c21-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="91c21-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91c21-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="91c21-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91c21-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="91c21-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91c21-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)

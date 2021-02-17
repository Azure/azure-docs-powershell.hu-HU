---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 9a1be7c45c507746ae3b8c97f883a61de0da78db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207535"
---
# <span data-ttu-id="a83fd-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="a83fd-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="a83fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a83fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a83fd-103">Egyéni fejlécadatokat ad egy helyi Traffic Manager-végpontobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="a83fd-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="a83fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a83fd-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a83fd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a83fd-105">DESCRIPTION</span></span>
<span data-ttu-id="a83fd-106">Az **Add-AzTrafficManagerCustomHeaderToEndpoint** parancsmag egyéni fejlécadatokat ad a helyi Azure Traffic Manager-végpontobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="a83fd-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="a83fd-107">Végpontot a New-AzTrafficManagerEndpoint parancsmagok Get-AzTrafficManagerEndpoint le.</span><span class="sxs-lookup"><span data-stu-id="a83fd-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="a83fd-108">Ez a parancsmag a helyi végpontobjektumon működik.</span><span class="sxs-lookup"><span data-stu-id="a83fd-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="a83fd-109">A Módosítások véglegesítése a Forgalomkezelő végpontjára a Set-AzTrafficManagerEndpoint parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="a83fd-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="a83fd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a83fd-110">EXAMPLES</span></span>

### <span data-ttu-id="a83fd-111">1. példa: Egyéni fejléc-információk hozzáadása egy végponthoz</span><span class="sxs-lookup"><span data-stu-id="a83fd-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="a83fd-112">Az első parancs egy Azure Traffic Manager-végpontot hoz létre a **New-AzTrafficManagerEndpoint** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="a83fd-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="a83fd-113">A parancs a helyi végpontot a $TrafficManagerEndpoint tárolja.</span><span class="sxs-lookup"><span data-stu-id="a83fd-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="a83fd-114">A második parancs egyéni fejlécadatokat ad hozzá a $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a83fd-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="a83fd-115">Az utolsó parancs frissíti a Traffic Managerben a végpontot úgy, hogy megfeleljen a helyi $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a83fd-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="a83fd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a83fd-116">PARAMETERS</span></span>

### <span data-ttu-id="a83fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a83fd-117">-DefaultProfile</span></span>
<span data-ttu-id="a83fd-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a83fd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a83fd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a83fd-119">-Name</span></span>
<span data-ttu-id="a83fd-120">A hozzáadni szükséges egyéni fejléc-információ nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a83fd-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="a83fd-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a83fd-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="a83fd-122">Helyi **TrafficManagerEndpoint-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="a83fd-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="a83fd-123">Ez a parancsmag módosítja ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="a83fd-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="a83fd-124">A **TrafficManagerEndpoint** objektum beszerzéséhez használja a Get-AzTrafficManagerEndpoint vagy New-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a83fd-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="a83fd-125">-Érték</span><span class="sxs-lookup"><span data-stu-id="a83fd-125">-Value</span></span>
<span data-ttu-id="a83fd-126">A hozzáadható egyéni fejléc-információ értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a83fd-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="a83fd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a83fd-127">-Confirm</span></span>
<span data-ttu-id="a83fd-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a83fd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a83fd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a83fd-129">-WhatIf</span></span>
<span data-ttu-id="a83fd-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a83fd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a83fd-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a83fd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a83fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a83fd-132">CommonParameters</span></span>
<span data-ttu-id="a83fd-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a83fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a83fd-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a83fd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a83fd-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a83fd-135">INPUTS</span></span>

### <span data-ttu-id="a83fd-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a83fd-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a83fd-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a83fd-137">OUTPUTS</span></span>

### <span data-ttu-id="a83fd-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a83fd-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a83fd-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a83fd-139">NOTES</span></span>

## <span data-ttu-id="a83fd-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a83fd-140">RELATED LINKS</span></span>

[<span data-ttu-id="a83fd-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="a83fd-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="a83fd-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a83fd-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a83fd-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a83fd-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a83fd-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a83fd-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)

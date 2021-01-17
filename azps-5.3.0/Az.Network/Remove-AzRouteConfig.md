---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: 57ef72599cdb0500a9903aeb09f67437fe5cc2f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481197"
---
# <span data-ttu-id="e87c1-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e87c1-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="e87c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e87c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e87c1-103">Eltávolít egy útvonalat egy útvonaltáblából.</span><span class="sxs-lookup"><span data-stu-id="e87c1-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="e87c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e87c1-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e87c1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e87c1-105">DESCRIPTION</span></span>
<span data-ttu-id="e87c1-106">A **Remove-AzRouteConfig** parancsmag eltávolít egy útvonalat egy Azure útválasztási táblából.</span><span class="sxs-lookup"><span data-stu-id="e87c1-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="e87c1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e87c1-107">EXAMPLES</span></span>

### <span data-ttu-id="e87c1-108">1. példa: Útvonal eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e87c1-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzRouteConfig -Name "Route02" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="e87c1-109">Ez a parancs a RouteTable01 nevű útvonaltáblát a **Get-AzRouteTable** parancsmaggal kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e87c1-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="e87c1-110">A parancs a folyamat műveleti operátorával átadja a táblát az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="e87c1-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e87c1-111">Az aktuális parancsmag eltávolítja az Route02 nevű útvonalat, és az eredményt átadja a **Set-AzRouteTable** parancsmagnak, amely frissíti a táblát a módosításoknak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="e87c1-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="e87c1-112">A tábla már nem tartalmazza az Útvonal02 nevű útvonalat.</span><span class="sxs-lookup"><span data-stu-id="e87c1-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="e87c1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e87c1-113">PARAMETERS</span></span>

### <span data-ttu-id="e87c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e87c1-114">-DefaultProfile</span></span>
<span data-ttu-id="e87c1-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e87c1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e87c1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e87c1-116">-Name</span></span>
<span data-ttu-id="e87c1-117">A parancsmag által eltávolított útvonal neve.</span><span class="sxs-lookup"><span data-stu-id="e87c1-117">Specifies the name of the route that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e87c1-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e87c1-118">-RouteTable</span></span>
<span data-ttu-id="e87c1-119">Azt az útvonaltáblát adja meg, amely a parancsmag által törölt útvonalat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e87c1-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e87c1-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e87c1-120">-Confirm</span></span>
<span data-ttu-id="e87c1-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e87c1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e87c1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e87c1-122">-WhatIf</span></span>
<span data-ttu-id="e87c1-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e87c1-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e87c1-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e87c1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e87c1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e87c1-125">CommonParameters</span></span>
<span data-ttu-id="e87c1-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e87c1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e87c1-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e87c1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e87c1-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e87c1-128">INPUTS</span></span>

### <span data-ttu-id="e87c1-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e87c1-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="e87c1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e87c1-130">OUTPUTS</span></span>

### <span data-ttu-id="e87c1-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e87c1-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="e87c1-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e87c1-132">NOTES</span></span>

## <span data-ttu-id="e87c1-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e87c1-133">RELATED LINKS</span></span>

[<span data-ttu-id="e87c1-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e87c1-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="e87c1-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e87c1-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="e87c1-136">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e87c1-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="e87c1-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e87c1-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)



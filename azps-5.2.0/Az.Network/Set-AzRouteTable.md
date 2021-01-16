---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: bd419d3b6ec55af885a0f05b7be5c5de269fccdd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357502"
---
# <span data-ttu-id="da47c-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="da47c-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="da47c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da47c-102">SYNOPSIS</span></span>
<span data-ttu-id="da47c-103">Frissíti az útvonaltáblát.</span><span class="sxs-lookup"><span data-stu-id="da47c-103">Updates a route table.</span></span>

## <span data-ttu-id="da47c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da47c-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da47c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da47c-105">DESCRIPTION</span></span>
<span data-ttu-id="da47c-106">A **Set-AzRouteTable** parancsmag frissíti az útvonaltáblát.</span><span class="sxs-lookup"><span data-stu-id="da47c-106">The **Set-AzRouteTable** cmdlet updates a route table.</span></span>

## <span data-ttu-id="da47c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da47c-107">EXAMPLES</span></span>

### <span data-ttu-id="da47c-108">1. példa: Útvonaltábla frissítése útvonal-konfiguráció hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="da47c-108">Example 1: Update a route table by adding route configuration to it</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="da47c-109">Ez a parancs a RouteTable01 nevű útválasztási táblát egy parancsmag használatával Get-AzRouteTable le.</span><span class="sxs-lookup"><span data-stu-id="da47c-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="da47c-110">A parancs a folyamat műveleti Add-AzRouteConfig keresztül átadja a táblát a Add-AzRouteConfig parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="da47c-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="da47c-111">**Az Add-AzRouteConfig** hozzáadja az Route07 nevű útvonalat, majd átadja az eredményt az aktuális parancsmagnak, amely frissíti a táblát a módosításoknak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="da47c-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

### <span data-ttu-id="da47c-112">2. példa: Útvonaltábla módosítása</span><span class="sxs-lookup"><span data-stu-id="da47c-112">Example 2: Modify route table</span></span>

```
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
False
PS C:\> $rt.DisableBgpRoutePropagation = $true
PS C:\> Set-AzRouteTable -RouteTable $rt
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
True
```

<span data-ttu-id="da47c-113">Az első parancs lekérte az rtName nevű útvonaltáblát, és a $rt tárolja.</span><span class="sxs-lookup"><span data-stu-id="da47c-113">The first command gets the route table named rtName and stores it in the $rt variable.</span></span>
<span data-ttu-id="da47c-114">A második parancs a DisableBgpRoutePropagation értékét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="da47c-114">The second command displays the value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="da47c-115">A harmadik parancs frissíti a DisableBgpRoutePropagation értékét.</span><span class="sxs-lookup"><span data-stu-id="da47c-115">The third command updates value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="da47c-116">A negyedik parancs frissíti az útvonaltáblát a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="da47c-116">The fourth command updates route table on the server.</span></span>
<span data-ttu-id="da47c-117">Az ötödik parancs frissül az útvonaltáblában, és a $rt tárolja.</span><span class="sxs-lookup"><span data-stu-id="da47c-117">The fifth command gets updated route table and stores it in the $rt variable.</span></span>
<span data-ttu-id="da47c-118">A hatodik parancs a DisableBgpRoutePropagation értékét jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="da47c-118">The sixth command displays the value of DisableBgpRoutePropagation.</span></span>

## <span data-ttu-id="da47c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da47c-119">PARAMETERS</span></span>

### <span data-ttu-id="da47c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da47c-120">-AsJob</span></span>
<span data-ttu-id="da47c-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="da47c-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da47c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da47c-122">-DefaultProfile</span></span>
<span data-ttu-id="da47c-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da47c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da47c-124">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="da47c-124">-RouteTable</span></span>
<span data-ttu-id="da47c-125">Egy útvonaltábla-objektumot ad meg, amely azt az állapotot képviseli, amelyre az útvonaltáblát be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="da47c-125">Specifies a route table object representing the state to which the route table should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da47c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da47c-126">-Confirm</span></span>
<span data-ttu-id="da47c-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="da47c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da47c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da47c-128">-WhatIf</span></span>
<span data-ttu-id="da47c-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="da47c-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da47c-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da47c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da47c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da47c-131">CommonParameters</span></span>
<span data-ttu-id="da47c-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da47c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da47c-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da47c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da47c-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da47c-134">INPUTS</span></span>

### <span data-ttu-id="da47c-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="da47c-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="da47c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da47c-136">OUTPUTS</span></span>

### <span data-ttu-id="da47c-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="da47c-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="da47c-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da47c-138">NOTES</span></span>

## <span data-ttu-id="da47c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da47c-139">RELATED LINKS</span></span>

[<span data-ttu-id="da47c-140">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="da47c-140">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="da47c-141">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="da47c-141">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="da47c-142">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="da47c-142">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="da47c-143">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="da47c-143">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)



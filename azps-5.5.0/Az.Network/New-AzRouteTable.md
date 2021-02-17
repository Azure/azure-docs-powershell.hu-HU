---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: e7e0b58dfd4ac925110c5f666bc7c360cc222983
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146851"
---
# <span data-ttu-id="a955c-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a955c-101">New-AzRouteTable</span></span>

## <span data-ttu-id="a955c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a955c-102">SYNOPSIS</span></span>
<span data-ttu-id="a955c-103">Útvonaltáblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a955c-103">Creates a route table.</span></span>

## <span data-ttu-id="a955c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a955c-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a955c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a955c-105">DESCRIPTION</span></span>
<span data-ttu-id="a955c-106">A **New-AzRouteTable** parancsmag létrehoz egy Azure útválasztási táblát.</span><span class="sxs-lookup"><span data-stu-id="a955c-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="a955c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a955c-107">EXAMPLES</span></span>

### <span data-ttu-id="a955c-108">1. példa: Útvonalokat tartalmazó útvonaltábla létrehozása</span><span class="sxs-lookup"><span data-stu-id="a955c-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              :
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null,
                        "ProvisioningState": "Succeeded"
                      }
                    ]
Subnets           : []
```

<span data-ttu-id="a955c-109">Az első parancs létrehoz egy Route07 nevű útvonalat a New-AzRouteConfig parancsmag használatával, majd tárolja azt a $Route változóban.</span><span class="sxs-lookup"><span data-stu-id="a955c-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="a955c-110">Ez az útvonal csomagokat továbbít a helyi virtuális hálózatra.</span><span class="sxs-lookup"><span data-stu-id="a955c-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="a955c-111">A második parancs létrehoz egy RouteTable01 nevű útválasztási táblát, és hozzáadja a $Route az új táblához.</span><span class="sxs-lookup"><span data-stu-id="a955c-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="a955c-112">A parancs megadja azt az erőforráscsoportot, amelyhez a tábla tartozik, valamint a tábla helyét.</span><span class="sxs-lookup"><span data-stu-id="a955c-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="a955c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a955c-113">PARAMETERS</span></span>

### <span data-ttu-id="a955c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a955c-114">-AsJob</span></span>
<span data-ttu-id="a955c-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a955c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a955c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a955c-116">-DefaultProfile</span></span>
<span data-ttu-id="a955c-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a955c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a955c-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="a955c-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="a955c-119">Tiltsa le a BGP-útvonal automatikus propagálását.</span><span class="sxs-lookup"><span data-stu-id="a955c-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="a955c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a955c-120">-Force</span></span>
<span data-ttu-id="a955c-121">Azt jelzi, hogy ez a parancsmag akkor is létrehoz egy útvonaltáblát, ha már létezik egy azonos nevű útválasztási tábla.</span><span class="sxs-lookup"><span data-stu-id="a955c-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="a955c-122">-Location</span><span class="sxs-lookup"><span data-stu-id="a955c-122">-Location</span></span>
<span data-ttu-id="a955c-123">Azt az Azure-régiót adja meg, amelyben ez a parancsmag útvonaltáblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a955c-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="a955c-124">További információért lásd: [Azure Régiók.](http://azure.microsoft.com/en-us/regions/)</span><span class="sxs-lookup"><span data-stu-id="a955c-124">For more information, see [Azure Regions](http://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a955c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a955c-125">-Name</span></span>
<span data-ttu-id="a955c-126">Az útvonaltábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a955c-126">Specifies a name for the route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a955c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a955c-127">-ResourceGroupName</span></span>
<span data-ttu-id="a955c-128">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag útvonaltáblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a955c-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a955c-129">-Útvonal</span><span class="sxs-lookup"><span data-stu-id="a955c-129">-Route</span></span>
<span data-ttu-id="a955c-130">Az útvonaltáblához társítandó **Útvonalobjektumok** tömbje.</span><span class="sxs-lookup"><span data-stu-id="a955c-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRoute[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a955c-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="a955c-131">-Tag</span></span>
<span data-ttu-id="a955c-132">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="a955c-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a955c-133">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="a955c-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a955c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a955c-134">-Confirm</span></span>
<span data-ttu-id="a955c-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a955c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a955c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a955c-136">-WhatIf</span></span>
<span data-ttu-id="a955c-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a955c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a955c-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a955c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a955c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a955c-139">CommonParameters</span></span>
<span data-ttu-id="a955c-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a955c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a955c-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a955c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a955c-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a955c-142">INPUTS</span></span>

### <span data-ttu-id="a955c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="a955c-143">System.String</span></span>

### <span data-ttu-id="a955c-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a955c-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a955c-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span><span class="sxs-lookup"><span data-stu-id="a955c-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="a955c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a955c-146">OUTPUTS</span></span>

### <span data-ttu-id="a955c-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="a955c-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="a955c-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a955c-148">NOTES</span></span>

## <span data-ttu-id="a955c-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a955c-149">RELATED LINKS</span></span>

[<span data-ttu-id="a955c-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a955c-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="a955c-151">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a955c-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="a955c-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a955c-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="a955c-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="a955c-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 6561037b9174fd732d616f425324c164529e6367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926522"
---
# <span data-ttu-id="01d92-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="01d92-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="01d92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01d92-102">SYNOPSIS</span></span>
<span data-ttu-id="01d92-103">Azure ExpressRoute-keresztkapcsolatot kap az Azure-tól.</span><span class="sxs-lookup"><span data-stu-id="01d92-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="01d92-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01d92-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01d92-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01d92-105">DESCRIPTION</span></span>
<span data-ttu-id="01d92-106">A **Get-AzExpressRouteCrossConnection** parancsmaggal lekérhető egy ExpressRoute-rel létesített kapcsolati objektum az előfizetéséből.</span><span class="sxs-lookup"><span data-stu-id="01d92-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="01d92-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="01d92-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="01d92-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01d92-108">EXAMPLES</span></span>

### <span data-ttu-id="01d92-109">1. példa: Az ExpressRoute-kapcsolat lekésse</span><span class="sxs-lookup"><span data-stu-id="01d92-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="01d92-110">2. példa: Az ExpressRoute-keresztkapcsolatok felsorolása szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="01d92-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="01d92-111">Ez a parancsmag felsorolja a "teszt" kifejezéssel kezdődik összes ExpressRoute-keresztkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="01d92-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="01d92-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01d92-112">PARAMETERS</span></span>

### <span data-ttu-id="01d92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d92-113">-DefaultProfile</span></span>
<span data-ttu-id="01d92-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01d92-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01d92-115">-Name</span><span class="sxs-lookup"><span data-stu-id="01d92-115">-Name</span></span>
<span data-ttu-id="01d92-116">Az ExpressRoute-keresztkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="01d92-116">The name of the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="01d92-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d92-117">-ResourceGroupName</span></span>
<span data-ttu-id="01d92-118">Az ExpressRoute keresztkapcsolatot tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="01d92-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="01d92-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d92-119">CommonParameters</span></span>
<span data-ttu-id="01d92-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d92-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d92-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01d92-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d92-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01d92-122">INPUTS</span></span>

### <span data-ttu-id="01d92-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="01d92-123">None</span></span>
<span data-ttu-id="01d92-124">Ez a parancsmag semmilyen bemenetet nem fogad el.</span><span class="sxs-lookup"><span data-stu-id="01d92-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01d92-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01d92-125">OUTPUTS</span></span>

### <span data-ttu-id="01d92-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="01d92-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="01d92-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01d92-127">NOTES</span></span>

## <span data-ttu-id="01d92-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01d92-128">RELATED LINKS</span></span>

[<span data-ttu-id="01d92-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="01d92-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
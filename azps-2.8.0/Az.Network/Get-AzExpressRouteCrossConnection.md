---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: c15a8b57338a6c5e7c2f054e07a0d26d716627fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837602"
---
# <span data-ttu-id="26664-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="26664-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="26664-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26664-102">SYNOPSIS</span></span>
<span data-ttu-id="26664-103">Azure ExpressRoute Cross kapcsolatot kap az Azure-tól.</span><span class="sxs-lookup"><span data-stu-id="26664-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="26664-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26664-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26664-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="26664-105">DESCRIPTION</span></span>
<span data-ttu-id="26664-106">A **Get-AzExpressRouteCrossConnection** parancsmag a ExpressRoute-kapcsolat objektumnak az előfizetésből való visszakeresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="26664-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="26664-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="26664-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="26664-108">Példák</span><span class="sxs-lookup"><span data-stu-id="26664-108">EXAMPLES</span></span>

### <span data-ttu-id="26664-109">Példa 1: a ExpressRoute Cross kapcsolat beszerzése</span><span class="sxs-lookup"><span data-stu-id="26664-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="26664-110">2. példa: a ExpressRoute közötti kapcsolatok listája szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="26664-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="26664-111">Ez a parancsmag felsorolja az összes olyan ExpressRoute, amely a "teszt" kezdetű kapcsolatokra mutat</span><span class="sxs-lookup"><span data-stu-id="26664-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="26664-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26664-112">PARAMETERS</span></span>

### <span data-ttu-id="26664-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26664-113">-DefaultProfile</span></span>
<span data-ttu-id="26664-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26664-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26664-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="26664-115">-Name</span></span>
<span data-ttu-id="26664-116">A ExpressRoute-kapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="26664-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="26664-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26664-117">-ResourceGroupName</span></span>
<span data-ttu-id="26664-118">Annak az erőforráscsoportnek a neve, amely a ExpressRoute-kereszt kapcsolatot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="26664-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="26664-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26664-119">CommonParameters</span></span>
<span data-ttu-id="26664-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26664-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26664-121">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="26664-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26664-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26664-122">INPUTS</span></span>

### <span data-ttu-id="26664-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="26664-123">None</span></span>
<span data-ttu-id="26664-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="26664-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26664-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26664-125">OUTPUTS</span></span>

### <span data-ttu-id="26664-126">Microsoft. Azure. commands. Network. models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="26664-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="26664-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26664-127">NOTES</span></span>

## <span data-ttu-id="26664-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26664-128">RELATED LINKS</span></span>

[<span data-ttu-id="26664-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="26664-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466221"
---
# <span data-ttu-id="3e4df-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3e4df-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="3e4df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e4df-102">SYNOPSIS</span></span>
<span data-ttu-id="3e4df-103">Azure ExpressRoute-keresztkapcsolatot kap az Azure-tól.</span><span class="sxs-lookup"><span data-stu-id="3e4df-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="3e4df-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e4df-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e4df-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e4df-105">DESCRIPTION</span></span>
<span data-ttu-id="3e4df-106">A **Get-AzExpressRouteCrossConnection** parancsmaggal lekérhető egy ExpressRoute-rel létesített kapcsolati objektum az előfizetéséből.</span><span class="sxs-lookup"><span data-stu-id="3e4df-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="3e4df-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3e4df-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="3e4df-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e4df-108">EXAMPLES</span></span>

### <span data-ttu-id="3e4df-109">1. példa: Az ExpressRoute-kapcsolat lekésse</span><span class="sxs-lookup"><span data-stu-id="3e4df-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="3e4df-110">2. példa: Az ExpressRoute-keresztkapcsolatok felsorolása szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="3e4df-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="3e4df-111">Ez a parancsmag felsorolja a "teszt" kifejezéssel kezdődik összes ExpressRoute-keresztkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="3e4df-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="3e4df-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e4df-112">PARAMETERS</span></span>

### <span data-ttu-id="3e4df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e4df-113">-DefaultProfile</span></span>
<span data-ttu-id="3e4df-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e4df-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e4df-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3e4df-115">-Name</span></span>
<span data-ttu-id="3e4df-116">Az ExpressRoute-keresztkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="3e4df-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="3e4df-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e4df-117">-ResourceGroupName</span></span>
<span data-ttu-id="3e4df-118">Az ExpressRoute keresztkapcsolatot tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3e4df-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="3e4df-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e4df-119">CommonParameters</span></span>
<span data-ttu-id="3e4df-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e4df-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e4df-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e4df-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e4df-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e4df-122">INPUTS</span></span>

### <span data-ttu-id="3e4df-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="3e4df-123">None</span></span>
<span data-ttu-id="3e4df-124">Ez a parancsmag semmilyen bemenetet nem fogad el.</span><span class="sxs-lookup"><span data-stu-id="3e4df-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e4df-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e4df-125">OUTPUTS</span></span>

### <span data-ttu-id="3e4df-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3e4df-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="3e4df-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e4df-127">NOTES</span></span>

## <span data-ttu-id="3e4df-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e4df-128">RELATED LINKS</span></span>

[<span data-ttu-id="3e4df-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3e4df-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 246675a2473bb20e5040f3898b6931f1b3ee6933
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154387"
---
# <span data-ttu-id="19647-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="19647-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="19647-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19647-102">SYNOPSIS</span></span>
<span data-ttu-id="19647-103">Identitás hozzárendelése ExpressRoutePorthoz.</span><span class="sxs-lookup"><span data-stu-id="19647-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="19647-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19647-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19647-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19647-105">DESCRIPTION</span></span>
<span data-ttu-id="19647-106">A **Get-AzExpressRoutePortIdentity** parancsmag egy helyi Azure ExpressRoutePort-objektumhoz rendeli az identitást.</span><span class="sxs-lookup"><span data-stu-id="19647-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="19647-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19647-107">EXAMPLES</span></span>

### <span data-ttu-id="19647-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="19647-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="19647-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19647-109">PARAMETERS</span></span>

### <span data-ttu-id="19647-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19647-110">-DefaultProfile</span></span>
<span data-ttu-id="19647-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19647-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19647-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="19647-112">-ExpressRoutePort</span></span>
<span data-ttu-id="19647-113">Az ExpressRoute-port</span><span class="sxs-lookup"><span data-stu-id="19647-113">The ExpressRoute Port</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19647-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19647-114">CommonParameters</span></span>
<span data-ttu-id="19647-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19647-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19647-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19647-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19647-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19647-117">INPUTS</span></span>

### <span data-ttu-id="19647-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="19647-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="19647-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19647-119">OUTPUTS</span></span>

### <span data-ttu-id="19647-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="19647-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="19647-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19647-121">NOTES</span></span>

## <span data-ttu-id="19647-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19647-122">RELATED LINKS</span></span>
[<span data-ttu-id="19647-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="19647-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="19647-124">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="19647-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="19647-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="19647-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
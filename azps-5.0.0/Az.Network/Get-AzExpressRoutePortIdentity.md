---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 246675a2473bb20e5040f3898b6931f1b3ee6933
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195670"
---
# <span data-ttu-id="10ca3-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="10ca3-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="10ca3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="10ca3-103">ExpressRoutePort-identitás hozzárendelése</span><span class="sxs-lookup"><span data-stu-id="10ca3-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="10ca3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10ca3-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10ca3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="10ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="10ca3-106">A **Get-AzExpressRoutePortIdentity** parancsmag egy helyi Azure ExpressRoutePort-objektumhoz rendelt identitást kap.</span><span class="sxs-lookup"><span data-stu-id="10ca3-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="10ca3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="10ca3-107">EXAMPLES</span></span>

### <span data-ttu-id="10ca3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="10ca3-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="10ca3-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10ca3-109">PARAMETERS</span></span>

### <span data-ttu-id="10ca3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ca3-110">-DefaultProfile</span></span>
<span data-ttu-id="10ca3-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10ca3-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10ca3-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="10ca3-112">-ExpressRoutePort</span></span>
<span data-ttu-id="10ca3-113">A ExpressRoute-port</span><span class="sxs-lookup"><span data-stu-id="10ca3-113">The ExpressRoute Port</span></span>

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

### <span data-ttu-id="10ca3-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ca3-114">CommonParameters</span></span>
<span data-ttu-id="10ca3-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10ca3-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ca3-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="10ca3-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ca3-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10ca3-117">INPUTS</span></span>

### <span data-ttu-id="10ca3-118">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="10ca3-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="10ca3-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10ca3-119">OUTPUTS</span></span>

### <span data-ttu-id="10ca3-120">Microsoft. Azure. commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="10ca3-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="10ca3-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10ca3-121">NOTES</span></span>

## <span data-ttu-id="10ca3-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10ca3-122">RELATED LINKS</span></span>
[<span data-ttu-id="10ca3-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="10ca3-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="10ca3-124">Új – AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="10ca3-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="10ca3-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="10ca3-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
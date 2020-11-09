---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303160"
---
# <span data-ttu-id="8371b-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="8371b-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="8371b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8371b-102">SYNOPSIS</span></span>
<span data-ttu-id="8371b-103">Beolvassa a ExpressRoutePort-kapcsolat konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="8371b-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="8371b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8371b-104">SYNTAX</span></span>

### <span data-ttu-id="8371b-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8371b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8371b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8371b-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8371b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8371b-107">DESCRIPTION</span></span>
<span data-ttu-id="8371b-108">A **Get-AzExpressRoutePortLinkConfig** parancsmag kikeresi egy ExpressRoutePort hivatkozásának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="8371b-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="8371b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8371b-109">EXAMPLES</span></span>

### <span data-ttu-id="8371b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8371b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="8371b-111">A ExpressRoutePort $erport Link1-konfigurációjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="8371b-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="8371b-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="8371b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="8371b-113">A ExpressRoutePort-ban a ResourceId $id a hivatkozás konfigurációját kapja $erport</span><span class="sxs-lookup"><span data-stu-id="8371b-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="8371b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8371b-114">PARAMETERS</span></span>

### <span data-ttu-id="8371b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8371b-115">-DefaultProfile</span></span>
<span data-ttu-id="8371b-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8371b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8371b-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8371b-117">-ExpressRoutePort</span></span>
<span data-ttu-id="8371b-118">A ExpressRoutePort-erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="8371b-118">The reference of the ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8371b-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8371b-119">-Name</span></span>
<span data-ttu-id="8371b-120">A hivatkozás neve.</span><span class="sxs-lookup"><span data-stu-id="8371b-120">Name of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8371b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8371b-121">-ResourceId</span></span>
<span data-ttu-id="8371b-122">A hivatkozás ResourceId</span><span class="sxs-lookup"><span data-stu-id="8371b-122">ResourceId of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8371b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8371b-123">CommonParameters</span></span>
<span data-ttu-id="8371b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8371b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8371b-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8371b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8371b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8371b-126">INPUTS</span></span>

### <span data-ttu-id="8371b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8371b-127">System.String</span></span>

### <span data-ttu-id="8371b-128">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8371b-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="8371b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8371b-129">OUTPUTS</span></span>

### <span data-ttu-id="8371b-130">Microsoft. Azure. commands. Network. models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="8371b-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="8371b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8371b-131">NOTES</span></span>

## <span data-ttu-id="8371b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8371b-132">RELATED LINKS</span></span>

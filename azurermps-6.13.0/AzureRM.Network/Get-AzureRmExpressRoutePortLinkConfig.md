---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
ms.openlocfilehash: c758131685787ec8627f6e0cd3760e2ee42107c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504359"
---
# <span data-ttu-id="ca384-101">Get-AzureRmExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="ca384-101">Get-AzureRmExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="ca384-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca384-102">SYNOPSIS</span></span>
<span data-ttu-id="ca384-103">Beolvassa a ExpressRoutePort-kapcsolat konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="ca384-103">Gets an ExpressRoutePort link configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca384-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca384-104">SYNTAX</span></span>

### <span data-ttu-id="ca384-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ca384-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca384-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca384-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> -ResourceId <String> 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca384-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca384-107">DESCRIPTION</span></span>
<span data-ttu-id="ca384-108">A **Get-AzureRmExpressRoutePortLinkConfig** parancsmag kikeresi egy ExpressRoutePort hivatkozásának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="ca384-108">The **Get-AzureRmExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="ca384-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ca384-109">EXAMPLES</span></span>

### <span data-ttu-id="ca384-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ca384-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="ca384-111">A ExpressRoutePort $erport Link1-konfigurációjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="ca384-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="ca384-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="ca384-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="ca384-113">A ExpressRoutePort-ban a ResourceId $id a hivatkozás konfigurációját kapja $erport</span><span class="sxs-lookup"><span data-stu-id="ca384-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="ca384-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca384-114">PARAMETERS</span></span>

### <span data-ttu-id="ca384-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca384-115">-DefaultProfile</span></span>
<span data-ttu-id="ca384-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca384-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca384-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ca384-117">-ExpressRoutePort</span></span>
<span data-ttu-id="ca384-118">A ExpressRoutePort-erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="ca384-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="ca384-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca384-119">-Name</span></span>
<span data-ttu-id="ca384-120">A hivatkozás neve.</span><span class="sxs-lookup"><span data-stu-id="ca384-120">Name of the link.</span></span>

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

### <span data-ttu-id="ca384-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca384-121">-ResourceId</span></span>
<span data-ttu-id="ca384-122">A hivatkozás ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca384-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="ca384-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca384-123">CommonParameters</span></span>
<span data-ttu-id="ca384-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca384-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca384-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca384-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca384-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca384-126">INPUTS</span></span>

### <span data-ttu-id="ca384-127">Microsoft. Azure. commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ca384-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ca384-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca384-128">OUTPUTS</span></span>

### <span data-ttu-id="ca384-129">Microsoft. Azure. commands. Network. models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="ca384-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="ca384-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca384-130">NOTES</span></span>

## <span data-ttu-id="ca384-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca384-131">RELATED LINKS</span></span>

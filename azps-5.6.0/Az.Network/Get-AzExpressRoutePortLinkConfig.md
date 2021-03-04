---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: a8326afbeb6d71d54ec861eb3ec65868e7e230bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921113"
---
# <span data-ttu-id="014d6-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="014d6-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="014d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="014d6-102">SYNOPSIS</span></span>
<span data-ttu-id="014d6-103">ExpressRoutePort-csatolást konfigurál.</span><span class="sxs-lookup"><span data-stu-id="014d6-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="014d6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="014d6-104">SYNTAX</span></span>

### <span data-ttu-id="014d6-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="014d6-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="014d6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="014d6-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="014d6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="014d6-107">DESCRIPTION</span></span>
<span data-ttu-id="014d6-108">A **Get-AzExpressRoutePortLinkConfig** parancsmag beolvassa egy ExpressRoutePort csatolásának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="014d6-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="014d6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="014d6-109">EXAMPLES</span></span>

### <span data-ttu-id="014d6-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="014d6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="014d6-111">Az ExpressRoutePort-$erport</span><span class="sxs-lookup"><span data-stu-id="014d6-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="014d6-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="014d6-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="014d6-113">Az ExpressRoutePort-$id ResourceId $erport</span><span class="sxs-lookup"><span data-stu-id="014d6-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="014d6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="014d6-114">PARAMETERS</span></span>

### <span data-ttu-id="014d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="014d6-115">-DefaultProfile</span></span>
<span data-ttu-id="014d6-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="014d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="014d6-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="014d6-117">-ExpressRoutePort</span></span>
<span data-ttu-id="014d6-118">Az ExpressRoutePort-erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="014d6-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="014d6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="014d6-119">-Name</span></span>
<span data-ttu-id="014d6-120">A hivatkozás neve.</span><span class="sxs-lookup"><span data-stu-id="014d6-120">Name of the link.</span></span>

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

### <span data-ttu-id="014d6-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="014d6-121">-ResourceId</span></span>
<span data-ttu-id="014d6-122">A hivatkozás ResourceId-e.</span><span class="sxs-lookup"><span data-stu-id="014d6-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="014d6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="014d6-123">CommonParameters</span></span>
<span data-ttu-id="014d6-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="014d6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="014d6-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="014d6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="014d6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="014d6-126">INPUTS</span></span>

### <span data-ttu-id="014d6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="014d6-127">System.String</span></span>

### <span data-ttu-id="014d6-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="014d6-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="014d6-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="014d6-129">OUTPUTS</span></span>

### <span data-ttu-id="014d6-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="014d6-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="014d6-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="014d6-131">NOTES</span></span>

## <span data-ttu-id="014d6-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="014d6-132">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380168"
---
# <span data-ttu-id="be1f8-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="be1f8-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="be1f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be1f8-102">SYNOPSIS</span></span>
<span data-ttu-id="be1f8-103">ExpressRoutePort-csatolást konfigurál.</span><span class="sxs-lookup"><span data-stu-id="be1f8-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="be1f8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="be1f8-104">SYNTAX</span></span>

### <span data-ttu-id="be1f8-105">ResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="be1f8-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be1f8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be1f8-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be1f8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="be1f8-107">DESCRIPTION</span></span>
<span data-ttu-id="be1f8-108">A **Get-AzExpressRoutePortLinkConfig** parancsmag beolvassa egy ExpressRoutePort csatolásának konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="be1f8-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="be1f8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="be1f8-109">EXAMPLES</span></span>

### <span data-ttu-id="be1f8-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="be1f8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="be1f8-111">Az ExpressRoutePort-$erport</span><span class="sxs-lookup"><span data-stu-id="be1f8-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="be1f8-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="be1f8-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="be1f8-113">Az ExpressRoutePort-$id ResourceId $erport</span><span class="sxs-lookup"><span data-stu-id="be1f8-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="be1f8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be1f8-114">PARAMETERS</span></span>

### <span data-ttu-id="be1f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be1f8-115">-DefaultProfile</span></span>
<span data-ttu-id="be1f8-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be1f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be1f8-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="be1f8-117">-ExpressRoutePort</span></span>
<span data-ttu-id="be1f8-118">Az ExpressRoutePort-erőforrás hivatkozása.</span><span class="sxs-lookup"><span data-stu-id="be1f8-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="be1f8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="be1f8-119">-Name</span></span>
<span data-ttu-id="be1f8-120">A hivatkozás neve.</span><span class="sxs-lookup"><span data-stu-id="be1f8-120">Name of the link.</span></span>

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

### <span data-ttu-id="be1f8-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be1f8-121">-ResourceId</span></span>
<span data-ttu-id="be1f8-122">A hivatkozás ResourceId-e.</span><span class="sxs-lookup"><span data-stu-id="be1f8-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="be1f8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be1f8-123">CommonParameters</span></span>
<span data-ttu-id="be1f8-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be1f8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be1f8-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be1f8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be1f8-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be1f8-126">INPUTS</span></span>

### <span data-ttu-id="be1f8-127">System.String</span><span class="sxs-lookup"><span data-stu-id="be1f8-127">System.String</span></span>

### <span data-ttu-id="be1f8-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="be1f8-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="be1f8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be1f8-129">OUTPUTS</span></span>

### <span data-ttu-id="be1f8-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="be1f8-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="be1f8-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="be1f8-131">NOTES</span></span>

## <span data-ttu-id="be1f8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be1f8-132">RELATED LINKS</span></span>

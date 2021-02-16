---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: e99df2f29781281ee0293f4cf52715153ff0d0cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151843"
---
# <span data-ttu-id="8f4ba-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="8f4ba-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="8f4ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f4ba-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4ba-103">Azure VirtualRouter-kapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="8f4ba-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="8f4ba-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8f4ba-104">SYNTAX</span></span>

### <span data-ttu-id="8f4ba-105">VirtualRouterSubscriptionIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8f4ba-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f4ba-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f4ba-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f4ba-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f4ba-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f4ba-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8f4ba-108">DESCRIPTION</span></span>
<span data-ttu-id="8f4ba-109">A **Get-AzVirtualRouter** parancsmag azure virtualroutert kap</span><span class="sxs-lookup"><span data-stu-id="8f4ba-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="8f4ba-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8f4ba-110">EXAMPLES</span></span>

### <span data-ttu-id="8f4ba-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8f4ba-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="8f4ba-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="8f4ba-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="8f4ba-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f4ba-113">PARAMETERS</span></span>

### <span data-ttu-id="8f4ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4ba-114">-DefaultProfile</span></span>
<span data-ttu-id="8f4ba-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f4ba-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f4ba-116">-ResourceGroupName</span></span>
<span data-ttu-id="8f4ba-117">A virtuális útválasztó erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-117">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4ba-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f4ba-118">-ResourceId</span></span>
<span data-ttu-id="8f4ba-119">A virtuális útválasztó ResourceId-neve.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-119">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4ba-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="8f4ba-120">-RouterName</span></span>
<span data-ttu-id="8f4ba-121">A virtuális útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4ba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4ba-122">CommonParameters</span></span>
<span data-ttu-id="8f4ba-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4ba-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f4ba-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4ba-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f4ba-125">INPUTS</span></span>

### <span data-ttu-id="8f4ba-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8f4ba-126">System.String</span></span>

## <span data-ttu-id="8f4ba-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f4ba-127">OUTPUTS</span></span>

### <span data-ttu-id="8f4ba-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="8f4ba-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="8f4ba-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8f4ba-129">NOTES</span></span>

## <span data-ttu-id="8f4ba-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f4ba-130">RELATED LINKS</span></span>

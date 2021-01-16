---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: 26e919935a65a486252cac234450adf214992b36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361086"
---
# <span data-ttu-id="0fe23-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="0fe23-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="0fe23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fe23-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe23-103">Azure VirtualRouter-kapcsolat létrehozása</span><span class="sxs-lookup"><span data-stu-id="0fe23-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="0fe23-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0fe23-104">SYNTAX</span></span>

### <span data-ttu-id="0fe23-105">VirtualRouterSubscriptionIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0fe23-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fe23-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe23-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fe23-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fe23-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fe23-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0fe23-108">DESCRIPTION</span></span>
<span data-ttu-id="0fe23-109">A **Get-AzVirtualRouter** parancsmag azure virtualroutert kap</span><span class="sxs-lookup"><span data-stu-id="0fe23-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="0fe23-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0fe23-110">EXAMPLES</span></span>

### <span data-ttu-id="0fe23-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="0fe23-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="0fe23-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="0fe23-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="0fe23-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fe23-113">PARAMETERS</span></span>

### <span data-ttu-id="0fe23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe23-114">-DefaultProfile</span></span>
<span data-ttu-id="0fe23-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fe23-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe23-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe23-116">-ResourceGroupName</span></span>
<span data-ttu-id="0fe23-117">A virtuális útválasztó erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="0fe23-117">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="0fe23-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fe23-118">-ResourceId</span></span>
<span data-ttu-id="0fe23-119">A virtuális útválasztó ResourceId-neve.</span><span class="sxs-lookup"><span data-stu-id="0fe23-119">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="0fe23-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="0fe23-120">-RouterName</span></span>
<span data-ttu-id="0fe23-121">A virtuális útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="0fe23-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="0fe23-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe23-122">CommonParameters</span></span>
<span data-ttu-id="0fe23-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fe23-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe23-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fe23-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe23-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0fe23-125">INPUTS</span></span>

### <span data-ttu-id="0fe23-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0fe23-126">System.String</span></span>

## <span data-ttu-id="0fe23-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fe23-127">OUTPUTS</span></span>

### <span data-ttu-id="0fe23-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="0fe23-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="0fe23-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0fe23-129">NOTES</span></span>

## <span data-ttu-id="0fe23-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fe23-130">RELATED LINKS</span></span>

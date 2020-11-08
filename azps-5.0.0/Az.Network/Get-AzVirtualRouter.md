---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: 26e919935a65a486252cac234450adf214992b36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186904"
---
# <span data-ttu-id="91cf3-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="91cf3-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="91cf3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="91cf3-103">Azure-VirtualRouter beszerzése</span><span class="sxs-lookup"><span data-stu-id="91cf3-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="91cf3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91cf3-104">SYNTAX</span></span>

### <span data-ttu-id="91cf3-105">VirtualRouterSubscriptionIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91cf3-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91cf3-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="91cf3-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91cf3-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91cf3-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91cf3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="91cf3-108">DESCRIPTION</span></span>
<span data-ttu-id="91cf3-109">A **Get-AzVirtualRouter** parancsmag Azure VirtualRouter kap</span><span class="sxs-lookup"><span data-stu-id="91cf3-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="91cf3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="91cf3-110">EXAMPLES</span></span>

### <span data-ttu-id="91cf3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="91cf3-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="91cf3-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="91cf3-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="91cf3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91cf3-113">PARAMETERS</span></span>

### <span data-ttu-id="91cf3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91cf3-114">-DefaultProfile</span></span>
<span data-ttu-id="91cf3-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91cf3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91cf3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91cf3-116">-ResourceGroupName</span></span>
<span data-ttu-id="91cf3-117">A virtuális útválasztó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="91cf3-117">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="91cf3-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91cf3-118">-ResourceId</span></span>
<span data-ttu-id="91cf3-119">A virtuális útválasztó ResourceId</span><span class="sxs-lookup"><span data-stu-id="91cf3-119">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="91cf3-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="91cf3-120">-RouterName</span></span>
<span data-ttu-id="91cf3-121">A virtuális útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="91cf3-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="91cf3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91cf3-122">CommonParameters</span></span>
<span data-ttu-id="91cf3-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91cf3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91cf3-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="91cf3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91cf3-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91cf3-125">INPUTS</span></span>

### <span data-ttu-id="91cf3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="91cf3-126">System.String</span></span>

## <span data-ttu-id="91cf3-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91cf3-127">OUTPUTS</span></span>

### <span data-ttu-id="91cf3-128">Microsoft. Azure. commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="91cf3-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="91cf3-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91cf3-129">NOTES</span></span>

## <span data-ttu-id="91cf3-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91cf3-130">RELATED LINKS</span></span>

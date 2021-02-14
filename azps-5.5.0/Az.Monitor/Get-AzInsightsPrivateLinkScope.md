---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203483"
---
# <span data-ttu-id="718d2-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="718d2-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="718d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="718d2-102">SYNOPSIS</span></span>
<span data-ttu-id="718d2-103">Személyes hivatkozás hatókörének lekérte</span><span class="sxs-lookup"><span data-stu-id="718d2-103">Get private link scope</span></span>

## <span data-ttu-id="718d2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="718d2-104">SYNTAX</span></span>

### <span data-ttu-id="718d2-105">ByResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="718d2-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="718d2-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="718d2-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="718d2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="718d2-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="718d2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="718d2-108">DESCRIPTION</span></span>
<span data-ttu-id="718d2-109">Saját hivatkozás hatókörének listába sorolása vagy lekért hatóköre</span><span class="sxs-lookup"><span data-stu-id="718d2-109">List or get private link scope</span></span> 

## <span data-ttu-id="718d2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="718d2-110">EXAMPLES</span></span>

### <span data-ttu-id="718d2-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="718d2-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="718d2-112">Privát hivatkozás hatókörének felsorolása az "rg_name" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="718d2-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="718d2-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="718d2-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="718d2-114">Privát hivatkozás hatókörének lekérte a "scope_name" nevet az "rg_name" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="718d2-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="718d2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="718d2-115">PARAMETERS</span></span>

### <span data-ttu-id="718d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="718d2-116">-DefaultProfile</span></span>
<span data-ttu-id="718d2-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="718d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="718d2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="718d2-118">-Name</span></span>
<span data-ttu-id="718d2-119">Private Link Scope Name</span><span class="sxs-lookup"><span data-stu-id="718d2-119">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="718d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="718d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="718d2-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="718d2-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="718d2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="718d2-122">-ResourceId</span></span>
<span data-ttu-id="718d2-123">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="718d2-123">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="718d2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="718d2-124">CommonParameters</span></span>
<span data-ttu-id="718d2-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="718d2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="718d2-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="718d2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="718d2-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="718d2-127">INPUTS</span></span>

### <span data-ttu-id="718d2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="718d2-128">System.String</span></span>

## <span data-ttu-id="718d2-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="718d2-129">OUTPUTS</span></span>

### <span data-ttu-id="718d2-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="718d2-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="718d2-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="718d2-131">NOTES</span></span>

## <span data-ttu-id="718d2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="718d2-132">RELATED LINKS</span></span>

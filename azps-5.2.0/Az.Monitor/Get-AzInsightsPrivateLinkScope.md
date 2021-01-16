---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367637"
---
# <span data-ttu-id="addff-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="addff-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="addff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="addff-102">SYNOPSIS</span></span>
<span data-ttu-id="addff-103">Személyes hivatkozás hatókörének lekérte</span><span class="sxs-lookup"><span data-stu-id="addff-103">Get private link scope</span></span>

## <span data-ttu-id="addff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="addff-104">SYNTAX</span></span>

### <span data-ttu-id="addff-105">ByResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="addff-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="addff-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="addff-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="addff-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="addff-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="addff-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="addff-108">DESCRIPTION</span></span>
<span data-ttu-id="addff-109">Saját hivatkozás hatókörének listába sorolása vagy lekért hatóköre</span><span class="sxs-lookup"><span data-stu-id="addff-109">List or get private link scope</span></span> 

## <span data-ttu-id="addff-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="addff-110">EXAMPLES</span></span>

### <span data-ttu-id="addff-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="addff-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="addff-112">Privát hivatkozás hatókörének felsorolása az "rg_name" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="addff-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="addff-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="addff-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="addff-114">Privát hivatkozás hatókörének lekérte "scope_name" névvel az "rg_name" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="addff-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="addff-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="addff-115">PARAMETERS</span></span>

### <span data-ttu-id="addff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="addff-116">-DefaultProfile</span></span>
<span data-ttu-id="addff-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="addff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="addff-118">-Name</span><span class="sxs-lookup"><span data-stu-id="addff-118">-Name</span></span>
<span data-ttu-id="addff-119">Private Link Scope Name</span><span class="sxs-lookup"><span data-stu-id="addff-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="addff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="addff-120">-ResourceGroupName</span></span>
<span data-ttu-id="addff-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="addff-121">Resource Group Name</span></span>

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

### <span data-ttu-id="addff-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="addff-122">-ResourceId</span></span>
<span data-ttu-id="addff-123">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="addff-123">Resource Id</span></span>

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

### <span data-ttu-id="addff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="addff-124">CommonParameters</span></span>
<span data-ttu-id="addff-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="addff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="addff-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="addff-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="addff-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="addff-127">INPUTS</span></span>

### <span data-ttu-id="addff-128">System.String</span><span class="sxs-lookup"><span data-stu-id="addff-128">System.String</span></span>

## <span data-ttu-id="addff-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="addff-129">OUTPUTS</span></span>

### <span data-ttu-id="addff-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="addff-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="addff-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="addff-131">NOTES</span></span>

## <span data-ttu-id="addff-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="addff-132">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 941b60da0282bdad523b06657639a730d1776ce3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932641"
---
# <span data-ttu-id="25460-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="25460-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="25460-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25460-102">SYNOPSIS</span></span>
<span data-ttu-id="25460-103">Személyes hivatkozás hatókörének lekérte</span><span class="sxs-lookup"><span data-stu-id="25460-103">Get private link scope</span></span>

## <span data-ttu-id="25460-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="25460-104">SYNTAX</span></span>

### <span data-ttu-id="25460-105">ByResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25460-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25460-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="25460-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25460-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25460-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25460-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="25460-108">DESCRIPTION</span></span>
<span data-ttu-id="25460-109">Saját hivatkozás hatókörének listába sorolása vagy lekért hatóköre</span><span class="sxs-lookup"><span data-stu-id="25460-109">List or get private link scope</span></span> 

## <span data-ttu-id="25460-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="25460-110">EXAMPLES</span></span>

### <span data-ttu-id="25460-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="25460-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="25460-112">Privát hivatkozás hatókörének felsorolása az "rg_name" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="25460-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="25460-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="25460-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="25460-114">Privát hivatkozás hatókörének lekérte "scope_name" névvel az "rg_name" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="25460-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="25460-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25460-115">PARAMETERS</span></span>

### <span data-ttu-id="25460-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25460-116">-DefaultProfile</span></span>
<span data-ttu-id="25460-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25460-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25460-118">-Name</span><span class="sxs-lookup"><span data-stu-id="25460-118">-Name</span></span>
<span data-ttu-id="25460-119">Private Link Scope Name</span><span class="sxs-lookup"><span data-stu-id="25460-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="25460-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25460-120">-ResourceGroupName</span></span>
<span data-ttu-id="25460-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="25460-121">Resource Group Name</span></span>

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

### <span data-ttu-id="25460-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25460-122">-ResourceId</span></span>
<span data-ttu-id="25460-123">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="25460-123">Resource Id</span></span>

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

### <span data-ttu-id="25460-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25460-124">CommonParameters</span></span>
<span data-ttu-id="25460-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25460-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25460-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25460-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25460-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25460-127">INPUTS</span></span>

### <span data-ttu-id="25460-128">System.String</span><span class="sxs-lookup"><span data-stu-id="25460-128">System.String</span></span>

## <span data-ttu-id="25460-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25460-129">OUTPUTS</span></span>

### <span data-ttu-id="25460-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="25460-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="25460-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="25460-131">NOTES</span></span>

## <span data-ttu-id="25460-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25460-132">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480054"
---
# <span data-ttu-id="83a96-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="83a96-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="83a96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83a96-102">SYNOPSIS</span></span>
<span data-ttu-id="83a96-103">create private link scope</span><span class="sxs-lookup"><span data-stu-id="83a96-103">create private link scope</span></span>

## <span data-ttu-id="83a96-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="83a96-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83a96-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="83a96-105">DESCRIPTION</span></span>
<span data-ttu-id="83a96-106">create private link scope</span><span class="sxs-lookup"><span data-stu-id="83a96-106">create private link scope</span></span>

## <span data-ttu-id="83a96-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="83a96-107">EXAMPLES</span></span>

### <span data-ttu-id="83a96-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="83a96-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="83a96-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span><span class="sxs-lookup"><span data-stu-id="83a96-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="83a96-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83a96-110">PARAMETERS</span></span>

### <span data-ttu-id="83a96-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83a96-111">-DefaultProfile</span></span>
<span data-ttu-id="83a96-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83a96-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83a96-113">-Location</span><span class="sxs-lookup"><span data-stu-id="83a96-113">-Location</span></span>
<span data-ttu-id="83a96-114">Hely</span><span class="sxs-lookup"><span data-stu-id="83a96-114">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83a96-115">-Name</span><span class="sxs-lookup"><span data-stu-id="83a96-115">-Name</span></span>
<span data-ttu-id="83a96-116">Private Link Scope Name</span><span class="sxs-lookup"><span data-stu-id="83a96-116">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83a96-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83a96-117">-ResourceGroupName</span></span>
<span data-ttu-id="83a96-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="83a96-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83a96-119">-Címkék</span><span class="sxs-lookup"><span data-stu-id="83a96-119">-Tags</span></span>
<span data-ttu-id="83a96-120">Címkék</span><span class="sxs-lookup"><span data-stu-id="83a96-120">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83a96-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83a96-121">-Confirm</span></span>
<span data-ttu-id="83a96-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="83a96-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83a96-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83a96-123">-WhatIf</span></span>
<span data-ttu-id="83a96-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="83a96-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83a96-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83a96-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83a96-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83a96-126">CommonParameters</span></span>
<span data-ttu-id="83a96-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83a96-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83a96-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83a96-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83a96-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83a96-129">INPUTS</span></span>

### <span data-ttu-id="83a96-130">System.String</span><span class="sxs-lookup"><span data-stu-id="83a96-130">System.String</span></span>

## <span data-ttu-id="83a96-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83a96-131">OUTPUTS</span></span>

### <span data-ttu-id="83a96-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="83a96-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="83a96-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="83a96-133">NOTES</span></span>

## <span data-ttu-id="83a96-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83a96-134">RELATED LINKS</span></span>

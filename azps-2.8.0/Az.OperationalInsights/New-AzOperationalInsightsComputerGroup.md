---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
ms.openlocfilehash: d1a1633303e30fc10c5eee7432101fa075f4d38f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838461"
---
# <span data-ttu-id="e5e43-101">New-AzOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="e5e43-101">New-AzOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="e5e43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5e43-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e43-103">Számítógép-csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e5e43-103">Creates a computer group.</span></span>

## <span data-ttu-id="e5e43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5e43-104">SYNTAX</span></span>

```
New-AzOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5e43-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5e43-105">DESCRIPTION</span></span>
<span data-ttu-id="e5e43-106">A **New-AzOperationalInsightsComputerGroup** parancsmag egy számítógép-csoportot hoz létre egy erőforrás-csoportban és-helyen.</span><span class="sxs-lookup"><span data-stu-id="e5e43-106">The **New-AzOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="e5e43-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e5e43-107">EXAMPLES</span></span>

## <span data-ttu-id="e5e43-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5e43-108">PARAMETERS</span></span>

### <span data-ttu-id="e5e43-109">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="e5e43-109">-Category</span></span>
<span data-ttu-id="e5e43-110">A számítógép csoport kategóriáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5e43-110">Specifies the category of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e43-111">-DefaultProfile</span></span>
<span data-ttu-id="e5e43-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e5e43-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5e43-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e5e43-113">-DisplayName</span></span>
<span data-ttu-id="e5e43-114">A számítógép csoport megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5e43-114">Specifies the display name of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e43-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e5e43-115">-Force</span></span>
<span data-ttu-id="e5e43-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e5e43-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e43-117">-Query</span><span class="sxs-lookup"><span data-stu-id="e5e43-117">-Query</span></span>
<span data-ttu-id="e5e43-118">A számítógép csoport lekérdezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5e43-118">Specifies the query of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e43-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e43-119">-ResourceGroupName</span></span>
<span data-ttu-id="e5e43-120">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5e43-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e5e43-121">A parancsmag az erőforráscsoport számítógépcsoport csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e5e43-121">The cmdlet creates computer group in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e43-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="e5e43-122">-SavedSearchId</span></span>
<span data-ttu-id="e5e43-123">A számítógép csoportjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5e43-123">Specifies the ID of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e43-124">-Verzió</span><span class="sxs-lookup"><span data-stu-id="e5e43-124">-Version</span></span>
<span data-ttu-id="e5e43-125">A verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5e43-125">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e43-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e5e43-126">-WorkspaceName</span></span>
<span data-ttu-id="e5e43-127">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5e43-127">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e43-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5e43-128">-Confirm</span></span>
<span data-ttu-id="e5e43-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5e43-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e43-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5e43-130">-WhatIf</span></span>
<span data-ttu-id="e5e43-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5e43-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5e43-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5e43-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e43-133">CommonParameters</span></span>
<span data-ttu-id="e5e43-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5e43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e43-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e43-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e43-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5e43-136">INPUTS</span></span>

### <span data-ttu-id="e5e43-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e5e43-137">System.String</span></span>

### <span data-ttu-id="e5e43-138">System. Int64</span><span class="sxs-lookup"><span data-stu-id="e5e43-138">System.Int64</span></span>

## <span data-ttu-id="e5e43-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5e43-139">OUTPUTS</span></span>

### <span data-ttu-id="e5e43-140">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="e5e43-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="e5e43-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5e43-141">NOTES</span></span>

## <span data-ttu-id="e5e43-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5e43-142">RELATED LINKS</span></span>

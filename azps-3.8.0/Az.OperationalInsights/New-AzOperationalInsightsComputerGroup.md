---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
ms.openlocfilehash: 299c91e1db10aaabda7c7dfadf856b445d1b2993
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010639"
---
# <span data-ttu-id="68f04-101">New-AzOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="68f04-101">New-AzOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="68f04-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68f04-102">SYNOPSIS</span></span>
<span data-ttu-id="68f04-103">Számítógép-csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="68f04-103">Creates a computer group.</span></span>

## <span data-ttu-id="68f04-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68f04-104">SYNTAX</span></span>

```
New-AzOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68f04-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="68f04-105">DESCRIPTION</span></span>
<span data-ttu-id="68f04-106">A **New-AzOperationalInsightsComputerGroup** parancsmag egy számítógép-csoportot hoz létre egy erőforrás-csoportban és-helyen.</span><span class="sxs-lookup"><span data-stu-id="68f04-106">The **New-AzOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="68f04-107">Példák</span><span class="sxs-lookup"><span data-stu-id="68f04-107">EXAMPLES</span></span>

## <span data-ttu-id="68f04-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68f04-108">PARAMETERS</span></span>

### <span data-ttu-id="68f04-109">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="68f04-109">-Category</span></span>
<span data-ttu-id="68f04-110">A számítógép csoport kategóriáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="68f04-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="68f04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f04-111">-DefaultProfile</span></span>
<span data-ttu-id="68f04-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="68f04-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68f04-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="68f04-113">-DisplayName</span></span>
<span data-ttu-id="68f04-114">A számítógép csoport megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68f04-114">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="68f04-115">-Force</span><span class="sxs-lookup"><span data-stu-id="68f04-115">-Force</span></span>
<span data-ttu-id="68f04-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="68f04-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="68f04-117">-Query</span><span class="sxs-lookup"><span data-stu-id="68f04-117">-Query</span></span>
<span data-ttu-id="68f04-118">A számítógép csoport lekérdezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="68f04-118">Specifies the query of the computer group.</span></span>

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

### <span data-ttu-id="68f04-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68f04-119">-ResourceGroupName</span></span>
<span data-ttu-id="68f04-120">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68f04-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="68f04-121">A parancsmag az erőforráscsoport számítógépcsoport csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="68f04-121">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="68f04-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="68f04-122">-SavedSearchId</span></span>
<span data-ttu-id="68f04-123">A számítógép csoportjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="68f04-123">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="68f04-124">-Verzió</span><span class="sxs-lookup"><span data-stu-id="68f04-124">-Version</span></span>
<span data-ttu-id="68f04-125">A verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="68f04-125">Specifies the version.</span></span>

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

### <span data-ttu-id="68f04-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="68f04-126">-WorkspaceName</span></span>
<span data-ttu-id="68f04-127">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68f04-127">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="68f04-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="68f04-128">-Confirm</span></span>
<span data-ttu-id="68f04-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="68f04-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68f04-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68f04-130">-WhatIf</span></span>
<span data-ttu-id="68f04-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="68f04-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68f04-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68f04-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68f04-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f04-133">CommonParameters</span></span>
<span data-ttu-id="68f04-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68f04-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f04-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68f04-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f04-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68f04-136">INPUTS</span></span>

### <span data-ttu-id="68f04-137">System. String</span><span class="sxs-lookup"><span data-stu-id="68f04-137">System.String</span></span>

### <span data-ttu-id="68f04-138">System. Int64</span><span class="sxs-lookup"><span data-stu-id="68f04-138">System.Int64</span></span>

## <span data-ttu-id="68f04-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68f04-139">OUTPUTS</span></span>

### <span data-ttu-id="68f04-140">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="68f04-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="68f04-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68f04-141">NOTES</span></span>

## <span data-ttu-id="68f04-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68f04-142">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 247589f50028fb8d4cebf78f0ad45bb2124e43cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494978"
---
# <span data-ttu-id="ff4ea-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="ff4ea-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="ff4ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ff4ea-103">Új mentett keresést hoz létre a megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff4ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff4ea-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff4ea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff4ea-105">DESCRIPTION</span></span>
<span data-ttu-id="ff4ea-106">A **New-AzureRmOperationalInsightsSavedSearch** parancsmag új mentett keresést hoz létre a munkaterülethez megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="ff4ea-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ff4ea-107">EXAMPLES</span></span>

### <span data-ttu-id="ff4ea-108">1. példa: új mentett keresés létrehozása</span><span class="sxs-lookup"><span data-stu-id="ff4ea-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="ff4ea-109">Ezzel a paranccsal új mentett keresést hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="ff4ea-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff4ea-110">PARAMETERS</span></span>

### <span data-ttu-id="ff4ea-111">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="ff4ea-111">-Category</span></span>
<span data-ttu-id="ff4ea-112">A kategória nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="ff4ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff4ea-113">-DefaultProfile</span></span>
<span data-ttu-id="ff4ea-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ff4ea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4ea-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ff4ea-115">-DisplayName</span></span>
<span data-ttu-id="ff4ea-116">A mentett keresés megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="ff4ea-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ff4ea-117">-Force</span></span>
<span data-ttu-id="ff4ea-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ff4ea-119">-Query</span><span class="sxs-lookup"><span data-stu-id="ff4ea-119">-Query</span></span>
<span data-ttu-id="ff4ea-120">A lekérdezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="ff4ea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff4ea-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff4ea-122">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="ff4ea-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="ff4ea-123">-SavedSearchId</span></span>
<span data-ttu-id="ff4ea-124">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="ff4ea-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="ff4ea-125">-Tag</span></span>
<span data-ttu-id="ff4ea-126">A mentett keresési címkék.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-126">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4ea-127">-Verzió</span><span class="sxs-lookup"><span data-stu-id="ff4ea-127">-Version</span></span>
<span data-ttu-id="ff4ea-128">A verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-128">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4ea-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ff4ea-129">-WorkspaceName</span></span>
<span data-ttu-id="ff4ea-130">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="ff4ea-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff4ea-131">-Confirm</span></span>
<span data-ttu-id="ff4ea-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff4ea-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff4ea-133">-WhatIf</span></span>
<span data-ttu-id="ff4ea-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff4ea-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff4ea-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff4ea-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff4ea-136">CommonParameters</span></span>
<span data-ttu-id="ff4ea-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff4ea-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff4ea-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff4ea-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff4ea-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff4ea-139">INPUTS</span></span>

### <span data-ttu-id="ff4ea-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ff4ea-140">System.String</span></span>

### <span data-ttu-id="ff4ea-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ff4ea-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ff4ea-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="ff4ea-142">System.Int64</span></span>

## <span data-ttu-id="ff4ea-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff4ea-143">OUTPUTS</span></span>

### <span data-ttu-id="ff4ea-144">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="ff4ea-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="ff4ea-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff4ea-145">NOTES</span></span>

## <span data-ttu-id="ff4ea-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff4ea-146">RELATED LINKS</span></span>

[<span data-ttu-id="ff4ea-147">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="ff4ea-147">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)



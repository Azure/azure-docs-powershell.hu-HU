---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: ebea93e7d59e0740aa21e909f35779857aacba01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493394"
---
# <span data-ttu-id="90a6b-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="90a6b-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="90a6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="90a6b-103">Már létezik mentett keresés frissítése.</span><span class="sxs-lookup"><span data-stu-id="90a6b-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90a6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90a6b-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tags] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90a6b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="90a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="90a6b-106">A **set-AzureRmOperationalInsightsSavedSearch** parancsmag a már létező mentett keresést frissíti.</span><span class="sxs-lookup"><span data-stu-id="90a6b-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="90a6b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="90a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="90a6b-108">1. példa: mentett keresés megadása frissített tulajdonságokkal</span><span class="sxs-lookup"><span data-stu-id="90a6b-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="90a6b-109">Ezzel a paranccsal a mentett keresések frissített tulajdonságokkal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="90a6b-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="90a6b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90a6b-110">PARAMETERS</span></span>

### <span data-ttu-id="90a6b-111">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="90a6b-111">-Category</span></span>
<span data-ttu-id="90a6b-112">A kategória nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a6b-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="90a6b-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="90a6b-113">-DisplayName</span></span>
<span data-ttu-id="90a6b-114">A megjelenítendő nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a6b-114">Specifies the display name.</span></span>

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

### <span data-ttu-id="90a6b-115">-ETag</span><span class="sxs-lookup"><span data-stu-id="90a6b-115">-ETag</span></span>
<span data-ttu-id="90a6b-116">A ETag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a6b-116">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90a6b-117">-Query</span><span class="sxs-lookup"><span data-stu-id="90a6b-117">-Query</span></span>
<span data-ttu-id="90a6b-118">A lekérdezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a6b-118">Specifies the query name.</span></span>

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

### <span data-ttu-id="90a6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90a6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="90a6b-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a6b-120">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="90a6b-121">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="90a6b-121">-SavedSearchId</span></span>
<span data-ttu-id="90a6b-122">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a6b-122">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="90a6b-123">-Címkék</span><span class="sxs-lookup"><span data-stu-id="90a6b-123">-Tags</span></span>
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

### <span data-ttu-id="90a6b-124">-Verzió</span><span class="sxs-lookup"><span data-stu-id="90a6b-124">-Version</span></span>
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

### <span data-ttu-id="90a6b-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="90a6b-125">-WorkspaceName</span></span>
<span data-ttu-id="90a6b-126">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a6b-126">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="90a6b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a6b-127">-DefaultProfile</span></span>
<span data-ttu-id="90a6b-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90a6b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90a6b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a6b-129">CommonParameters</span></span>
<span data-ttu-id="90a6b-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90a6b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a6b-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a6b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a6b-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90a6b-132">INPUTS</span></span>

## <span data-ttu-id="90a6b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90a6b-133">OUTPUTS</span></span>

## <span data-ttu-id="90a6b-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90a6b-134">NOTES</span></span>

## <span data-ttu-id="90a6b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90a6b-135">RELATED LINKS</span></span>

[<span data-ttu-id="90a6b-136">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="90a6b-136">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)



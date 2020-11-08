---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017977"
---
# <span data-ttu-id="2f891-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2f891-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="2f891-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f891-102">SYNOPSIS</span></span>
<span data-ttu-id="2f891-103">Az alkalmazásban betekintést kap a hivatkozásokat tároló fiók</span><span class="sxs-lookup"><span data-stu-id="2f891-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="2f891-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f891-104">SYNTAX</span></span>

### <span data-ttu-id="2f891-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f891-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f891-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f891-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f891-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f891-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f891-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f891-108">DESCRIPTION</span></span>
<span data-ttu-id="2f891-109">Az alkalmazásban betekintést kap a hivatkozásokat tároló fiók</span><span class="sxs-lookup"><span data-stu-id="2f891-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="2f891-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2f891-110">EXAMPLES</span></span>

### <span data-ttu-id="2f891-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2f891-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="2f891-112">A "componentName" összetevőhöz társított csatolt tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="2f891-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="2f891-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f891-113">PARAMETERS</span></span>

### <span data-ttu-id="2f891-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="2f891-114">-ComponentName</span></span>
<span data-ttu-id="2f891-115">Összetevő neve</span><span class="sxs-lookup"><span data-stu-id="2f891-115">Component Name</span></span>

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

### <span data-ttu-id="2f891-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f891-116">-DefaultProfile</span></span>
<span data-ttu-id="2f891-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f891-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f891-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f891-118">-InputObject</span></span>
<span data-ttu-id="2f891-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2f891-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f891-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f891-120">-ResourceGroupName</span></span>
<span data-ttu-id="2f891-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="2f891-121">Resource Group Name</span></span>

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

### <span data-ttu-id="2f891-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f891-122">-ResourceId</span></span>
<span data-ttu-id="2f891-123">Összetevő-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f891-123">Component ResourceId</span></span>

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

### <span data-ttu-id="2f891-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f891-124">CommonParameters</span></span>
<span data-ttu-id="2f891-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f891-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f891-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2f891-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f891-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f891-127">INPUTS</span></span>

### <span data-ttu-id="2f891-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2f891-128">System.String</span></span>

### <span data-ttu-id="2f891-129">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2f891-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="2f891-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f891-130">OUTPUTS</span></span>

### <span data-ttu-id="2f891-131">Microsoft. Azure. Command. ApplicationInsights. models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="2f891-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="2f891-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f891-132">NOTES</span></span>

## <span data-ttu-id="2f891-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f891-133">RELATED LINKS</span></span>

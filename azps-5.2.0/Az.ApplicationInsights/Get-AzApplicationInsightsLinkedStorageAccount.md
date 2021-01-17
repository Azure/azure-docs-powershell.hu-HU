---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353549"
---
# <span data-ttu-id="898a7-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="898a7-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="898a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="898a7-102">SYNOPSIS</span></span>
<span data-ttu-id="898a7-103">Alkalmazásstatikációkhoz kapcsolt tárfiók lekérte</span><span class="sxs-lookup"><span data-stu-id="898a7-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="898a7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="898a7-104">SYNTAX</span></span>

### <span data-ttu-id="898a7-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="898a7-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="898a7-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="898a7-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="898a7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="898a7-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="898a7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="898a7-108">DESCRIPTION</span></span>
<span data-ttu-id="898a7-109">Alkalmazásstatikációkhoz kapcsolt tárfiók lekérte</span><span class="sxs-lookup"><span data-stu-id="898a7-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="898a7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="898a7-110">EXAMPLES</span></span>

### <span data-ttu-id="898a7-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="898a7-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="898a7-112">Az "componentName" összetevővel társított csatolt tárfiók bekérte</span><span class="sxs-lookup"><span data-stu-id="898a7-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="898a7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="898a7-113">PARAMETERS</span></span>

### <span data-ttu-id="898a7-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="898a7-114">-ComponentName</span></span>
<span data-ttu-id="898a7-115">Összetevő neve</span><span class="sxs-lookup"><span data-stu-id="898a7-115">Component Name</span></span>

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

### <span data-ttu-id="898a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="898a7-116">-DefaultProfile</span></span>
<span data-ttu-id="898a7-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="898a7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="898a7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="898a7-118">-InputObject</span></span>
<span data-ttu-id="898a7-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="898a7-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="898a7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="898a7-120">-ResourceGroupName</span></span>
<span data-ttu-id="898a7-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="898a7-121">Resource Group Name</span></span>

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

### <span data-ttu-id="898a7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="898a7-122">-ResourceId</span></span>
<span data-ttu-id="898a7-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="898a7-123">Component ResourceId</span></span>

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

### <span data-ttu-id="898a7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="898a7-124">CommonParameters</span></span>
<span data-ttu-id="898a7-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="898a7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="898a7-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="898a7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="898a7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="898a7-127">INPUTS</span></span>

### <span data-ttu-id="898a7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="898a7-128">System.String</span></span>

### <span data-ttu-id="898a7-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="898a7-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="898a7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="898a7-130">OUTPUTS</span></span>

### <span data-ttu-id="898a7-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="898a7-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="898a7-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="898a7-132">NOTES</span></span>

## <span data-ttu-id="898a7-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="898a7-133">RELATED LINKS</span></span>

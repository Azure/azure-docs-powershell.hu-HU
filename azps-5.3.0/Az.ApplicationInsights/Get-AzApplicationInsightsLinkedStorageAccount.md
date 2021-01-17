---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381358"
---
# <span data-ttu-id="4d366-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4d366-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="4d366-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d366-102">SYNOPSIS</span></span>
<span data-ttu-id="4d366-103">Alkalmazásstatikációkhoz kapcsolt tárfiók lekérte</span><span class="sxs-lookup"><span data-stu-id="4d366-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="4d366-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4d366-104">SYNTAX</span></span>

### <span data-ttu-id="4d366-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d366-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d366-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d366-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d366-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d366-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d366-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4d366-108">DESCRIPTION</span></span>
<span data-ttu-id="4d366-109">Alkalmazásstatikációkhoz kapcsolt tárfiók lekérte</span><span class="sxs-lookup"><span data-stu-id="4d366-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="4d366-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4d366-110">EXAMPLES</span></span>

### <span data-ttu-id="4d366-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4d366-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="4d366-112">A "componentName" összetevővel társított csatolt tárfiók bekérte</span><span class="sxs-lookup"><span data-stu-id="4d366-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="4d366-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d366-113">PARAMETERS</span></span>

### <span data-ttu-id="4d366-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="4d366-114">-ComponentName</span></span>
<span data-ttu-id="4d366-115">Összetevő neve</span><span class="sxs-lookup"><span data-stu-id="4d366-115">Component Name</span></span>

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

### <span data-ttu-id="4d366-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d366-116">-DefaultProfile</span></span>
<span data-ttu-id="4d366-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d366-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d366-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d366-118">-InputObject</span></span>
<span data-ttu-id="4d366-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4d366-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="4d366-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d366-120">-ResourceGroupName</span></span>
<span data-ttu-id="4d366-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4d366-121">Resource Group Name</span></span>

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

### <span data-ttu-id="4d366-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d366-122">-ResourceId</span></span>
<span data-ttu-id="4d366-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d366-123">Component ResourceId</span></span>

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

### <span data-ttu-id="4d366-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d366-124">CommonParameters</span></span>
<span data-ttu-id="4d366-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d366-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d366-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d366-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d366-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d366-127">INPUTS</span></span>

### <span data-ttu-id="4d366-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4d366-128">System.String</span></span>

### <span data-ttu-id="4d366-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4d366-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="4d366-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d366-130">OUTPUTS</span></span>

### <span data-ttu-id="4d366-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="4d366-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="4d366-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4d366-132">NOTES</span></span>

## <span data-ttu-id="4d366-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d366-133">RELATED LINKS</span></span>

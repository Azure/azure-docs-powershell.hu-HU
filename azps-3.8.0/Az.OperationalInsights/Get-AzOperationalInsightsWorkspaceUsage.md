---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: c1054e8dfb9a9133da740c5162c8e8f60c9df5d1
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017275"
---
# <span data-ttu-id="2948e-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="2948e-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="2948e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2948e-102">SYNOPSIS</span></span>
<span data-ttu-id="2948e-103">A munkaterület használati adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="2948e-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="2948e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2948e-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2948e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2948e-105">DESCRIPTION</span></span>
<span data-ttu-id="2948e-106">A **Get-AzOperationalInsightsWorkspaceUsage** parancsmag kikeresi a munkaterület használati adatait.</span><span class="sxs-lookup"><span data-stu-id="2948e-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="2948e-107">Ez a cikk bemutatja, hogy mennyi adatot elemeztek a munkaterület egy bizonyos időszakra.</span><span class="sxs-lookup"><span data-stu-id="2948e-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="2948e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2948e-108">EXAMPLES</span></span>

### <span data-ttu-id="2948e-109">Példa 1: használati érték beszerzése munkaterületi név szerint</span><span class="sxs-lookup"><span data-stu-id="2948e-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="2948e-110">Ez a parancs a megadott erőforráscsoport MyWorkspace nevű munkaterülete használati adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2948e-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="2948e-111">2. példa: használati adatainak beszerzése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="2948e-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="2948e-112">Ez a parancs a MyWorkSpace nevű munkaterületet az Get-AzOperationalInsightsWorkspace parancsmag segítségével kapja meg, majd átadja a munkaterületet az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="2948e-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="2948e-113">A parancs kinyeri az adott munkaterület használati adatait.</span><span class="sxs-lookup"><span data-stu-id="2948e-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="2948e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2948e-114">PARAMETERS</span></span>

### <span data-ttu-id="2948e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2948e-115">-DefaultProfile</span></span>
<span data-ttu-id="2948e-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2948e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2948e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2948e-117">-Name</span></span>
<span data-ttu-id="2948e-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2948e-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2948e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2948e-119">-ResourceGroupName</span></span>
<span data-ttu-id="2948e-120">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2948e-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="2948e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2948e-121">CommonParameters</span></span>
<span data-ttu-id="2948e-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2948e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2948e-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2948e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2948e-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2948e-124">INPUTS</span></span>

### <span data-ttu-id="2948e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2948e-125">System.String</span></span>

## <span data-ttu-id="2948e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2948e-126">OUTPUTS</span></span>

### <span data-ttu-id="2948e-127">Microsoft. Azure. Command. OperationalInsights. models. PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="2948e-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="2948e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2948e-128">NOTES</span></span>

## <span data-ttu-id="2948e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2948e-129">RELATED LINKS</span></span>

[<span data-ttu-id="2948e-130">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="2948e-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="2948e-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="2948e-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



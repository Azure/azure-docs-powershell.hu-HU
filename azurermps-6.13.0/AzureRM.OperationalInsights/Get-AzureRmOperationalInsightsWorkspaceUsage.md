---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: fa238d963f472e79946632311a9f93c8586650ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505287"
---
# <span data-ttu-id="fae76-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="fae76-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="fae76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fae76-102">SYNOPSIS</span></span>
<span data-ttu-id="fae76-103">A munkaterület használati adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="fae76-103">Gets the usage data for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fae76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fae76-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fae76-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fae76-105">DESCRIPTION</span></span>
<span data-ttu-id="fae76-106">A **Get-AzureRmOperationalInsightsWorkspaceUsage** parancsmag kikeresi a munkaterület használati adatait.</span><span class="sxs-lookup"><span data-stu-id="fae76-106">The **Get-AzureRmOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="fae76-107">Ez a cikk bemutatja, hogy mennyi adatot elemeztek a munkaterület egy bizonyos időszakra.</span><span class="sxs-lookup"><span data-stu-id="fae76-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="fae76-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fae76-108">EXAMPLES</span></span>

### <span data-ttu-id="fae76-109">Példa 1: használati érték beszerzése munkaterületi név szerint</span><span class="sxs-lookup"><span data-stu-id="fae76-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="fae76-110">Ez a parancs a megadott erőforráscsoport MyWorkspace nevű munkaterülete használati adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fae76-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="fae76-111">2. példa: használati adatainak beszerzése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="fae76-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="fae76-112">Ez a parancs a MyWorkSpace nevű munkaterületet az Get-AzureRmOperationalInsightsWorkspace parancsmag segítségével kapja meg, majd átadja a munkaterületet az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="fae76-112">This command gets the workspace named MyWorkSpace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="fae76-113">A parancs kinyeri az adott munkaterület használati adatait.</span><span class="sxs-lookup"><span data-stu-id="fae76-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="fae76-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fae76-114">PARAMETERS</span></span>

### <span data-ttu-id="fae76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae76-115">-DefaultProfile</span></span>
<span data-ttu-id="fae76-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fae76-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fae76-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fae76-117">-Name</span></span>
<span data-ttu-id="fae76-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fae76-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="fae76-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae76-119">-ResourceGroupName</span></span>
<span data-ttu-id="fae76-120">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fae76-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="fae76-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae76-121">CommonParameters</span></span>
<span data-ttu-id="fae76-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fae76-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae76-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fae76-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae76-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fae76-124">INPUTS</span></span>

### <span data-ttu-id="fae76-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fae76-125">System.String</span></span>

## <span data-ttu-id="fae76-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fae76-126">OUTPUTS</span></span>

### <span data-ttu-id="fae76-127">Microsoft. Azure. Command. OperationalInsights. models. PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="fae76-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="fae76-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fae76-128">NOTES</span></span>

## <span data-ttu-id="fae76-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fae76-129">RELATED LINKS</span></span>

[<span data-ttu-id="fae76-130">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fae76-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="fae76-131">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="fae76-131">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)



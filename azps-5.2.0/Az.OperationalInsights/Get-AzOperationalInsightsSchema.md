---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343361"
---
# <span data-ttu-id="c7910-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="c7910-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="c7910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7910-102">SYNOPSIS</span></span>
<span data-ttu-id="c7910-103">A munkaterülethez társított sémát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c7910-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="c7910-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c7910-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7910-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c7910-105">DESCRIPTION</span></span>
<span data-ttu-id="c7910-106">A **Get-AzOperationalInsightsSchema** parancsmag az erőforráscsoporton belül a megadott munkaterülethez társított sémát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="c7910-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="c7910-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c7910-107">EXAMPLES</span></span>

### <span data-ttu-id="c7910-108">1. példa: A munkaterület sémájának lekérte</span><span class="sxs-lookup"><span data-stu-id="c7910-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="c7910-109">Ez a parancs a munkaterülethez társított sémákat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c7910-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="c7910-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7910-110">PARAMETERS</span></span>

### <span data-ttu-id="c7910-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7910-111">-DefaultProfile</span></span>
<span data-ttu-id="c7910-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c7910-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7910-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7910-113">-ResourceGroupName</span></span>
<span data-ttu-id="c7910-114">Egy munkaterületet tartalmazó Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7910-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c7910-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c7910-115">-WorkspaceName</span></span>
<span data-ttu-id="c7910-116">Munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c7910-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="c7910-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7910-117">CommonParameters</span></span>
<span data-ttu-id="c7910-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7910-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7910-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7910-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7910-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7910-120">INPUTS</span></span>

### <span data-ttu-id="c7910-121">System.String</span><span class="sxs-lookup"><span data-stu-id="c7910-121">System.String</span></span>

## <span data-ttu-id="c7910-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7910-122">OUTPUTS</span></span>

### <span data-ttu-id="c7910-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="c7910-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="c7910-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c7910-124">NOTES</span></span>

## <span data-ttu-id="c7910-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7910-125">RELATED LINKS</span></span>

[<span data-ttu-id="c7910-126">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c7910-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



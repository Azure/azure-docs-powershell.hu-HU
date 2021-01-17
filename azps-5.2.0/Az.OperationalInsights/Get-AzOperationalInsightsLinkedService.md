---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370256"
---
# <span data-ttu-id="7a1fd-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="7a1fd-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="7a1fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="7a1fd-103">Csatolt szolgáltatás le- vagy listába való be- vagy listából munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="7a1fd-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="7a1fd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7a1fd-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a1fd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7a1fd-105">DESCRIPTION</span></span>
<span data-ttu-id="7a1fd-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span><span class="sxs-lookup"><span data-stu-id="7a1fd-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="7a1fd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7a1fd-107">EXAMPLES</span></span>

### <span data-ttu-id="7a1fd-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7a1fd-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="7a1fd-109">Csatolt munkaterület-szolgáltatás lekérte</span><span class="sxs-lookup"><span data-stu-id="7a1fd-109">Get linked service for workspace</span></span>

## <span data-ttu-id="7a1fd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a1fd-110">PARAMETERS</span></span>

### <span data-ttu-id="7a1fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a1fd-111">-DefaultProfile</span></span>
<span data-ttu-id="7a1fd-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1fd-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="7a1fd-113">-LinkedServiceName</span></span>
<span data-ttu-id="7a1fd-114">A hivatkozott szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-114">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1fd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a1fd-115">-ResourceGroupName</span></span>
<span data-ttu-id="7a1fd-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1fd-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7a1fd-117">-WorkspaceName</span></span>
<span data-ttu-id="7a1fd-118">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-118">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a1fd-119">CommonParameters</span></span>
<span data-ttu-id="7a1fd-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a1fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a1fd-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a1fd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a1fd-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a1fd-122">INPUTS</span></span>

### <span data-ttu-id="7a1fd-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7a1fd-123">System.String</span></span>

## <span data-ttu-id="7a1fd-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a1fd-124">OUTPUTS</span></span>

### <span data-ttu-id="7a1fd-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="7a1fd-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="7a1fd-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7a1fd-126">NOTES</span></span>

## <span data-ttu-id="7a1fd-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a1fd-127">RELATED LINKS</span></span>

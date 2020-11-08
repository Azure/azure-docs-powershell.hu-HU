---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187576"
---
# <span data-ttu-id="79006-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="79006-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="79006-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79006-102">SYNOPSIS</span></span>
<span data-ttu-id="79006-103">Munkaterülethez kapcsolt szolgáltatás beszerzése vagy listázása</span><span class="sxs-lookup"><span data-stu-id="79006-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="79006-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79006-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79006-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="79006-105">DESCRIPTION</span></span>
<span data-ttu-id="79006-106">A munkaterülethez kapcsolt szolgáltatások beolvasása vagy listázása, a lista, ha a "-LinkedServiceName" nem volt megadva</span><span class="sxs-lookup"><span data-stu-id="79006-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="79006-107">Példák</span><span class="sxs-lookup"><span data-stu-id="79006-107">EXAMPLES</span></span>

### <span data-ttu-id="79006-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="79006-108">Example 1</span></span>
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

<span data-ttu-id="79006-109">Kapcsolt szolgáltatás beszerzése munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="79006-109">Get linked service for workspace</span></span>

## <span data-ttu-id="79006-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79006-110">PARAMETERS</span></span>

### <span data-ttu-id="79006-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79006-111">-DefaultProfile</span></span>
<span data-ttu-id="79006-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79006-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79006-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="79006-113">-LinkedServiceName</span></span>
<span data-ttu-id="79006-114">A kapcsolt szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="79006-114">The linked service name.</span></span>

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

### <span data-ttu-id="79006-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79006-115">-ResourceGroupName</span></span>
<span data-ttu-id="79006-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="79006-116">The resource group name.</span></span>

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

### <span data-ttu-id="79006-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="79006-117">-WorkspaceName</span></span>
<span data-ttu-id="79006-118">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="79006-118">The workspace name.</span></span>

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

### <span data-ttu-id="79006-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79006-119">CommonParameters</span></span>
<span data-ttu-id="79006-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79006-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79006-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="79006-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79006-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79006-122">INPUTS</span></span>

### <span data-ttu-id="79006-123">System. String</span><span class="sxs-lookup"><span data-stu-id="79006-123">System.String</span></span>

## <span data-ttu-id="79006-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79006-124">OUTPUTS</span></span>

### <span data-ttu-id="79006-125">Microsoft. Azure. Command. OperationalInsights. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="79006-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="79006-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79006-126">NOTES</span></span>

## <span data-ttu-id="79006-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79006-127">RELATED LINKS</span></span>

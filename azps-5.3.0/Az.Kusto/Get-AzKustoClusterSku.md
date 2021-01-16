---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 42fed776d1f77211c7967dd6313d0ddd1e04b65a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466369"
---
# <span data-ttu-id="a05b2-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="a05b2-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="a05b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a05b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a05b2-103">A Kusto-erőforrásszolgáltatóhoz használható, erre jogosult termékek listája.</span><span class="sxs-lookup"><span data-stu-id="a05b2-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="a05b2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a05b2-104">SYNTAX</span></span>

### <span data-ttu-id="a05b2-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a05b2-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a05b2-106">Lista1</span><span class="sxs-lookup"><span data-stu-id="a05b2-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a05b2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a05b2-107">DESCRIPTION</span></span>
<span data-ttu-id="a05b2-108">A Kusto-erőforrásszolgáltatóhoz használható, erre jogosult termékek listája.</span><span class="sxs-lookup"><span data-stu-id="a05b2-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="a05b2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a05b2-109">EXAMPLES</span></span>

### <span data-ttu-id="a05b2-110">1. példa: A jogosult termékek listája</span><span class="sxs-lookup"><span data-stu-id="a05b2-110">Example 1: Lists eligible SKUs</span></span>
```powershell
PS C:\> Get-AzKustoClusterSku

Location             Name                        ResourceType Tier
--------             ----                        ------------ ----
{eastus2}            D13_v2                      clusters     Standard
{eastus2}            D14_v2                      clusters     Standard
{eastus2}            L8                          clusters     Standard
{eastus2}            L16                         clusters     Standard
{eastus2}            D11_v2                      clusters     Standard
{eastus2}            D12_v2                      clusters     Standard
{eastus2}            L4                          clusters     Standard
{eastus2}            Standard_D13_v2             clusters     Standard
{eastus2}            Standard_D14_v2             clusters     Standard
{eastus2}            Standard_L8s                clusters     Standard
{eastus2}            Standard_L16s               clusters     Standard
{eastus2}            Standard_D11_v2             clusters     Standard
{eastus2}            Standard_D12_v2             clusters     Standard
{eastus2}            Standard_L4s                clusters     Standard
{eastus2}            Standard_DS13_v2+1TB_PS     clusters     Standard
{eastus2}            Standard_DS13_v2+2TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+3TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+4TB_PS     clusters     Standard
{eastus2}            Dev(No SLA)_Standard_D11_v2 clusters     Basic
{westcentralus}      D13_v2                      clusters     Standard
{westcentralus}      D14_v2                      clusters     Standard
{westcentralus}      D11_v2                      clusters     Standard
{westcentralus}      D12_v2                      clusters     Standard
{westcentralus}      Standard_D13_v2             clusters     Standard
{westcentralus}      Standard_D14_v2             clusters     Standard
{westcentralus}      Standard_D11_v2             clusters     Standard
{westcentralus}      Standard_D12_v2             clusters     Standard
{westcentralus}      Standard_DS13_v2+1TB_PS     clusters     Standard
{westcentralus}      Standard_DS13_v2+2TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+3TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+4TB_PS     clusters     Standard
...
```

<span data-ttu-id="a05b2-111">A fenti parancs felsorolja a jogosult SKUs-okat.</span><span class="sxs-lookup"><span data-stu-id="a05b2-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="a05b2-112">2. példa: Az adott fürtre vonatkozó, jogosult termékkódok listája</span><span class="sxs-lookup"><span data-stu-id="a05b2-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
```powershell
PS C:\>  Get-AzKustoClusterSku -ResourceGroupName testrg -ClusterName testnewkustocluster

ResourceType
------------
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
...
```

<span data-ttu-id="a05b2-113">A fenti parancs felsorolja az adott fürtre vonatkozó, jogosult termékkódokat.</span><span class="sxs-lookup"><span data-stu-id="a05b2-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="a05b2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a05b2-114">PARAMETERS</span></span>

### <span data-ttu-id="a05b2-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a05b2-115">-ClusterName</span></span>
<span data-ttu-id="a05b2-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="a05b2-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a05b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05b2-117">-DefaultProfile</span></span>
<span data-ttu-id="a05b2-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a05b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a05b2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05b2-119">-ResourceGroupName</span></span>
<span data-ttu-id="a05b2-120">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a05b2-120">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a05b2-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a05b2-121">-SubscriptionId</span></span>
<span data-ttu-id="a05b2-122">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="a05b2-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a05b2-123">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a05b2-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a05b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05b2-124">CommonParameters</span></span>
<span data-ttu-id="a05b2-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a05b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05b2-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a05b2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05b2-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a05b2-127">INPUTS</span></span>

## <span data-ttu-id="a05b2-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a05b2-128">OUTPUTS</span></span>

### <span data-ttu-id="a05b2-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="a05b2-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span></span>

### <span data-ttu-id="a05b2-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="a05b2-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span></span>

## <span data-ttu-id="a05b2-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a05b2-131">NOTES</span></span>

<span data-ttu-id="a05b2-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a05b2-132">ALIASES</span></span>

## <span data-ttu-id="a05b2-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a05b2-133">RELATED LINKS</span></span>


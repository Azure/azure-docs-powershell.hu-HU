---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 88b3104512b1cad4cddf98f521b44c6b638c05b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025676"
---
# <span data-ttu-id="4d512-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="4d512-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="4d512-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d512-102">SYNOPSIS</span></span>
<span data-ttu-id="4d512-103">A Kusto erőforrás-szolgáltató számára feljogosított SKU-ket jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="4d512-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="4d512-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d512-104">SYNTAX</span></span>

### <span data-ttu-id="4d512-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d512-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d512-106">Lista1</span><span class="sxs-lookup"><span data-stu-id="4d512-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4d512-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d512-107">DESCRIPTION</span></span>
<span data-ttu-id="4d512-108">A Kusto erőforrás-szolgáltató számára feljogosított SKU-ket jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="4d512-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="4d512-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4d512-109">EXAMPLES</span></span>

### <span data-ttu-id="4d512-110">Példa 1: támogatható SKU-listák</span><span class="sxs-lookup"><span data-stu-id="4d512-110">Example 1: Lists eligible SKUs</span></span>
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

<span data-ttu-id="4d512-111">A fenti parancs a feljogosított SKU-t sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="4d512-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="4d512-112">2. példa: meghatározott szektorcsoportokra feljogosított SKU-listák</span><span class="sxs-lookup"><span data-stu-id="4d512-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
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

<span data-ttu-id="4d512-113">A fenti parancs megjeleníti a megfelelő SKU-ot adott fürtökhöz.</span><span class="sxs-lookup"><span data-stu-id="4d512-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="4d512-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d512-114">PARAMETERS</span></span>

### <span data-ttu-id="4d512-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="4d512-115">-ClusterName</span></span>
<span data-ttu-id="4d512-116">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="4d512-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4d512-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d512-117">-DefaultProfile</span></span>
<span data-ttu-id="4d512-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d512-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d512-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d512-119">-ResourceGroupName</span></span>
<span data-ttu-id="4d512-120">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d512-120">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4d512-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d512-121">-SubscriptionId</span></span>
<span data-ttu-id="4d512-122">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4d512-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4d512-123">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="4d512-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4d512-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d512-124">CommonParameters</span></span>
<span data-ttu-id="4d512-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d512-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d512-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4d512-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d512-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d512-127">INPUTS</span></span>

## <span data-ttu-id="4d512-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d512-128">OUTPUTS</span></span>

### <span data-ttu-id="4d512-129">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="4d512-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAzureResourceSku</span></span>

### <span data-ttu-id="4d512-130">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="4d512-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ISkuDescription</span></span>

## <span data-ttu-id="4d512-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d512-131">NOTES</span></span>

<span data-ttu-id="4d512-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4d512-132">ALIASES</span></span>

## <span data-ttu-id="4d512-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d512-133">RELATED LINKS</span></span>


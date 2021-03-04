---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: 5b53c9806fa541c28b7f318f464a26e9a88104e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924873"
---
# <span data-ttu-id="d92c8-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="d92c8-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="d92c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d92c8-102">SYNOPSIS</span></span>
<span data-ttu-id="d92c8-103">A fürt tulajdonában lévő és egy másik fürt által követett adatbázisok listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d92c8-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="d92c8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d92c8-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d92c8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d92c8-105">DESCRIPTION</span></span>
<span data-ttu-id="d92c8-106">A fürt tulajdonában lévő és egy másik fürt által követett adatbázisok listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d92c8-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="d92c8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d92c8-107">EXAMPLES</span></span>

### <span data-ttu-id="d92c8-108">1. példa: Az összes követett adatbázis felsorolása</span><span class="sxs-lookup"><span data-stu-id="d92c8-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="d92c8-109">A fenti parancs felsorolja az összes adatbázist, amely a fürt tulajdonában van, és amelyet egy másik fürt követett.</span><span class="sxs-lookup"><span data-stu-id="d92c8-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="d92c8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d92c8-110">PARAMETERS</span></span>

### <span data-ttu-id="d92c8-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d92c8-111">-ClusterName</span></span>
<span data-ttu-id="d92c8-112">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="d92c8-112">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d92c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d92c8-113">-DefaultProfile</span></span>
<span data-ttu-id="d92c8-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d92c8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d92c8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d92c8-115">-ResourceGroupName</span></span>
<span data-ttu-id="d92c8-116">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d92c8-116">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d92c8-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d92c8-117">-SubscriptionId</span></span>
<span data-ttu-id="d92c8-118">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="d92c8-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d92c8-119">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="d92c8-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d92c8-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d92c8-120">-Confirm</span></span>
<span data-ttu-id="d92c8-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d92c8-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d92c8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d92c8-122">-WhatIf</span></span>
<span data-ttu-id="d92c8-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d92c8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d92c8-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d92c8-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d92c8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d92c8-125">CommonParameters</span></span>
<span data-ttu-id="d92c8-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d92c8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d92c8-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d92c8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d92c8-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d92c8-128">INPUTS</span></span>

## <span data-ttu-id="d92c8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d92c8-129">OUTPUTS</span></span>

### <span data-ttu-id="d92c8-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFowerwerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="d92c8-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="d92c8-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d92c8-131">NOTES</span></span>

<span data-ttu-id="d92c8-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d92c8-132">ALIASES</span></span>

## <span data-ttu-id="d92c8-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d92c8-133">RELATED LINKS</span></span>


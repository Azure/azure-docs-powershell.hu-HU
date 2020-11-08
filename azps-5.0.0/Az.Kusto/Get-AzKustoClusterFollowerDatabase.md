---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: e35e0731fb14cf8ca45b6e56d3957d13ccb88398
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194733"
---
# <span data-ttu-id="e9394-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="e9394-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="e9394-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9394-102">SYNOPSIS</span></span>
<span data-ttu-id="e9394-103">Azoknak az adatbázisoknak a listáját jeleníti meg, amelyek a fürt tulajdonosa, és amelyeket egy másik fürt követett.</span><span class="sxs-lookup"><span data-stu-id="e9394-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="e9394-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9394-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e9394-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9394-105">DESCRIPTION</span></span>
<span data-ttu-id="e9394-106">Azoknak az adatbázisoknak a listáját jeleníti meg, amelyek a fürt tulajdonosa, és amelyeket egy másik fürt követett.</span><span class="sxs-lookup"><span data-stu-id="e9394-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="e9394-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e9394-107">EXAMPLES</span></span>

### <span data-ttu-id="e9394-108">Példa 1: az összes követett adatbázis listázása</span><span class="sxs-lookup"><span data-stu-id="e9394-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="e9394-109">A fenti parancs felsorolja az összes olyan adatbázist, amely a fürt tulajdonosa, és amelyet egy másik fürt követett.</span><span class="sxs-lookup"><span data-stu-id="e9394-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="e9394-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9394-110">PARAMETERS</span></span>

### <span data-ttu-id="e9394-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="e9394-111">-ClusterName</span></span>
<span data-ttu-id="e9394-112">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="e9394-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e9394-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9394-113">-DefaultProfile</span></span>
<span data-ttu-id="e9394-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9394-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9394-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9394-115">-ResourceGroupName</span></span>
<span data-ttu-id="e9394-116">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e9394-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e9394-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e9394-117">-SubscriptionId</span></span>
<span data-ttu-id="e9394-118">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e9394-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e9394-119">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e9394-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e9394-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e9394-120">-Confirm</span></span>
<span data-ttu-id="e9394-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e9394-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9394-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9394-122">-WhatIf</span></span>
<span data-ttu-id="e9394-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e9394-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9394-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e9394-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9394-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9394-125">CommonParameters</span></span>
<span data-ttu-id="e9394-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9394-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9394-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e9394-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9394-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9394-128">INPUTS</span></span>

## <span data-ttu-id="e9394-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9394-129">OUTPUTS</span></span>

### <span data-ttu-id="e9394-130">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="e9394-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="e9394-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9394-131">NOTES</span></span>

<span data-ttu-id="e9394-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e9394-132">ALIASES</span></span>

## <span data-ttu-id="e9394-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9394-133">RELATED LINKS</span></span>


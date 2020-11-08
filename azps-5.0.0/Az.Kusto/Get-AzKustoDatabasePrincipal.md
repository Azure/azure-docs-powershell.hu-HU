---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c9b25327d170d05a4c2ad97b3cb7ce7626fbfec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194722"
---
# <span data-ttu-id="b5197-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="b5197-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="b5197-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5197-102">SYNOPSIS</span></span>
<span data-ttu-id="b5197-103">A megadott Kusto-fürtöt és-adatbázist tartalmazó adatbázis-résztvevők listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b5197-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="b5197-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5197-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b5197-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5197-105">DESCRIPTION</span></span>
<span data-ttu-id="b5197-106">A megadott Kusto-fürtöt és-adatbázist tartalmazó adatbázis-résztvevők listáját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b5197-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="b5197-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b5197-107">EXAMPLES</span></span>

### <span data-ttu-id="b5197-108">1. példa: az adott Kusto-ös fürt és adatbázis adatbázis-vezetőinek listája</span><span class="sxs-lookup"><span data-stu-id="b5197-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="b5197-109">A fenti parancs visszaadja az adatbázis-résztvevők listáját az adott Kusto-fürtből és-adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="b5197-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="b5197-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5197-110">PARAMETERS</span></span>

### <span data-ttu-id="b5197-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="b5197-111">-ClusterName</span></span>
<span data-ttu-id="b5197-112">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b5197-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b5197-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b5197-113">-DatabaseName</span></span>
<span data-ttu-id="b5197-114">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="b5197-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="b5197-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5197-115">-DefaultProfile</span></span>
<span data-ttu-id="b5197-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5197-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5197-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5197-117">-ResourceGroupName</span></span>
<span data-ttu-id="b5197-118">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b5197-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b5197-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5197-119">-SubscriptionId</span></span>
<span data-ttu-id="b5197-120">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b5197-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b5197-121">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b5197-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b5197-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b5197-122">-Confirm</span></span>
<span data-ttu-id="b5197-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b5197-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5197-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5197-124">-WhatIf</span></span>
<span data-ttu-id="b5197-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b5197-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5197-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5197-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5197-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5197-127">CommonParameters</span></span>
<span data-ttu-id="b5197-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5197-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5197-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b5197-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5197-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5197-130">INPUTS</span></span>

## <span data-ttu-id="b5197-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5197-131">OUTPUTS</span></span>

### <span data-ttu-id="b5197-132">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="b5197-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="b5197-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5197-133">NOTES</span></span>

<span data-ttu-id="b5197-134">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b5197-134">ALIASES</span></span>

## <span data-ttu-id="b5197-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5197-135">RELATED LINKS</span></span>


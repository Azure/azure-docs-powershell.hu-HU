---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b5f94aeb66749fa9bc89a89febb0bc5597241d58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025958"
---
# <span data-ttu-id="5c90c-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="5c90c-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="5c90c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5c90c-102">SYNOPSIS</span></span>
<span data-ttu-id="5c90c-103">Egy adatbázisra vonatkozó árazási szintű tippeket kap.</span><span class="sxs-lookup"><span data-stu-id="5c90c-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="5c90c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5c90c-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c90c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5c90c-105">DESCRIPTION</span></span>
<span data-ttu-id="5c90c-106">A **Get-AzSqlDatabaseUpgradeHint** parancsmag árazási szintű tippeket ad az Azure SQL-adatbázisok frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="5c90c-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="5c90c-107">Az olyan adatbázisokban, amelyek továbbra is a webes és az üzleti árak szintjein találhatók, az új alapszintű, normál vagy prémium árazási szintekre frissíthetik a célzást.</span><span class="sxs-lookup"><span data-stu-id="5c90c-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="5c90c-108">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="5c90c-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5c90c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5c90c-109">EXAMPLES</span></span>

### <span data-ttu-id="5c90c-110">Példa 1: javaslatok kérése a kiszolgálón található összes adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="5c90c-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="5c90c-111">Ez a parancs a Server01 nevű kiszolgálón található összes adatbázisra vonatkozó frissítési tippeket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="5c90c-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="5c90c-112">2. példa: javaslatok kérése adott adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="5c90c-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="5c90c-113">Ez a parancs adott adatbázishoz tartozó frissítési tippeket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="5c90c-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="5c90c-114">3. példa: a rugalmas adatbázis-készletben nem szereplő összes adatbázisra vonatkozó ajánlás kérése</span><span class="sxs-lookup"><span data-stu-id="5c90c-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="5c90c-115">A parancs a rugalmas adatbázis-készletben nem szereplő összes adatbázisra vonatkozó frissítési tippeket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="5c90c-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="5c90c-116">Példa 4: javaslatok kérése a kiszolgálón található összes adatbázisra szűréssel</span><span class="sxs-lookup"><span data-stu-id="5c90c-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="5c90c-117">Ez a parancs az "adatbázis" kezdetű Server01 nevű kiszolgálón található összes adatbázisra vonatkozó frissítési tippeket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="5c90c-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="5c90c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5c90c-118">PARAMETERS</span></span>

### <span data-ttu-id="5c90c-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c90c-119">-DatabaseName</span></span>
<span data-ttu-id="5c90c-120">Annak az SQL-adatbázisnak a neve, amelyhez a parancsmag frissítési tippeket kap.</span><span class="sxs-lookup"><span data-stu-id="5c90c-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="5c90c-121">Ha nem ad meg adatbázist, ez a parancsmag tippeket ad a logikai kiszolgálón található összes adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="5c90c-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c90c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c90c-122">-DefaultProfile</span></span>
<span data-ttu-id="5c90c-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5c90c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c90c-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="5c90c-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="5c90c-125">Azt jelzi, hogy a rugalmas adatbázis-készletben lévő adatbázisok ki vannak-e zárva a visszaadott ajánlásokból.</span><span class="sxs-lookup"><span data-stu-id="5c90c-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c90c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c90c-126">-ResourceGroupName</span></span>
<span data-ttu-id="5c90c-127">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="5c90c-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5c90c-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5c90c-128">-ServerName</span></span>
<span data-ttu-id="5c90c-129">Itt adhatja meg annak az adatbázisnak a nevét, amelynek a parancsmagja a frissítési tippeket kapja.</span><span class="sxs-lookup"><span data-stu-id="5c90c-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="5c90c-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5c90c-130">-Confirm</span></span>
<span data-ttu-id="5c90c-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5c90c-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c90c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c90c-132">-WhatIf</span></span>
<span data-ttu-id="5c90c-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5c90c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c90c-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5c90c-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c90c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c90c-135">CommonParameters</span></span>
<span data-ttu-id="5c90c-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5c90c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c90c-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5c90c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c90c-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c90c-138">INPUTS</span></span>

### <span data-ttu-id="5c90c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5c90c-139">System.String</span></span>

### <span data-ttu-id="5c90c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c90c-140">System.Boolean</span></span>

## <span data-ttu-id="5c90c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c90c-141">OUTPUTS</span></span>

### <span data-ttu-id="5c90c-142">Microsoft. Azure. Management. SQL. LegacySdk. models. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="5c90c-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="5c90c-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5c90c-143">NOTES</span></span>

## <span data-ttu-id="5c90c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c90c-144">RELATED LINKS</span></span>

[<span data-ttu-id="5c90c-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="5c90c-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="5c90c-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="5c90c-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)



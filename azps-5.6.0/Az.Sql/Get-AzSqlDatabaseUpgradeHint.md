---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: 9018dab5f09bbab6a3fb1197ee8aabd09141e664
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014677"
---
# <span data-ttu-id="aed3b-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="aed3b-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="aed3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aed3b-102">SYNOPSIS</span></span>
<span data-ttu-id="aed3b-103">Az adatbázisokra vonatkozó árszint-tippeket kap.</span><span class="sxs-lookup"><span data-stu-id="aed3b-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="aed3b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aed3b-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aed3b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aed3b-105">DESCRIPTION</span></span>
<span data-ttu-id="aed3b-106">A **Get-AzSqlDatabaseUpgradeHint** parancsmag árazási szintmutatókat kap az Azure SQL-adatbázis frissítésében.</span><span class="sxs-lookup"><span data-stu-id="aed3b-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="aed3b-107">Azok az adatbázisok, amelyek továbbra is a webes és vállalati árazási szinteken maradnak, tippeket kap az új alapszintű, normál vagy prémiumszintű árszintre való frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="aed3b-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="aed3b-108">Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.</span><span class="sxs-lookup"><span data-stu-id="aed3b-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="aed3b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aed3b-109">EXAMPLES</span></span>

### <span data-ttu-id="aed3b-110">1. példa: Javaslatok a kiszolgáló összes adatbázisához</span><span class="sxs-lookup"><span data-stu-id="aed3b-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="aed3b-111">Ez a parancs frissítési tippeket ad vissza a Kiszolgáló01 nevű kiszolgálón található összes adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="aed3b-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="aed3b-112">2. példa: Javaslatok lekérte adott adatbázisra</span><span class="sxs-lookup"><span data-stu-id="aed3b-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="aed3b-113">Ez a parancs frissítési tippeket ad vissza egy adott adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="aed3b-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="aed3b-114">3. példa: Javaslat minden olyan adatbázishoz, amely nem rugalmas adatbáziskészletben található</span><span class="sxs-lookup"><span data-stu-id="aed3b-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="aed3b-115">Ez a parancs frissítési tippeket ad vissza minden olyan adatbázishoz, amely nem rugalmas adatbáziskészletben található.</span><span class="sxs-lookup"><span data-stu-id="aed3b-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="aed3b-116">4. példa: Javaslatok a kiszolgálón található összes adatbázishoz szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="aed3b-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="aed3b-117">Ez a parancs frissítési tippeket ad vissza a Kiszolgáló01 kiszolgáló összes olyan adatbázisához, amely az "Adatbázis" kezdetű.</span><span class="sxs-lookup"><span data-stu-id="aed3b-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="aed3b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aed3b-118">PARAMETERS</span></span>

### <span data-ttu-id="aed3b-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aed3b-119">-DatabaseName</span></span>
<span data-ttu-id="aed3b-120">Annak az SQL-adatbázisnak a neve, amelyhez ez a parancsmag frissítési tippet kap.</span><span class="sxs-lookup"><span data-stu-id="aed3b-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="aed3b-121">Ha nem ad meg adatbázist, ez a parancsmag tippeket kap a logikai kiszolgálón található összes adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="aed3b-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="aed3b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed3b-122">-DefaultProfile</span></span>
<span data-ttu-id="aed3b-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="aed3b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aed3b-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="aed3b-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="aed3b-125">Azt jelzi, hogy a rugalmas adatbáziskészletek adatbázisai ki vannak-e zárva a visszaadott javaslatokból.</span><span class="sxs-lookup"><span data-stu-id="aed3b-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="aed3b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aed3b-126">-ResourceGroupName</span></span>
<span data-ttu-id="aed3b-127">Annak az erőforráscsoportnak a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="aed3b-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="aed3b-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aed3b-128">-ServerName</span></span>
<span data-ttu-id="aed3b-129">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja frissítési tippet kap.</span><span class="sxs-lookup"><span data-stu-id="aed3b-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="aed3b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aed3b-130">-Confirm</span></span>
<span data-ttu-id="aed3b-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aed3b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aed3b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aed3b-132">-WhatIf</span></span>
<span data-ttu-id="aed3b-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aed3b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aed3b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aed3b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aed3b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed3b-135">CommonParameters</span></span>
<span data-ttu-id="aed3b-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aed3b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed3b-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aed3b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed3b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aed3b-138">INPUTS</span></span>

### <span data-ttu-id="aed3b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="aed3b-139">System.String</span></span>

### <span data-ttu-id="aed3b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aed3b-140">System.Boolean</span></span>

## <span data-ttu-id="aed3b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aed3b-141">OUTPUTS</span></span>

### <span data-ttu-id="aed3b-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="aed3b-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="aed3b-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aed3b-143">NOTES</span></span>

## <span data-ttu-id="aed3b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aed3b-144">RELATED LINKS</span></span>

[<span data-ttu-id="aed3b-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="aed3b-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="aed3b-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="aed3b-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)



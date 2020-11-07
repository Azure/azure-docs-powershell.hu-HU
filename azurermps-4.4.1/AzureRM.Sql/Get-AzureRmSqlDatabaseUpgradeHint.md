---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
ms.openlocfilehash: c0a917d2f5e10bb499ecf6fc698bee9a84d64363
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679322"
---
# <span data-ttu-id="790da-101">Get-AzureRmSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="790da-101">Get-AzureRmSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="790da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="790da-102">SYNOPSIS</span></span>
<span data-ttu-id="790da-103">Egy adatbázisra vonatkozó árazási szintű tippeket kap.</span><span class="sxs-lookup"><span data-stu-id="790da-103">Gets pricing tier hints for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="790da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="790da-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="790da-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="790da-105">DESCRIPTION</span></span>
<span data-ttu-id="790da-106">A **Get-AzureRmSqlDatabaseUpgradeHint** parancsmag árazási szintű tippeket ad az Azure SQL-adatbázisok frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="790da-106">The **Get-AzureRmSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="790da-107">Az olyan adatbázisokban, amelyek továbbra is a webes és az üzleti árak szintjein találhatók, az új alapszintű, normál vagy prémium árazási szintekre frissíthetik a célzást.</span><span class="sxs-lookup"><span data-stu-id="790da-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>

<span data-ttu-id="790da-108">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="790da-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="790da-109">Példák</span><span class="sxs-lookup"><span data-stu-id="790da-109">EXAMPLES</span></span>

### <span data-ttu-id="790da-110">Példa 1: javaslatok kérése a kiszolgálón található összes adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="790da-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="790da-111">Ez a parancs a Server01 nevű kiszolgálón található összes adatbázisra vonatkozó frissítési tippeket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="790da-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="790da-112">2. példa: javaslatok kérése adott adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="790da-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="790da-113">Ez a parancs adott adatbázishoz tartozó frissítési tippeket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="790da-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="790da-114">3. példa: a rugalmas adatbázis-készletben nem szereplő összes adatbázisra vonatkozó ajánlás kérése</span><span class="sxs-lookup"><span data-stu-id="790da-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="790da-115">A parancs a rugalmas adatbázis-készletben nem szereplő összes adatbázisra vonatkozó frissítési tippeket ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="790da-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

## <span data-ttu-id="790da-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="790da-116">PARAMETERS</span></span>

### <span data-ttu-id="790da-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="790da-117">-DatabaseName</span></span>
<span data-ttu-id="790da-118">Annak az SQL-adatbázisnak a neve, amelyhez a parancsmag frissítési tippeket kap.</span><span class="sxs-lookup"><span data-stu-id="790da-118">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="790da-119">Ha nem ad meg adatbázist, ez a parancsmag tippeket ad a logikai kiszolgálón található összes adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="790da-119">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="790da-120">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="790da-120">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="790da-121">Azt jelzi, hogy a rugalmas adatbázis-készletben lévő adatbázisok ki vannak-e zárva a visszaadott ajánlásokból.</span><span class="sxs-lookup"><span data-stu-id="790da-121">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="790da-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="790da-122">-ResourceGroupName</span></span>
<span data-ttu-id="790da-123">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="790da-123">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="790da-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="790da-124">-ServerName</span></span>
<span data-ttu-id="790da-125">Itt adhatja meg annak az adatbázisnak a nevét, amelynek a parancsmagja a frissítési tippeket kapja.</span><span class="sxs-lookup"><span data-stu-id="790da-125">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="790da-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="790da-126">-Confirm</span></span>
<span data-ttu-id="790da-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="790da-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="790da-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="790da-128">-WhatIf</span></span>
<span data-ttu-id="790da-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="790da-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="790da-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="790da-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="790da-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="790da-131">-DefaultProfile</span></span>
<span data-ttu-id="790da-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="790da-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="790da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="790da-133">CommonParameters</span></span>
<span data-ttu-id="790da-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="790da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="790da-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="790da-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="790da-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="790da-136">INPUTS</span></span>

## <span data-ttu-id="790da-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="790da-137">OUTPUTS</span></span>

## <span data-ttu-id="790da-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="790da-138">NOTES</span></span>

## <span data-ttu-id="790da-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="790da-139">RELATED LINKS</span></span>

[<span data-ttu-id="790da-140">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="790da-140">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="790da-141">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="790da-141">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)



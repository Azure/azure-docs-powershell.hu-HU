---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
ms.openlocfilehash: 8516cbecac3cb4c741bb7aea1e93c10f25222b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502336"
---
# <span data-ttu-id="38950-101">Get-AzureRmSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="38950-101">Get-AzureRmSqlServerUpgradeHint</span></span>

## <span data-ttu-id="38950-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38950-102">SYNOPSIS</span></span>
<span data-ttu-id="38950-103">Egy Azure SQL-adatbázis kiszolgálójának frissítésére vonatkozó árazási szint tippeket kap.</span><span class="sxs-lookup"><span data-stu-id="38950-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38950-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38950-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38950-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="38950-105">DESCRIPTION</span></span>
<span data-ttu-id="38950-106">A **Get-AzureRmSqlServerUpgradeHint** parancsmag árazási szintű tippeket ad az Azure SQL-adatbázis kiszolgálójának frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="38950-106">The **Get-AzureRmSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="38950-107">A tippek tartalmazhatják az adatbázis rugalmas készletét és az önálló adatbázis-tippeket.</span><span class="sxs-lookup"><span data-stu-id="38950-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="38950-108">Az olyan adatbázisokban, amelyek továbbra is a webes és az üzleti árak szintjein találhatók, tippeket kaphat az új alapszintű, normál vagy prémium árazási szintekre való áttérésre, illetve a rugalmas adatbázis-készletre.</span><span class="sxs-lookup"><span data-stu-id="38950-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="38950-109">Ez a parancsmag a megadott kiszolgálón tárolt összes adatbázisra vonatkozó tippeket ad.</span><span class="sxs-lookup"><span data-stu-id="38950-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="38950-110">Példák</span><span class="sxs-lookup"><span data-stu-id="38950-110">EXAMPLES</span></span>

### <span data-ttu-id="38950-111">Példa 1: egyesített javaslatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="38950-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="38950-112">Ez a parancs a Server01 nevű kiszolgálón található összes adatbázisra vonatkozóan egyesített javaslatokat kap.</span><span class="sxs-lookup"><span data-stu-id="38950-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="38950-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38950-113">PARAMETERS</span></span>

### <span data-ttu-id="38950-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38950-114">-DefaultProfile</span></span>
<span data-ttu-id="38950-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="38950-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38950-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="38950-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="38950-117">Azt jelzi, hogy a rugalmas adatbázis-gyűjtőben megtalálható adatbázisokat kell-e visszaadni.</span><span class="sxs-lookup"><span data-stu-id="38950-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38950-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38950-118">-ResourceGroupName</span></span>
<span data-ttu-id="38950-119">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="38950-119">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38950-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="38950-120">-ServerName</span></span>
<span data-ttu-id="38950-121">Annak a kiszolgálónak a nevét adja meg, amelynek a parancsmagja a frissítési tippeket kapja.</span><span class="sxs-lookup"><span data-stu-id="38950-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38950-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="38950-122">-Confirm</span></span>
<span data-ttu-id="38950-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="38950-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38950-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38950-124">-WhatIf</span></span>
<span data-ttu-id="38950-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="38950-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38950-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38950-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38950-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38950-127">CommonParameters</span></span>
<span data-ttu-id="38950-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38950-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38950-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38950-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38950-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38950-130">INPUTS</span></span>

### <span data-ttu-id="38950-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="38950-131">None</span></span>
<span data-ttu-id="38950-132">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="38950-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38950-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38950-133">OUTPUTS</span></span>

## <span data-ttu-id="38950-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38950-134">NOTES</span></span>

## <span data-ttu-id="38950-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38950-135">RELATED LINKS</span></span>

[<span data-ttu-id="38950-136">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="38950-136">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="38950-137">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="38950-137">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)

[<span data-ttu-id="38950-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="38950-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



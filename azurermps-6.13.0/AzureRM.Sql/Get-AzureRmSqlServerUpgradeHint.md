---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
ms.openlocfilehash: 597156e101a9d16eff36d05fae71b32e0033ad6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495603"
---
# <span data-ttu-id="2ad06-101">Get-AzureRmSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="2ad06-101">Get-AzureRmSqlServerUpgradeHint</span></span>

## <span data-ttu-id="2ad06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ad06-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad06-103">Egy Azure SQL-adatbázis kiszolgálójának frissítésére vonatkozó árazási szint tippeket kap.</span><span class="sxs-lookup"><span data-stu-id="2ad06-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ad06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ad06-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ad06-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ad06-105">DESCRIPTION</span></span>
<span data-ttu-id="2ad06-106">A **Get-AzureRmSqlServerUpgradeHint** parancsmag árazási szintű tippeket ad az Azure SQL-adatbázis kiszolgálójának frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="2ad06-106">The **Get-AzureRmSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="2ad06-107">A tippek tartalmazhatják az adatbázis rugalmas készletét és az önálló adatbázis-tippeket.</span><span class="sxs-lookup"><span data-stu-id="2ad06-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="2ad06-108">Az olyan adatbázisokban, amelyek továbbra is a webes és az üzleti árak szintjein találhatók, tippeket kaphat az új alapszintű, normál vagy prémium árazási szintekre való áttérésre, illetve a rugalmas adatbázis-készletre.</span><span class="sxs-lookup"><span data-stu-id="2ad06-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="2ad06-109">Ez a parancsmag a megadott kiszolgálón tárolt összes adatbázisra vonatkozó tippeket ad.</span><span class="sxs-lookup"><span data-stu-id="2ad06-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="2ad06-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2ad06-110">EXAMPLES</span></span>

### <span data-ttu-id="2ad06-111">Példa 1: egyesített javaslatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="2ad06-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="2ad06-112">Ez a parancs a Server01 nevű kiszolgálón található összes adatbázisra vonatkozóan egyesített javaslatokat kap.</span><span class="sxs-lookup"><span data-stu-id="2ad06-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="2ad06-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ad06-113">PARAMETERS</span></span>

### <span data-ttu-id="2ad06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad06-114">-DefaultProfile</span></span>
<span data-ttu-id="2ad06-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2ad06-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ad06-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="2ad06-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="2ad06-117">Azt jelzi, hogy a rugalmas adatbázis-gyűjtőben megtalálható adatbázisokat kell-e visszaadni.</span><span class="sxs-lookup"><span data-stu-id="2ad06-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="2ad06-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad06-118">-ResourceGroupName</span></span>
<span data-ttu-id="2ad06-119">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="2ad06-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="2ad06-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2ad06-120">-ServerName</span></span>
<span data-ttu-id="2ad06-121">Annak a kiszolgálónak a nevét adja meg, amelynek a parancsmagja a frissítési tippeket kapja.</span><span class="sxs-lookup"><span data-stu-id="2ad06-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="2ad06-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2ad06-122">-Confirm</span></span>
<span data-ttu-id="2ad06-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ad06-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ad06-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ad06-124">-WhatIf</span></span>
<span data-ttu-id="2ad06-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2ad06-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ad06-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ad06-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ad06-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad06-127">CommonParameters</span></span>
<span data-ttu-id="2ad06-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ad06-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad06-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ad06-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad06-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ad06-130">INPUTS</span></span>

### <span data-ttu-id="2ad06-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2ad06-131">System.String</span></span>

### <span data-ttu-id="2ad06-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ad06-132">System.Boolean</span></span>

## <span data-ttu-id="2ad06-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ad06-133">OUTPUTS</span></span>

### <span data-ttu-id="2ad06-134">Microsoft. Azure. Command. SQL. ServiceTierAdvisor. Model. UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="2ad06-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="2ad06-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ad06-135">NOTES</span></span>

## <span data-ttu-id="2ad06-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ad06-136">RELATED LINKS</span></span>

[<span data-ttu-id="2ad06-137">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="2ad06-137">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="2ad06-138">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="2ad06-138">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)

[<span data-ttu-id="2ad06-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="2ad06-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



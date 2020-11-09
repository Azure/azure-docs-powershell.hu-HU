---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: 841de793c6e0c6d9213be262576dbd4f407fd947
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300491"
---
# <span data-ttu-id="dff48-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="dff48-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="dff48-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dff48-102">SYNOPSIS</span></span>
<span data-ttu-id="dff48-103">Egy Azure SQL-adatbázis kiszolgálójának frissítésére vonatkozó árazási szint tippeket kap.</span><span class="sxs-lookup"><span data-stu-id="dff48-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="dff48-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dff48-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dff48-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dff48-105">DESCRIPTION</span></span>
<span data-ttu-id="dff48-106">A **Get-AzSqlServerUpgradeHint** parancsmag árazási szintű tippeket ad az Azure SQL-adatbázis kiszolgálójának frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="dff48-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="dff48-107">A tippek tartalmazhatják az adatbázis rugalmas készletét és az önálló adatbázis-tippeket.</span><span class="sxs-lookup"><span data-stu-id="dff48-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="dff48-108">Az olyan adatbázisokban, amelyek továbbra is a webes és az üzleti árak szintjein találhatók, tippeket kaphat az új alapszintű, normál vagy prémium árazási szintekre való áttérésre, illetve a rugalmas adatbázis-készletre.</span><span class="sxs-lookup"><span data-stu-id="dff48-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="dff48-109">Ez a parancsmag a megadott kiszolgálón tárolt összes adatbázisra vonatkozó tippeket ad.</span><span class="sxs-lookup"><span data-stu-id="dff48-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="dff48-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dff48-110">EXAMPLES</span></span>

### <span data-ttu-id="dff48-111">Példa 1: egyesített javaslatok beszerzése</span><span class="sxs-lookup"><span data-stu-id="dff48-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="dff48-112">Ez a parancs a Server01 nevű kiszolgálón található összes adatbázisra vonatkozóan egyesített javaslatokat kap.</span><span class="sxs-lookup"><span data-stu-id="dff48-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="dff48-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dff48-113">PARAMETERS</span></span>

### <span data-ttu-id="dff48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dff48-114">-DefaultProfile</span></span>
<span data-ttu-id="dff48-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dff48-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dff48-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="dff48-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="dff48-117">Azt jelzi, hogy a rugalmas adatbázis-gyűjtőben megtalálható adatbázisokat kell-e visszaadni.</span><span class="sxs-lookup"><span data-stu-id="dff48-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="dff48-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dff48-118">-ResourceGroupName</span></span>
<span data-ttu-id="dff48-119">Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgálót hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="dff48-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="dff48-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="dff48-120">-ServerName</span></span>
<span data-ttu-id="dff48-121">Annak a kiszolgálónak a nevét adja meg, amelynek a parancsmagja a frissítési tippeket kapja.</span><span class="sxs-lookup"><span data-stu-id="dff48-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="dff48-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dff48-122">-Confirm</span></span>
<span data-ttu-id="dff48-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dff48-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dff48-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dff48-124">-WhatIf</span></span>
<span data-ttu-id="dff48-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dff48-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dff48-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dff48-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dff48-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff48-127">CommonParameters</span></span>
<span data-ttu-id="dff48-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dff48-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff48-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dff48-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff48-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dff48-130">INPUTS</span></span>

### <span data-ttu-id="dff48-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dff48-131">System.String</span></span>

### <span data-ttu-id="dff48-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dff48-132">System.Boolean</span></span>

## <span data-ttu-id="dff48-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dff48-133">OUTPUTS</span></span>

### <span data-ttu-id="dff48-134">Microsoft. Azure. Command. SQL. ServiceTierAdvisor. Model. UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="dff48-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="dff48-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dff48-135">NOTES</span></span>

## <span data-ttu-id="dff48-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dff48-136">RELATED LINKS</span></span>

[<span data-ttu-id="dff48-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="dff48-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="dff48-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="dff48-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="dff48-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="dff48-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



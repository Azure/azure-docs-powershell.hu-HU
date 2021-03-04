---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: fc75aa4f838d19044514d3e6c343e04cdbf1d9be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920265"
---
# <span data-ttu-id="7146f-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="7146f-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="7146f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7146f-102">SYNOPSIS</span></span>
<span data-ttu-id="7146f-103">Az Azure SQL-adatbázis-kiszolgáló frissítéséhez árszint-tippeket ad.</span><span class="sxs-lookup"><span data-stu-id="7146f-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="7146f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7146f-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7146f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7146f-105">DESCRIPTION</span></span>
<span data-ttu-id="7146f-106">A **Get-AzSqlServerUpgradeHint parancsmag** árazási szintmutatókat kap az Azure SQL Database-kiszolgáló frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="7146f-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="7146f-107">A tippek tartalmazzák a rugalmas adatbáziskészletet és a különálló adatbázis-tippeket.</span><span class="sxs-lookup"><span data-stu-id="7146f-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="7146f-108">Azok az adatbázisok, amelyek továbbra is a webes és vállalati árazási szinteken maradnak, tippeket kap az új alapszintű, normál vagy prémiumszintű árszintre való frissítéshez, illetve a rugalmas adatbáziskészlethez való ugráshoz.</span><span class="sxs-lookup"><span data-stu-id="7146f-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="7146f-109">Ez a parancsmag tippeket ad vissza a megadott kiszolgálón üzemeltetett összes adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="7146f-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="7146f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7146f-110">EXAMPLES</span></span>

### <span data-ttu-id="7146f-111">1. példa: Kombinált javaslatok</span><span class="sxs-lookup"><span data-stu-id="7146f-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="7146f-112">Ez a parancs kombinált javaslatokat kap a Server01 nevű kiszolgálón található összes adatbázisra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="7146f-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="7146f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7146f-113">PARAMETERS</span></span>

### <span data-ttu-id="7146f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7146f-114">-DefaultProfile</span></span>
<span data-ttu-id="7146f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7146f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7146f-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="7146f-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="7146f-117">Azt jelzi, hogy a rugalmas adatbáziskészletekbe foglalt adatbázisokat kell-e visszaadni.</span><span class="sxs-lookup"><span data-stu-id="7146f-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="7146f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7146f-118">-ResourceGroupName</span></span>
<span data-ttu-id="7146f-119">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="7146f-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7146f-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7146f-120">-ServerName</span></span>
<span data-ttu-id="7146f-121">Megadja annak a kiszolgálónak a nevét, amelyhez a parancsmag frissítési tippet kap.</span><span class="sxs-lookup"><span data-stu-id="7146f-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="7146f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7146f-122">-Confirm</span></span>
<span data-ttu-id="7146f-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7146f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7146f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7146f-124">-WhatIf</span></span>
<span data-ttu-id="7146f-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7146f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7146f-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7146f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7146f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7146f-127">CommonParameters</span></span>
<span data-ttu-id="7146f-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7146f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7146f-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7146f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7146f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7146f-130">INPUTS</span></span>

### <span data-ttu-id="7146f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7146f-131">System.String</span></span>

### <span data-ttu-id="7146f-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7146f-132">System.Boolean</span></span>

## <span data-ttu-id="7146f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7146f-133">OUTPUTS</span></span>

### <span data-ttu-id="7146f-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="7146f-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="7146f-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7146f-135">NOTES</span></span>

## <span data-ttu-id="7146f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7146f-136">RELATED LINKS</span></span>

[<span data-ttu-id="7146f-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="7146f-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="7146f-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="7146f-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="7146f-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="7146f-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



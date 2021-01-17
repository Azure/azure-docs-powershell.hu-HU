---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: 841de793c6e0c6d9213be262576dbd4f407fd947
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469969"
---
# <span data-ttu-id="9713c-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="9713c-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="9713c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9713c-102">SYNOPSIS</span></span>
<span data-ttu-id="9713c-103">Az Azure SQL-adatbázis-kiszolgáló frissítéséhez árszint-tippeket ad.</span><span class="sxs-lookup"><span data-stu-id="9713c-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="9713c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9713c-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9713c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9713c-105">DESCRIPTION</span></span>
<span data-ttu-id="9713c-106">A **Get-AzSqlServerUpgradeHint parancsmag** árazási szintmutatókat kap az Azure SQL Database-kiszolgáló frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="9713c-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="9713c-107">A tippek tartalmazzák a rugalmas adatbáziskészletet és a különálló adatbázis-tippeket.</span><span class="sxs-lookup"><span data-stu-id="9713c-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="9713c-108">Azok az adatbázisok, amelyek továbbra is a webes és vállalati árazási szinteken maradnak, tippeket kap az új alapszintű, normál vagy prémiumszintű árszintre való frissítéshez, illetve a rugalmas adatbáziskészlethez való ugráshoz.</span><span class="sxs-lookup"><span data-stu-id="9713c-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="9713c-109">Ez a parancsmag tippeket ad a megadott kiszolgálón üzemeltetett összes adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="9713c-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="9713c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9713c-110">EXAMPLES</span></span>

### <span data-ttu-id="9713c-111">1. példa: Kombinált javaslatok</span><span class="sxs-lookup"><span data-stu-id="9713c-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="9713c-112">Ez a parancs kombinált javaslatokat kap a Server01 nevű kiszolgálón található összes adatbázisra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="9713c-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="9713c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9713c-113">PARAMETERS</span></span>

### <span data-ttu-id="9713c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9713c-114">-DefaultProfile</span></span>
<span data-ttu-id="9713c-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9713c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9713c-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="9713c-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="9713c-117">Azt jelzi, hogy a rugalmas adatbáziskészletekbe foglalt adatbázisokat kell-e eredményül visszaadni.</span><span class="sxs-lookup"><span data-stu-id="9713c-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="9713c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9713c-118">-ResourceGroupName</span></span>
<span data-ttu-id="9713c-119">Annak az erőforráscsoportnak a neve, amelyhez a kiszolgáló hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="9713c-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9713c-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9713c-120">-ServerName</span></span>
<span data-ttu-id="9713c-121">Megadja annak a kiszolgálónak a nevét, amelyhez a parancsmag frissítési tippet kap.</span><span class="sxs-lookup"><span data-stu-id="9713c-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="9713c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9713c-122">-Confirm</span></span>
<span data-ttu-id="9713c-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9713c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9713c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9713c-124">-WhatIf</span></span>
<span data-ttu-id="9713c-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9713c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9713c-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9713c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9713c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9713c-127">CommonParameters</span></span>
<span data-ttu-id="9713c-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9713c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9713c-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9713c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9713c-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9713c-130">INPUTS</span></span>

### <span data-ttu-id="9713c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9713c-131">System.String</span></span>

### <span data-ttu-id="9713c-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9713c-132">System.Boolean</span></span>

## <span data-ttu-id="9713c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9713c-133">OUTPUTS</span></span>

### <span data-ttu-id="9713c-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="9713c-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="9713c-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9713c-135">NOTES</span></span>

## <span data-ttu-id="9713c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9713c-136">RELATED LINKS</span></span>

[<span data-ttu-id="9713c-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="9713c-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="9713c-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="9713c-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="9713c-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="9713c-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



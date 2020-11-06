---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: a9f86b9b316c14e40505932e0bf3b30fc66c55c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501019"
---
# <span data-ttu-id="b40e5-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="b40e5-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="b40e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b40e5-102">SYNOPSIS</span></span>
<span data-ttu-id="b40e5-103">Elasztikus adatbázisokat kap egy rugalmas készletben és a hozzájuk tartozó tulajdonsági értékeken.</span><span class="sxs-lookup"><span data-stu-id="b40e5-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b40e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b40e5-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b40e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b40e5-105">DESCRIPTION</span></span>
<span data-ttu-id="b40e5-106">A **Get-AzureRmSqlElasticPoolDatabase** parancsmag rugalmasan változó adatbázisokat és a hozzájuk tartozó tulajdonságértékeket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b40e5-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="b40e5-107">Az Azure SQL-adatbázisban megadhatja a rugalmas adatbázis nevét úgy, hogy csak az adott adatbázishoz tartozó tulajdonságértékeket láthassa.</span><span class="sxs-lookup"><span data-stu-id="b40e5-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="b40e5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b40e5-108">EXAMPLES</span></span>

### <span data-ttu-id="b40e5-109">Példa 1: az összes adatbázis beszerzése rugalmas készletbe</span><span class="sxs-lookup"><span data-stu-id="b40e5-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="b40e5-110">Ez a parancs a ElasticPool01 nevű rugalmas készlet minden adatbázisát bekapja.</span><span class="sxs-lookup"><span data-stu-id="b40e5-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="b40e5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b40e5-111">PARAMETERS</span></span>

### <span data-ttu-id="b40e5-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b40e5-112">-DatabaseName</span></span>
<span data-ttu-id="b40e5-113">Annak az SQL-adatbázisnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="b40e5-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b40e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b40e5-114">-DefaultProfile</span></span>
<span data-ttu-id="b40e5-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b40e5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b40e5-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b40e5-116">-ElasticPoolName</span></span>
<span data-ttu-id="b40e5-117">Egy rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b40e5-117">Specifies the name of an elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b40e5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b40e5-118">-ResourceGroupName</span></span>
<span data-ttu-id="b40e5-119">Annak a csoportnak a neve, amelyhez a rugalmas készlet van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b40e5-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="b40e5-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b40e5-120">-ServerName</span></span>
<span data-ttu-id="b40e5-121">Egy rugalmas készletet tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b40e5-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="b40e5-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b40e5-122">-Confirm</span></span>
<span data-ttu-id="b40e5-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b40e5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b40e5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b40e5-124">-WhatIf</span></span>
<span data-ttu-id="b40e5-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b40e5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b40e5-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b40e5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b40e5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b40e5-127">CommonParameters</span></span>
<span data-ttu-id="b40e5-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b40e5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b40e5-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b40e5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b40e5-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b40e5-130">INPUTS</span></span>

### <span data-ttu-id="b40e5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b40e5-131">System.String</span></span>

## <span data-ttu-id="b40e5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b40e5-132">OUTPUTS</span></span>

### <span data-ttu-id="b40e5-133">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b40e5-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b40e5-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b40e5-134">NOTES</span></span>

## <span data-ttu-id="b40e5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b40e5-135">RELATED LINKS</span></span>

[<span data-ttu-id="b40e5-136">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b40e5-136">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="b40e5-137">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="b40e5-137">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="b40e5-138">Új – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b40e5-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="b40e5-139">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b40e5-139">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="b40e5-140">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b40e5-140">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


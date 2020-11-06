---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: f2229fa904144b0dd95a054da95db99600963406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494619"
---
# <span data-ttu-id="299a3-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="299a3-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="299a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="299a3-102">SYNOPSIS</span></span>
<span data-ttu-id="299a3-103">Elasztikus adatbázisokat kap egy rugalmas készletben és a hozzájuk tartozó tulajdonsági értékeken.</span><span class="sxs-lookup"><span data-stu-id="299a3-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="299a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="299a3-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="299a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="299a3-105">DESCRIPTION</span></span>
<span data-ttu-id="299a3-106">A **Get-AzureRmSqlElasticPoolDatabase** parancsmag rugalmasan változó adatbázisokat és a hozzájuk tartozó tulajdonságértékeket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="299a3-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="299a3-107">Az Azure SQL-adatbázisban megadhatja a rugalmas adatbázis nevét úgy, hogy csak az adott adatbázishoz tartozó tulajdonságértékeket láthassa.</span><span class="sxs-lookup"><span data-stu-id="299a3-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="299a3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="299a3-108">EXAMPLES</span></span>

### <span data-ttu-id="299a3-109">Példa 1: az összes adatbázis beszerzése rugalmas készletbe</span><span class="sxs-lookup"><span data-stu-id="299a3-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="299a3-110">Ez a parancs a ElasticPool01 nevű rugalmas készlet minden adatbázisát bekapja.</span><span class="sxs-lookup"><span data-stu-id="299a3-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="299a3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="299a3-111">PARAMETERS</span></span>

### <span data-ttu-id="299a3-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="299a3-112">-DatabaseName</span></span>
<span data-ttu-id="299a3-113">Annak az SQL-adatbázisnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="299a3-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="299a3-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="299a3-114">-ElasticPoolName</span></span>
<span data-ttu-id="299a3-115">Egy rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="299a3-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="299a3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="299a3-116">-ResourceGroupName</span></span>
<span data-ttu-id="299a3-117">Annak a csoportnak a neve, amelyhez a rugalmas készlet van rendelve.</span><span class="sxs-lookup"><span data-stu-id="299a3-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="299a3-118">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="299a3-118">-ServerName</span></span>
<span data-ttu-id="299a3-119">Egy rugalmas készletet tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="299a3-119">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="299a3-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="299a3-120">-Confirm</span></span>
<span data-ttu-id="299a3-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="299a3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="299a3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="299a3-122">-WhatIf</span></span>
<span data-ttu-id="299a3-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="299a3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="299a3-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="299a3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="299a3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299a3-125">-DefaultProfile</span></span>
<span data-ttu-id="299a3-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="299a3-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="299a3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299a3-127">CommonParameters</span></span>
<span data-ttu-id="299a3-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="299a3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299a3-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="299a3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299a3-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="299a3-130">INPUTS</span></span>

## <span data-ttu-id="299a3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="299a3-131">OUTPUTS</span></span>

### <span data-ttu-id="299a3-132">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="299a3-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="299a3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="299a3-133">NOTES</span></span>

## <span data-ttu-id="299a3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="299a3-134">RELATED LINKS</span></span>

[<span data-ttu-id="299a3-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="299a3-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="299a3-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="299a3-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="299a3-137">Új – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="299a3-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="299a3-138">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="299a3-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="299a3-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="299a3-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


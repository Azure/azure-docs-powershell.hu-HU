---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: b37ae31c1f0dc6360743a863f0305fd5823cbb3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503927"
---
# <span data-ttu-id="f5177-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="f5177-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="f5177-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5177-102">SYNOPSIS</span></span>
<span data-ttu-id="f5177-103">A rugalmas adatbázisok áthelyezésének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f5177-103">Gets the status of moving elastic databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5177-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5177-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> -ElasticPoolName <String> -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5177-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5177-105">DESCRIPTION</span></span>
<span data-ttu-id="f5177-106">A **Get-AzureRmSqlDatabaseActivity** parancsmag olyan rugalmas adatbázisok állapotát kapja meg, amelyek az Azure SQL-adatbázisban egy rugalmas adatbázis-készletbe kerülnek.</span><span class="sxs-lookup"><span data-stu-id="f5177-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of elastic databases moving into or out of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="f5177-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f5177-107">EXAMPLES</span></span>

### <span data-ttu-id="f5177-108">Példa 1: az összes SQL-adatbázis-példány állapotának beolvasása</span><span class="sxs-lookup"><span data-stu-id="f5177-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="f5177-109">Ez a parancs a ElasticPool01 nevű rugalmas készletben minden SQL adatbázis-példány műveleti állapotát visszaadja.</span><span class="sxs-lookup"><span data-stu-id="f5177-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="f5177-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5177-110">PARAMETERS</span></span>

### <span data-ttu-id="f5177-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f5177-111">-DatabaseName</span></span>
<span data-ttu-id="f5177-112">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja az állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="f5177-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5177-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f5177-113">-ElasticPoolName</span></span>
<span data-ttu-id="f5177-114">Annak a rugalmas adatbázis-készletnek a nevét adja meg, amelynek a parancsmagja az állapotot kapja.</span><span class="sxs-lookup"><span data-stu-id="f5177-114">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5177-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f5177-115">-OperationId</span></span>
<span data-ttu-id="f5177-116">Annak a műveletnek az AZONOSÍTÓját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="f5177-116">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5177-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5177-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5177-118">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="f5177-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f5177-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f5177-119">-ServerName</span></span>
<span data-ttu-id="f5177-120">A rugalmas adatbázis-készletet tároló Microsoft SQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5177-120">Specifies the name of the Microsoft SQL Server that hosts the elastic database pool.</span></span>

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

### <span data-ttu-id="f5177-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5177-121">-Confirm</span></span>
<span data-ttu-id="f5177-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5177-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5177-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5177-123">-WhatIf</span></span>
<span data-ttu-id="f5177-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5177-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5177-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5177-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5177-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5177-126">-DefaultProfile</span></span>
<span data-ttu-id="f5177-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5177-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5177-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5177-128">CommonParameters</span></span>
<span data-ttu-id="f5177-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5177-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5177-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5177-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5177-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5177-131">INPUTS</span></span>

## <span data-ttu-id="f5177-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5177-132">OUTPUTS</span></span>

### <span data-ttu-id="f5177-133">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="f5177-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="f5177-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5177-134">NOTES</span></span>

## <span data-ttu-id="f5177-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5177-135">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: a6b5b21b8911aa8d156ced40476d1b0ecadad361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494306"
---
# <span data-ttu-id="f031e-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f031e-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="f031e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f031e-102">SYNOPSIS</span></span>
<span data-ttu-id="f031e-103">Egy rugalmas adatbázis-készlet törlése</span><span class="sxs-lookup"><span data-stu-id="f031e-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f031e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f031e-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f031e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f031e-105">DESCRIPTION</span></span>
<span data-ttu-id="f031e-106">A **Remove-AzureRmSqlElasticPool** parancsmag egy Azure SQL-adatbázis rugalmas készletének törlése.</span><span class="sxs-lookup"><span data-stu-id="f031e-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="f031e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f031e-107">EXAMPLES</span></span>

### <span data-ttu-id="f031e-108">Példa 1: elasztikus Pool törlése</span><span class="sxs-lookup"><span data-stu-id="f031e-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="f031e-109">Ez a parancs törli a ElasticPool01 nevű elasztikus medencét.</span><span class="sxs-lookup"><span data-stu-id="f031e-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="f031e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f031e-110">PARAMETERS</span></span>

### <span data-ttu-id="f031e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f031e-111">-DefaultProfile</span></span>
<span data-ttu-id="f031e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f031e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f031e-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f031e-113">-ElasticPoolName</span></span>
<span data-ttu-id="f031e-114">Annak a rugalmas készletnek a nevét adja meg, amelyre a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="f031e-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f031e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f031e-115">-Force</span></span>
<span data-ttu-id="f031e-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f031e-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f031e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f031e-117">-ResourceGroupName</span></span>
<span data-ttu-id="f031e-118">Annak az erőforráscsoport a neve, amelyhez a rugalmas készlet van rendelve.</span><span class="sxs-lookup"><span data-stu-id="f031e-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="f031e-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f031e-119">-ServerName</span></span>
<span data-ttu-id="f031e-120">A rugalmas készletet tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f031e-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="f031e-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f031e-121">-Confirm</span></span>
<span data-ttu-id="f031e-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f031e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f031e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f031e-123">-WhatIf</span></span>
<span data-ttu-id="f031e-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f031e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f031e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f031e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f031e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f031e-126">CommonParameters</span></span>
<span data-ttu-id="f031e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f031e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f031e-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f031e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f031e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f031e-129">INPUTS</span></span>

### <span data-ttu-id="f031e-130">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="f031e-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="f031e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f031e-131">OUTPUTS</span></span>

### <span data-ttu-id="f031e-132">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="f031e-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="f031e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f031e-133">NOTES</span></span>

## <span data-ttu-id="f031e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f031e-134">RELATED LINKS</span></span>

[<span data-ttu-id="f031e-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f031e-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f031e-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="f031e-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="f031e-137">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="f031e-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="f031e-138">Új – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f031e-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f031e-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f031e-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="f031e-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f031e-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



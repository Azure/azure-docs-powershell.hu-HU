---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: b58ec1f76737f34664bdecef38f2b596be3702d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668845"
---
# <span data-ttu-id="f397c-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f397c-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="f397c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f397c-102">SYNOPSIS</span></span>
<span data-ttu-id="f397c-103">Egy rugalmas adatbázis-készlet törlése</span><span class="sxs-lookup"><span data-stu-id="f397c-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="f397c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f397c-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f397c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f397c-105">DESCRIPTION</span></span>
<span data-ttu-id="f397c-106">A **Remove-AzSqlElasticPool** parancsmag egy Azure SQL-adatbázis rugalmas készletének törlése.</span><span class="sxs-lookup"><span data-stu-id="f397c-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="f397c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f397c-107">EXAMPLES</span></span>

### <span data-ttu-id="f397c-108">Példa 1: elasztikus Pool törlése</span><span class="sxs-lookup"><span data-stu-id="f397c-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="f397c-109">Ez a parancs törli a ElasticPool01 nevű elasztikus medencét.</span><span class="sxs-lookup"><span data-stu-id="f397c-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="f397c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f397c-110">PARAMETERS</span></span>

### <span data-ttu-id="f397c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f397c-111">-DefaultProfile</span></span>
<span data-ttu-id="f397c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f397c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f397c-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f397c-113">-ElasticPoolName</span></span>
<span data-ttu-id="f397c-114">Annak a rugalmas készletnek a nevét adja meg, amelyre a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="f397c-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f397c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f397c-115">-Force</span></span>
<span data-ttu-id="f397c-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="f397c-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f397c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f397c-117">-ResourceGroupName</span></span>
<span data-ttu-id="f397c-118">Annak az erőforráscsoport a neve, amelyhez a rugalmas készlet van rendelve.</span><span class="sxs-lookup"><span data-stu-id="f397c-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="f397c-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f397c-119">-ServerName</span></span>
<span data-ttu-id="f397c-120">A rugalmas készletet tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f397c-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="f397c-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f397c-121">-Confirm</span></span>
<span data-ttu-id="f397c-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f397c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f397c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f397c-123">-WhatIf</span></span>
<span data-ttu-id="f397c-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f397c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f397c-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f397c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f397c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f397c-126">CommonParameters</span></span>
<span data-ttu-id="f397c-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f397c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f397c-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f397c-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f397c-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f397c-129">INPUTS</span></span>

### <span data-ttu-id="f397c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f397c-130">System.String</span></span>

## <span data-ttu-id="f397c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f397c-131">OUTPUTS</span></span>

### <span data-ttu-id="f397c-132">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="f397c-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="f397c-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f397c-133">NOTES</span></span>

## <span data-ttu-id="f397c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f397c-134">RELATED LINKS</span></span>

[<span data-ttu-id="f397c-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f397c-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="f397c-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="f397c-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="f397c-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="f397c-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="f397c-138">Új – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f397c-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="f397c-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f397c-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="f397c-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f397c-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



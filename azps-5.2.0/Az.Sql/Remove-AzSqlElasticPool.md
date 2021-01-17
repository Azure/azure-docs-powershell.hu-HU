---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: d751954a5c66d9220513017aa62b6797f8f1ea6f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369625"
---
# <span data-ttu-id="b639b-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b639b-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="b639b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b639b-102">SYNOPSIS</span></span>
<span data-ttu-id="b639b-103">Egy rugalmas adatbáziskészlet törlése.</span><span class="sxs-lookup"><span data-stu-id="b639b-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="b639b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b639b-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b639b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b639b-105">DESCRIPTION</span></span>
<span data-ttu-id="b639b-106">A **Remove-AzSqlElasticPool** parancsmag törli az Azure SQL-adatbázis rugalmas készletét.</span><span class="sxs-lookup"><span data-stu-id="b639b-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="b639b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b639b-107">EXAMPLES</span></span>

### <span data-ttu-id="b639b-108">1. példa: Rugalmas készlet törlése</span><span class="sxs-lookup"><span data-stu-id="b639b-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="b639b-109">Ez a parancs töröl egy RugalmasságPool01 nevű rugalmas készletet.</span><span class="sxs-lookup"><span data-stu-id="b639b-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="b639b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b639b-110">PARAMETERS</span></span>

### <span data-ttu-id="b639b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b639b-111">-DefaultProfile</span></span>
<span data-ttu-id="b639b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b639b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b639b-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b639b-113">-ElasticPoolName</span></span>
<span data-ttu-id="b639b-114">Annak a rugalmas készletnek a nevét adja meg, amelyből a parancsmag töröl.</span><span class="sxs-lookup"><span data-stu-id="b639b-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="b639b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b639b-115">-Force</span></span>
<span data-ttu-id="b639b-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="b639b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b639b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b639b-117">-ResourceGroupName</span></span>
<span data-ttu-id="b639b-118">Annak az erőforráscsoportnak a neve, amelyhez a rugalmas készlet hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b639b-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="b639b-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b639b-119">-ServerName</span></span>
<span data-ttu-id="b639b-120">A rugalmas készletet tartalmazó kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="b639b-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="b639b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b639b-121">-Confirm</span></span>
<span data-ttu-id="b639b-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b639b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b639b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b639b-123">-WhatIf</span></span>
<span data-ttu-id="b639b-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b639b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b639b-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b639b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b639b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b639b-126">CommonParameters</span></span>
<span data-ttu-id="b639b-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b639b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b639b-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b639b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b639b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b639b-129">INPUTS</span></span>

### <span data-ttu-id="b639b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b639b-130">System.String</span></span>

## <span data-ttu-id="b639b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b639b-131">OUTPUTS</span></span>

### <span data-ttu-id="b639b-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="b639b-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="b639b-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b639b-133">NOTES</span></span>

## <span data-ttu-id="b639b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b639b-134">RELATED LINKS</span></span>

[<span data-ttu-id="b639b-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b639b-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="b639b-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="b639b-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="b639b-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="b639b-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="b639b-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b639b-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="b639b-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b639b-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="b639b-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b639b-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



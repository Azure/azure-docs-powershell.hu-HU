---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 013a7c40a5acfb4306d53e0ff5b8da1b54f86e46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999558"
---
# <span data-ttu-id="315ee-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="315ee-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="315ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="315ee-102">SYNOPSIS</span></span>
<span data-ttu-id="315ee-103">Egy rugalmas készleten található műveletek állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="315ee-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="315ee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="315ee-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="315ee-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="315ee-105">DESCRIPTION</span></span>
<span data-ttu-id="315ee-106">A **Get-AzSqlElasticPoolActivity** parancsmag egy Azure SQL-adatbázis rugalmas készletén található műveletek állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="315ee-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="315ee-107">A készlet létrehozási és konfigurációs frissítésének állapotát egyaránt láthatja.</span><span class="sxs-lookup"><span data-stu-id="315ee-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="315ee-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="315ee-108">EXAMPLES</span></span>

### <span data-ttu-id="315ee-109">1. példa: Rugalmas készlet műveleteinek állapotának megtekintése</span><span class="sxs-lookup"><span data-stu-id="315ee-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="315ee-110">Ez a parancs a RugalmasságPool01 nevű rugalmas készlet műveleteinek állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="315ee-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="315ee-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="315ee-111">PARAMETERS</span></span>

### <span data-ttu-id="315ee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="315ee-112">-DefaultProfile</span></span>
<span data-ttu-id="315ee-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="315ee-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="315ee-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="315ee-114">-ElasticPoolName</span></span>
<span data-ttu-id="315ee-115">Egy rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="315ee-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="315ee-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="315ee-116">-OperationId</span></span>
<span data-ttu-id="315ee-117">A visszakeresni szükséges művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="315ee-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="315ee-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="315ee-118">-ResourceGroupName</span></span>
<span data-ttu-id="315ee-119">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a rugalmas készlet hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="315ee-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="315ee-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="315ee-120">-ServerName</span></span>
<span data-ttu-id="315ee-121">Egy rugalmas készletet tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="315ee-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="315ee-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="315ee-122">-Confirm</span></span>
<span data-ttu-id="315ee-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="315ee-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="315ee-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="315ee-124">-WhatIf</span></span>
<span data-ttu-id="315ee-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="315ee-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="315ee-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="315ee-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="315ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="315ee-127">CommonParameters</span></span>
<span data-ttu-id="315ee-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="315ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="315ee-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="315ee-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="315ee-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="315ee-130">INPUTS</span></span>

### <span data-ttu-id="315ee-131">System.String</span><span class="sxs-lookup"><span data-stu-id="315ee-131">System.String</span></span>

### <span data-ttu-id="315ee-132">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="315ee-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="315ee-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="315ee-133">OUTPUTS</span></span>

### <span data-ttu-id="315ee-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="315ee-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="315ee-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="315ee-135">NOTES</span></span>

## <span data-ttu-id="315ee-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="315ee-136">RELATED LINKS</span></span>

[<span data-ttu-id="315ee-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="315ee-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="315ee-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="315ee-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="315ee-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="315ee-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="315ee-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="315ee-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="315ee-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="315ee-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)



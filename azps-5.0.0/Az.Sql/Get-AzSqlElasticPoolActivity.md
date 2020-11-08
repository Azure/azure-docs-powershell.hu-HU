---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 2e0768b14337f4504df1e6cdf9565533584e0339
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185836"
---
# <span data-ttu-id="789e0-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="789e0-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="789e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="789e0-102">SYNOPSIS</span></span>
<span data-ttu-id="789e0-103">Egy rugalmas készleten kapja meg a műveletek állapotát.</span><span class="sxs-lookup"><span data-stu-id="789e0-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="789e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="789e0-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="789e0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="789e0-105">DESCRIPTION</span></span>
<span data-ttu-id="789e0-106">A **Get-AzSqlElasticPoolActivity** parancsmag a műveletek állapotát az Azure SQL-adatbázisok rugalmas készletében kapja.</span><span class="sxs-lookup"><span data-stu-id="789e0-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="789e0-107">A Pool-készítési és a konfigurációs frissítések állapotát is láthatja.</span><span class="sxs-lookup"><span data-stu-id="789e0-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="789e0-108">Példák</span><span class="sxs-lookup"><span data-stu-id="789e0-108">EXAMPLES</span></span>

### <span data-ttu-id="789e0-109">Példa 1: műveletek állapotának megszerzése rugalmas készlet esetén</span><span class="sxs-lookup"><span data-stu-id="789e0-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="789e0-110">Ez a parancs a ElasticPool01 nevű rugalmas készlet műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="789e0-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="789e0-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="789e0-111">PARAMETERS</span></span>

### <span data-ttu-id="789e0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789e0-112">-DefaultProfile</span></span>
<span data-ttu-id="789e0-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="789e0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="789e0-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="789e0-114">-ElasticPoolName</span></span>
<span data-ttu-id="789e0-115">Egy rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="789e0-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="789e0-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="789e0-116">-OperationId</span></span>
<span data-ttu-id="789e0-117">A lekérdezni kívánt művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="789e0-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="789e0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="789e0-118">-ResourceGroupName</span></span>
<span data-ttu-id="789e0-119">Annak a csoportnak a neve, amelyhez a rugalmas készlet van rendelve.</span><span class="sxs-lookup"><span data-stu-id="789e0-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="789e0-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="789e0-120">-ServerName</span></span>
<span data-ttu-id="789e0-121">Egy rugalmas készletet tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="789e0-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="789e0-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="789e0-122">-Confirm</span></span>
<span data-ttu-id="789e0-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="789e0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="789e0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="789e0-124">-WhatIf</span></span>
<span data-ttu-id="789e0-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="789e0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="789e0-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="789e0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="789e0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789e0-127">CommonParameters</span></span>
<span data-ttu-id="789e0-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="789e0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789e0-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="789e0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789e0-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="789e0-130">INPUTS</span></span>

### <span data-ttu-id="789e0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="789e0-131">System.String</span></span>

### <span data-ttu-id="789e0-132">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="789e0-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="789e0-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="789e0-133">OUTPUTS</span></span>

### <span data-ttu-id="789e0-134">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="789e0-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="789e0-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="789e0-135">NOTES</span></span>

## <span data-ttu-id="789e0-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="789e0-136">RELATED LINKS</span></span>

[<span data-ttu-id="789e0-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="789e0-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="789e0-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="789e0-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="789e0-139">Új – AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="789e0-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="789e0-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="789e0-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="789e0-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="789e0-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)



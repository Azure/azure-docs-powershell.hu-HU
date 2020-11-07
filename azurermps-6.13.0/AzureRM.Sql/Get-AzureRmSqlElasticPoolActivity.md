---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: f5e7455a253c86fe363b72c5d4c0e8ff47b96f56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679136"
---
# <span data-ttu-id="e704a-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="e704a-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="e704a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e704a-102">SYNOPSIS</span></span>
<span data-ttu-id="e704a-103">Egy rugalmas készleten kapja meg a műveletek állapotát.</span><span class="sxs-lookup"><span data-stu-id="e704a-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e704a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e704a-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e704a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e704a-105">DESCRIPTION</span></span>
<span data-ttu-id="e704a-106">A **Get-AzureRmSqlElasticPoolActivity** parancsmag a műveletek állapotát az Azure SQL-adatbázisok rugalmas készletében kapja.</span><span class="sxs-lookup"><span data-stu-id="e704a-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="e704a-107">A Pool-készítési és a konfigurációs frissítések állapotát is láthatja.</span><span class="sxs-lookup"><span data-stu-id="e704a-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="e704a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e704a-108">EXAMPLES</span></span>

### <span data-ttu-id="e704a-109">Példa 1: műveletek állapotának megszerzése rugalmas készlet esetén</span><span class="sxs-lookup"><span data-stu-id="e704a-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="e704a-110">Ez a parancs a ElasticPool01 nevű rugalmas készlet műveletének állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e704a-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="e704a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e704a-111">PARAMETERS</span></span>

### <span data-ttu-id="e704a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e704a-112">-DefaultProfile</span></span>
<span data-ttu-id="e704a-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e704a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e704a-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e704a-114">-ElasticPoolName</span></span>
<span data-ttu-id="e704a-115">Egy rugalmas készlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e704a-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="e704a-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e704a-116">-OperationId</span></span>
<span data-ttu-id="e704a-117">A lekérdezni kívánt művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e704a-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="e704a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e704a-118">-ResourceGroupName</span></span>
<span data-ttu-id="e704a-119">Annak a csoportnak a neve, amelyhez a rugalmas készlet van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e704a-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="e704a-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e704a-120">-ServerName</span></span>
<span data-ttu-id="e704a-121">Egy rugalmas készletet tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e704a-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="e704a-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e704a-122">-Confirm</span></span>
<span data-ttu-id="e704a-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e704a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e704a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e704a-124">-WhatIf</span></span>
<span data-ttu-id="e704a-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e704a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e704a-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e704a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e704a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e704a-127">CommonParameters</span></span>
<span data-ttu-id="e704a-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e704a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e704a-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e704a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e704a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e704a-130">INPUTS</span></span>

### <span data-ttu-id="e704a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e704a-131">System.String</span></span>

### <span data-ttu-id="e704a-132">System. null ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e704a-132">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e704a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e704a-133">OUTPUTS</span></span>

### <span data-ttu-id="e704a-134">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="e704a-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="e704a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e704a-135">NOTES</span></span>

## <span data-ttu-id="e704a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e704a-136">RELATED LINKS</span></span>

[<span data-ttu-id="e704a-137">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e704a-137">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e704a-138">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="e704a-138">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="e704a-139">Új – AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e704a-139">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e704a-140">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e704a-140">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e704a-141">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e704a-141">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: dc1dffd84a95bd9cffac1dbafb5183d56e0b7c52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195295"
---
# <span data-ttu-id="7122d-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="7122d-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="7122d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7122d-102">SYNOPSIS</span></span>
<span data-ttu-id="7122d-103">Egy rugalmas készleten lemondja az aszinkron frissítési műveletet.</span><span class="sxs-lookup"><span data-stu-id="7122d-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="7122d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7122d-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7122d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7122d-105">DESCRIPTION</span></span>
<span data-ttu-id="7122d-106">A **stop-AzSqlElasticPoolActivity** parancsmag egy rugalmas készleten megszünteti az aszinkron frissítési műveletet.</span><span class="sxs-lookup"><span data-stu-id="7122d-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="7122d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7122d-107">EXAMPLES</span></span>

### <span data-ttu-id="7122d-108">1. példa: az aszinkron frissítési művelet megszakítása rugalmas készleten</span><span class="sxs-lookup"><span data-stu-id="7122d-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete :
```

<span data-ttu-id="7122d-109">Ez a parancs a rugalmas készleten lemondja az aszinkron frissítések műveletet.</span><span class="sxs-lookup"><span data-stu-id="7122d-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="7122d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7122d-110">PARAMETERS</span></span>

### <span data-ttu-id="7122d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7122d-111">-DefaultProfile</span></span>
<span data-ttu-id="7122d-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7122d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7122d-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7122d-113">-ElasticPoolName</span></span>
<span data-ttu-id="7122d-114">Az Azure SQL elasztikus Pool neve.</span><span class="sxs-lookup"><span data-stu-id="7122d-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="7122d-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7122d-115">-OperationId</span></span>
<span data-ttu-id="7122d-116">A lekérdezni kívánt művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7122d-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="7122d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7122d-117">-PassThru</span></span>
<span data-ttu-id="7122d-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7122d-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7122d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7122d-119">-ResourceGroupName</span></span>
<span data-ttu-id="7122d-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7122d-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7122d-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="7122d-121">-ServerName</span></span>
<span data-ttu-id="7122d-122">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben a rugalmas készlet található.</span><span class="sxs-lookup"><span data-stu-id="7122d-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="7122d-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7122d-123">-Confirm</span></span>
<span data-ttu-id="7122d-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7122d-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7122d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7122d-125">-WhatIf</span></span>
<span data-ttu-id="7122d-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7122d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7122d-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7122d-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7122d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7122d-128">CommonParameters</span></span>
<span data-ttu-id="7122d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7122d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7122d-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7122d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7122d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7122d-131">INPUTS</span></span>

### <span data-ttu-id="7122d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7122d-132">System.String</span></span>

### <span data-ttu-id="7122d-133">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7122d-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7122d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7122d-134">OUTPUTS</span></span>

### <span data-ttu-id="7122d-135">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="7122d-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="7122d-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7122d-136">NOTES</span></span>

## <span data-ttu-id="7122d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7122d-137">RELATED LINKS</span></span>

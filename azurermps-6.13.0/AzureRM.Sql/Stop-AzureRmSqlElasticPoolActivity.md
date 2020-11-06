---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 999fd83af11422f1499e386f194fd75d9b99e152
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494859"
---
# <span data-ttu-id="1cfe1-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="1cfe1-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="1cfe1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1cfe1-102">SYNOPSIS</span></span>
<span data-ttu-id="1cfe1-103">Egy rugalmas készleten lemondja az aszinkron frissítési műveletet.</span><span class="sxs-lookup"><span data-stu-id="1cfe1-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cfe1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1cfe1-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cfe1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1cfe1-105">DESCRIPTION</span></span>
<span data-ttu-id="1cfe1-106">A **stop-AzureRmSqlElasticPoolActivity** parancsmag egy rugalmas készleten megszünteti az aszinkron frissítési műveletet.</span><span class="sxs-lookup"><span data-stu-id="1cfe1-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="1cfe1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1cfe1-107">EXAMPLES</span></span>

### <span data-ttu-id="1cfe1-108">1. példa: az aszinkron frissítési művelet megszakítása rugalmas készleten</span><span class="sxs-lookup"><span data-stu-id="1cfe1-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="1cfe1-109">Ez a parancs a rugalmas készleten lemondja az aszinkron frissítések műveletet.</span><span class="sxs-lookup"><span data-stu-id="1cfe1-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="1cfe1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1cfe1-110">PARAMETERS</span></span>

### <span data-ttu-id="1cfe1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cfe1-111">-DefaultProfile</span></span>
<span data-ttu-id="1cfe1-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1cfe1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cfe1-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1cfe1-113">-ElasticPoolName</span></span>
<span data-ttu-id="1cfe1-114">Az Azure SQL elasztikus Pool neve.</span><span class="sxs-lookup"><span data-stu-id="1cfe1-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="1cfe1-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="1cfe1-115">-OperationId</span></span>
<span data-ttu-id="1cfe1-116">A lekérdezni kívánt művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1cfe1-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="1cfe1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cfe1-117">-PassThru</span></span>
<span data-ttu-id="1cfe1-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1cfe1-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1cfe1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cfe1-119">-ResourceGroupName</span></span>
<span data-ttu-id="1cfe1-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1cfe1-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="1cfe1-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1cfe1-121">-ServerName</span></span>
<span data-ttu-id="1cfe1-122">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben a rugalmas készlet található.</span><span class="sxs-lookup"><span data-stu-id="1cfe1-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="1cfe1-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1cfe1-123">-Confirm</span></span>
<span data-ttu-id="1cfe1-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1cfe1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cfe1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cfe1-125">-WhatIf</span></span>
<span data-ttu-id="1cfe1-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1cfe1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cfe1-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1cfe1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cfe1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cfe1-128">CommonParameters</span></span>
<span data-ttu-id="1cfe1-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1cfe1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cfe1-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cfe1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cfe1-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cfe1-131">INPUTS</span></span>

### <span data-ttu-id="1cfe1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1cfe1-132">System.String</span></span>

### <span data-ttu-id="1cfe1-133">System. null ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1cfe1-133">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="1cfe1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cfe1-134">OUTPUTS</span></span>

### <span data-ttu-id="1cfe1-135">Microsoft. Azure. Command. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="1cfe1-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="1cfe1-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1cfe1-136">NOTES</span></span>

## <span data-ttu-id="1cfe1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1cfe1-137">RELATED LINKS</span></span>

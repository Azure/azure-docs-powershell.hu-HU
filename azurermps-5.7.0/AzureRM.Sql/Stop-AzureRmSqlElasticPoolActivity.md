---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 87744454627feaadc8c953e1ad4e50016f14879f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500363"
---
# <span data-ttu-id="cfdb1-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="cfdb1-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="cfdb1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cfdb1-102">SYNOPSIS</span></span>
<span data-ttu-id="cfdb1-103">Egy rugalmas készleten lemondja az aszinkron frissítési műveletet.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfdb1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cfdb1-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cfdb1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cfdb1-105">DESCRIPTION</span></span>
<span data-ttu-id="cfdb1-106">A **stop-AzureRmSqlElasticPoolActivity** parancsmag egy rugalmas készleten megszünteti az aszinkron frissítési műveletet.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="cfdb1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cfdb1-107">EXAMPLES</span></span>

### <span data-ttu-id="cfdb1-108">1. példa: az aszinkron frissítési művelet megszakítása rugalmas készleten</span><span class="sxs-lookup"><span data-stu-id="cfdb1-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
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

<span data-ttu-id="cfdb1-109">Ez a parancs a rugalmas készleten lemondja az aszinkron frissítések műveletet.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="cfdb1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cfdb1-110">PARAMETERS</span></span>

### <span data-ttu-id="cfdb1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfdb1-111">-DefaultProfile</span></span>
<span data-ttu-id="cfdb1-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfdb1-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="cfdb1-113">-ElasticPoolName</span></span>
<span data-ttu-id="cfdb1-114">Az Azure SQL elasztikus Pool neve.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-114">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfdb1-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="cfdb1-115">-OperationId</span></span>
<span data-ttu-id="cfdb1-116">A lekérdezni kívánt művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-116">The ID of the operation to retrieve.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfdb1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfdb1-117">-ResourceGroupName</span></span>
<span data-ttu-id="cfdb1-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="cfdb1-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="cfdb1-119">-ServerName</span></span>
<span data-ttu-id="cfdb1-120">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben a rugalmas készlet található.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-120">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="cfdb1-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cfdb1-121">-Confirm</span></span>
<span data-ttu-id="cfdb1-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdb1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfdb1-123">-WhatIf</span></span>
<span data-ttu-id="cfdb1-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfdb1-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfdb1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfdb1-126">CommonParameters</span></span>
<span data-ttu-id="cfdb1-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cfdb1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfdb1-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfdb1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfdb1-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfdb1-129">INPUTS</span></span>

### <span data-ttu-id="cfdb1-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="cfdb1-130">None</span></span>

<span data-ttu-id="cfdb1-131">A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="cfdb1-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfdb1-132">OUTPUTS</span></span>

### <span data-ttu-id="cfdb1-133">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="cfdb1-133">System.Object</span></span>

## <span data-ttu-id="cfdb1-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cfdb1-134">NOTES</span></span>

## <span data-ttu-id="cfdb1-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfdb1-135">RELATED LINKS</span></span>




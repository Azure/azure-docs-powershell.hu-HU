---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 149579bb6bbcd4ee5fe5fa192ad040e6e4c68b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505575"
---
# <span data-ttu-id="5614b-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="5614b-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="5614b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5614b-102">SYNOPSIS</span></span>
<span data-ttu-id="5614b-103">Egy Azure SQL-adatbázis-tanácsadó automatikus végrehajtási állapotát módosítja.</span><span class="sxs-lookup"><span data-stu-id="5614b-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5614b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5614b-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5614b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5614b-105">DESCRIPTION</span></span>
<span data-ttu-id="5614b-106">A **set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** parancsmag módosította az Azure SQL-adatbázis-tanácsadók automatikus végrehajtás tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="5614b-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="5614b-107">Ez a parancsmag jelenleg az engedélyezett, a letiltott és az alapértelmezett értéket támogatja.</span><span class="sxs-lookup"><span data-stu-id="5614b-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="5614b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5614b-108">EXAMPLES</span></span>

### <span data-ttu-id="5614b-109">1. példa: az automatikus végrehajtás engedélyezése egy tanácsadónál</span><span class="sxs-lookup"><span data-stu-id="5614b-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="5614b-110">Ez a parancs módosítja egy CreateIndex nevű tanácsadó automatikus végrehajtási állapotát.</span><span class="sxs-lookup"><span data-stu-id="5614b-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="5614b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5614b-111">PARAMETERS</span></span>

### <span data-ttu-id="5614b-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="5614b-112">-AdvisorName</span></span>
<span data-ttu-id="5614b-113">Annak a tanácsadónak a nevét adja meg, amelyhez ez a parancsmag módosította az állapotot.</span><span class="sxs-lookup"><span data-stu-id="5614b-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="5614b-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="5614b-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="5614b-115">Az állapot értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5614b-115">Specifies the value for the status.</span></span>
<span data-ttu-id="5614b-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5614b-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5614b-117">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="5614b-117">Enabled</span></span> 
- <span data-ttu-id="5614b-118">Tiltva</span><span class="sxs-lookup"><span data-stu-id="5614b-118">Disabled</span></span> 
- <span data-ttu-id="5614b-119">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="5614b-119">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5614b-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5614b-120">-DatabaseName</span></span>
<span data-ttu-id="5614b-121">Annak az adatbázisnak a nevét adja meg, amelynek a parancsmagja módosította az állapotot.</span><span class="sxs-lookup"><span data-stu-id="5614b-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="5614b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5614b-122">-ResourceGroupName</span></span>
<span data-ttu-id="5614b-123">Az adatbázist tartalmazó kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5614b-123">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="5614b-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="5614b-124">-ServerName</span></span>
<span data-ttu-id="5614b-125">Az adatbázis kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5614b-125">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="5614b-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5614b-126">-Confirm</span></span>
<span data-ttu-id="5614b-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5614b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5614b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5614b-128">-WhatIf</span></span>
<span data-ttu-id="5614b-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5614b-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5614b-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5614b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5614b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5614b-131">-DefaultProfile</span></span>
<span data-ttu-id="5614b-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5614b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5614b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5614b-133">CommonParameters</span></span>
<span data-ttu-id="5614b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5614b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5614b-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5614b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5614b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5614b-136">INPUTS</span></span>

## <span data-ttu-id="5614b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5614b-137">OUTPUTS</span></span>

### <span data-ttu-id="5614b-138">Microsoft. Azure. Command. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="5614b-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>
<span data-ttu-id="5614b-139">Ez a parancsmag egy **AzureSqlDatabaseAdvisorModel** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="5614b-139">This cmdlet returns an **AzureSqlDatabaseAdvisorModel** object.</span></span>

## <span data-ttu-id="5614b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5614b-140">NOTES</span></span>

## <span data-ttu-id="5614b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5614b-141">RELATED LINKS</span></span>

[<span data-ttu-id="5614b-142">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="5614b-142">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="5614b-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="5614b-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveradvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 02a4348511afabe7f398eafeb6d0849525f0abac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186960"
---
# <span data-ttu-id="38d2a-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="38d2a-101">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="38d2a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="38d2a-103">Egy Azure SQL Server-tanácsadó automatikus végrehajtási állapotát frissíti.</span><span class="sxs-lookup"><span data-stu-id="38d2a-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="38d2a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38d2a-104">SYNTAX</span></span>

```
Set-AzSqlServerAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38d2a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="38d2a-105">DESCRIPTION</span></span>
<span data-ttu-id="38d2a-106">A **set-AzSqlServerAdvisorAutoExecuteStatus** parancsmag az Azure SQL Server-tanácsadók automatikus végrehajtás tulajdonságát állítja be.</span><span class="sxs-lookup"><span data-stu-id="38d2a-106">The **Set-AzSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="38d2a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="38d2a-107">EXAMPLES</span></span>

### <span data-ttu-id="38d2a-108">1. példa: az automatikus végrehajtás engedélyezése egy tanácsadónál</span><span class="sxs-lookup"><span data-stu-id="38d2a-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="38d2a-109">Ez a parancs lehetővé teszi egy CreateIndex nevű tanácsadó automatikus végrehajtási állapotát.</span><span class="sxs-lookup"><span data-stu-id="38d2a-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="38d2a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38d2a-110">PARAMETERS</span></span>

### <span data-ttu-id="38d2a-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="38d2a-111">-AdvisorName</span></span>
<span data-ttu-id="38d2a-112">Annak a tanácsadónak a nevét adja meg, amelynek a parancsmagja frissíti az automatikus végrehajtás állapotát.</span><span class="sxs-lookup"><span data-stu-id="38d2a-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="38d2a-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="38d2a-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="38d2a-114">Azt az értéket adja meg, amelyre ez a parancsmag frissíti az automatikus végrehajtás állapotát.</span><span class="sxs-lookup"><span data-stu-id="38d2a-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>
<span data-ttu-id="38d2a-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="38d2a-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38d2a-116">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="38d2a-116">Enabled</span></span>
- <span data-ttu-id="38d2a-117">Tiltva</span><span class="sxs-lookup"><span data-stu-id="38d2a-117">Disabled</span></span>
- <span data-ttu-id="38d2a-118">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="38d2a-118">Default</span></span>

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

### <span data-ttu-id="38d2a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d2a-119">-DefaultProfile</span></span>
<span data-ttu-id="38d2a-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="38d2a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38d2a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d2a-121">-ResourceGroupName</span></span>
<span data-ttu-id="38d2a-122">A kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38d2a-122">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="38d2a-123">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="38d2a-123">-ServerName</span></span>
<span data-ttu-id="38d2a-124">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38d2a-124">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="38d2a-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="38d2a-125">-Confirm</span></span>
<span data-ttu-id="38d2a-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="38d2a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38d2a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38d2a-127">-WhatIf</span></span>
<span data-ttu-id="38d2a-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="38d2a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38d2a-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38d2a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38d2a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d2a-130">CommonParameters</span></span>
<span data-ttu-id="38d2a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38d2a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d2a-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="38d2a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d2a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38d2a-133">INPUTS</span></span>

### <span data-ttu-id="38d2a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="38d2a-134">System.String</span></span>

### <span data-ttu-id="38d2a-135">Microsoft. Azure. Command. SQL. Advisor. parancsmag. AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="38d2a-135">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="38d2a-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38d2a-136">OUTPUTS</span></span>

### <span data-ttu-id="38d2a-137">Microsoft. Azure. Command. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="38d2a-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="38d2a-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38d2a-138">NOTES</span></span>
* <span data-ttu-id="38d2a-139">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, Server, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="38d2a-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="38d2a-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38d2a-140">RELATED LINKS</span></span>

[<span data-ttu-id="38d2a-141">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="38d2a-141">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="38d2a-142">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="38d2a-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
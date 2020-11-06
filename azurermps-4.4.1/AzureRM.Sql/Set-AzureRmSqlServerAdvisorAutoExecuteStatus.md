---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: f483d3deb6c4e4ee6fb5c091dffc9b7969766d6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499124"
---
# <span data-ttu-id="29b74-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="29b74-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="29b74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29b74-102">SYNOPSIS</span></span>
<span data-ttu-id="29b74-103">Egy Azure SQL Server-tanácsadó automatikus végrehajtási állapotát frissíti.</span><span class="sxs-lookup"><span data-stu-id="29b74-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29b74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29b74-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29b74-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29b74-105">DESCRIPTION</span></span>
<span data-ttu-id="29b74-106">A **set-AzureRmSqlServerAdvisorAutoExecuteStatus** parancsmag az Azure SQL Server-tanácsadók automatikus végrehajtás tulajdonságát állítja be.</span><span class="sxs-lookup"><span data-stu-id="29b74-106">The **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="29b74-107">Példák</span><span class="sxs-lookup"><span data-stu-id="29b74-107">EXAMPLES</span></span>

### <span data-ttu-id="29b74-108">1. példa: az automatikus végrehajtás engedélyezése egy tanácsadónál</span><span class="sxs-lookup"><span data-stu-id="29b74-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzureRmSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
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

<span data-ttu-id="29b74-109">Ez a parancs lehetővé teszi egy CreateIndex nevű tanácsadó automatikus végrehajtási állapotát.</span><span class="sxs-lookup"><span data-stu-id="29b74-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="29b74-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29b74-110">PARAMETERS</span></span>

### <span data-ttu-id="29b74-111">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="29b74-111">-AdvisorName</span></span>
<span data-ttu-id="29b74-112">Annak a tanácsadónak a nevét adja meg, amelynek a parancsmagja frissíti az automatikus végrehajtás állapotát.</span><span class="sxs-lookup"><span data-stu-id="29b74-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="29b74-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="29b74-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="29b74-114">Azt az értéket adja meg, amelyre ez a parancsmag frissíti az automatikus végrehajtás állapotát.</span><span class="sxs-lookup"><span data-stu-id="29b74-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="29b74-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="29b74-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29b74-116">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="29b74-116">Enabled</span></span>
- <span data-ttu-id="29b74-117">Tiltva</span><span class="sxs-lookup"><span data-stu-id="29b74-117">Disabled</span></span>
- <span data-ttu-id="29b74-118">Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="29b74-118">Default</span></span>

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

### <span data-ttu-id="29b74-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29b74-119">-ResourceGroupName</span></span>
<span data-ttu-id="29b74-120">A kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29b74-120">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="29b74-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="29b74-121">-ServerName</span></span>
<span data-ttu-id="29b74-122">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29b74-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="29b74-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29b74-123">-Confirm</span></span>
<span data-ttu-id="29b74-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29b74-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29b74-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29b74-125">-WhatIf</span></span>
<span data-ttu-id="29b74-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29b74-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29b74-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29b74-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29b74-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b74-128">-DefaultProfile</span></span>
<span data-ttu-id="29b74-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29b74-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29b74-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b74-130">CommonParameters</span></span>
<span data-ttu-id="29b74-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29b74-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b74-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29b74-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b74-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29b74-133">INPUTS</span></span>

## <span data-ttu-id="29b74-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29b74-134">OUTPUTS</span></span>

### <span data-ttu-id="29b74-135">Microsoft. Azure. Command. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="29b74-135">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="29b74-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29b74-136">NOTES</span></span>
* <span data-ttu-id="29b74-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, Server, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="29b74-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="29b74-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29b74-138">RELATED LINKS</span></span>

[<span data-ttu-id="29b74-139">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="29b74-139">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="29b74-140">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="29b74-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

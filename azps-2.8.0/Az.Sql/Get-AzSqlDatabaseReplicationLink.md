---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
ms.openlocfilehash: 6bb2a3891abe8453ee8460f6879dbc134f6ab29b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839238"
---
# <span data-ttu-id="01ba3-101">Get-AzSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="01ba3-101">Get-AzSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="01ba3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="01ba3-103">A Geo-replikációs kapcsolatokat az Azure SQL-adatbázis és egy erőforráscsoport vagy SQL-kiszolgáló között kapja.</span><span class="sxs-lookup"><span data-stu-id="01ba3-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

## <span data-ttu-id="01ba3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01ba3-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01ba3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="01ba3-105">DESCRIPTION</span></span>
<span data-ttu-id="01ba3-106">A **Get-AzSqlDatabaseReplicationLink** parancsmag lecseréli a **Get-AzSqlDatabaseCopy** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="01ba3-106">The **Get-AzSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="01ba3-107">A megadott Azure SQL-adatbázis és egy erőforráscsoport vagy AzureSQL-kiszolgáló között minden geo-replikációs kapcsolatot kap.</span><span class="sxs-lookup"><span data-stu-id="01ba3-107">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="01ba3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="01ba3-108">EXAMPLES</span></span>

## <span data-ttu-id="01ba3-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01ba3-109">PARAMETERS</span></span>

### <span data-ttu-id="01ba3-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="01ba3-110">-DatabaseName</span></span>
<span data-ttu-id="01ba3-111">Annak az SQL-adatbázisnak a neve, amelyből a hivatkozásokat le szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="01ba3-111">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="01ba3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ba3-112">-DefaultProfile</span></span>
<span data-ttu-id="01ba3-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="01ba3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01ba3-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01ba3-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="01ba3-115">Annak az erőforrás-csoportnak a neve, amelyhez a partner hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="01ba3-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="01ba3-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="01ba3-116">-PartnerServerName</span></span>
<span data-ttu-id="01ba3-117">A partner Azure SQL Server-kiszolgálójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="01ba3-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="01ba3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01ba3-118">-ResourceGroupName</span></span>
<span data-ttu-id="01ba3-119">Annak az adatbázisnak az Azure-erőforráscsoport nevét adja meg, amelynek a hivatkozásait le szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="01ba3-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="01ba3-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="01ba3-120">-ServerName</span></span>
<span data-ttu-id="01ba3-121">Annak az SQL-kiszolgálónak a nevét adja meg, amelybe a hivatkozásokat le szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="01ba3-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="01ba3-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="01ba3-122">-Confirm</span></span>
<span data-ttu-id="01ba3-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="01ba3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01ba3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01ba3-124">-WhatIf</span></span>
<span data-ttu-id="01ba3-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="01ba3-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01ba3-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01ba3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01ba3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ba3-127">CommonParameters</span></span>
<span data-ttu-id="01ba3-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01ba3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ba3-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="01ba3-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ba3-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01ba3-130">INPUTS</span></span>

### <span data-ttu-id="01ba3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="01ba3-131">System.String</span></span>

## <span data-ttu-id="01ba3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01ba3-132">OUTPUTS</span></span>

### <span data-ttu-id="01ba3-133">Microsoft. Azure. Command. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="01ba3-133">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="01ba3-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01ba3-134">NOTES</span></span>

## <span data-ttu-id="01ba3-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01ba3-135">RELATED LINKS</span></span>

[<span data-ttu-id="01ba3-136">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="01ba3-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

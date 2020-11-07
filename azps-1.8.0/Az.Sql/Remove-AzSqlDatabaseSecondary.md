---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 6e77f70c92d9075671a0011e54c4cc4fc5df764c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668856"
---
# <span data-ttu-id="b7acb-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b7acb-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="b7acb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7acb-102">SYNOPSIS</span></span>
<span data-ttu-id="b7acb-103">Az SQL-adatbázis és a megadott másodlagos adatbázis közötti adatreplikáció megszüntetése</span><span class="sxs-lookup"><span data-stu-id="b7acb-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="b7acb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7acb-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7acb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7acb-105">DESCRIPTION</span></span>
<span data-ttu-id="b7acb-106">A **Remove-AzSqlDatabaseSecondary** parancsmag a Geo-replikációs hivatkozás megszüntetését kényszeríti.</span><span class="sxs-lookup"><span data-stu-id="b7acb-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="b7acb-107">Ez a parancsmag az Stop-AzSqlDatabaseCopy parancsmagot cseréli le.</span><span class="sxs-lookup"><span data-stu-id="b7acb-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="b7acb-108">A megszakítás előtt nincs replikációs szinkronizálás.</span><span class="sxs-lookup"><span data-stu-id="b7acb-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="b7acb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b7acb-109">EXAMPLES</span></span>

## <span data-ttu-id="b7acb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7acb-110">PARAMETERS</span></span>

### <span data-ttu-id="b7acb-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7acb-111">-DatabaseName</span></span>
<span data-ttu-id="b7acb-112">Annak az elsődleges Azure SQL-adatbázisnak a neve, amely a parancsmag által eltávolított replikációs hivatkozással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="b7acb-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b7acb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7acb-113">-DefaultProfile</span></span>
<span data-ttu-id="b7acb-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b7acb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7acb-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7acb-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="b7acb-116">A partner erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7acb-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="b7acb-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="b7acb-117">-PartnerServerName</span></span>
<span data-ttu-id="b7acb-118">Adja meg a partner SQL-kiszolgálójának nevét.</span><span class="sxs-lookup"><span data-stu-id="b7acb-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="b7acb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7acb-119">-ResourceGroupName</span></span>
<span data-ttu-id="b7acb-120">Az eltávolítandó replikációs hivatkozással társított erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7acb-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="b7acb-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b7acb-121">-ServerName</span></span>
<span data-ttu-id="b7acb-122">Annak az SQL-kiszolgálónak a nevét adja meg, amelynek a replikációs hivatkozását el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="b7acb-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="b7acb-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7acb-123">-Confirm</span></span>
<span data-ttu-id="b7acb-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7acb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7acb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7acb-125">-WhatIf</span></span>
<span data-ttu-id="b7acb-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b7acb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7acb-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7acb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7acb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7acb-128">CommonParameters</span></span>
<span data-ttu-id="b7acb-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7acb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7acb-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b7acb-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7acb-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7acb-131">INPUTS</span></span>

### <span data-ttu-id="b7acb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b7acb-132">System.String</span></span>

## <span data-ttu-id="b7acb-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7acb-133">OUTPUTS</span></span>

### <span data-ttu-id="b7acb-134">Microsoft. Azure. Command. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="b7acb-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="b7acb-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7acb-135">NOTES</span></span>

## <span data-ttu-id="b7acb-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7acb-136">RELATED LINKS</span></span>

[<span data-ttu-id="b7acb-137">Új – AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b7acb-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="b7acb-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b7acb-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="b7acb-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="b7acb-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

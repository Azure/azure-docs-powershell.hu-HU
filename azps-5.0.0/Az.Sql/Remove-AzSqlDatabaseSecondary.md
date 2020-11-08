---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 4353a61efd0141947879ad6795c321f5ed43e1d3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185821"
---
# <span data-ttu-id="70264-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="70264-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="70264-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70264-102">SYNOPSIS</span></span>
<span data-ttu-id="70264-103">Az SQL-adatbázis és a megadott másodlagos adatbázis közötti adatreplikáció megszüntetése</span><span class="sxs-lookup"><span data-stu-id="70264-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="70264-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70264-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70264-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="70264-105">DESCRIPTION</span></span>
<span data-ttu-id="70264-106">A **Remove-AzSqlDatabaseSecondary** parancsmag a Geo-replikációs hivatkozás megszüntetését kényszeríti.</span><span class="sxs-lookup"><span data-stu-id="70264-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="70264-107">Ez a parancsmag az Stop-AzSqlDatabaseCopy parancsmagot cseréli le.</span><span class="sxs-lookup"><span data-stu-id="70264-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="70264-108">A megszakítás előtt nincs replikációs szinkronizálás.</span><span class="sxs-lookup"><span data-stu-id="70264-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="70264-109">Példák</span><span class="sxs-lookup"><span data-stu-id="70264-109">EXAMPLES</span></span>

## <span data-ttu-id="70264-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70264-110">PARAMETERS</span></span>

### <span data-ttu-id="70264-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="70264-111">-DatabaseName</span></span>
<span data-ttu-id="70264-112">Annak az elsődleges Azure SQL-adatbázisnak a neve, amely a parancsmag által eltávolított replikációs hivatkozással rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="70264-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="70264-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70264-113">-DefaultProfile</span></span>
<span data-ttu-id="70264-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="70264-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70264-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70264-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="70264-116">A partner erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70264-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="70264-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="70264-117">-PartnerServerName</span></span>
<span data-ttu-id="70264-118">Adja meg a partner SQL-kiszolgálójának nevét.</span><span class="sxs-lookup"><span data-stu-id="70264-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="70264-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70264-119">-ResourceGroupName</span></span>
<span data-ttu-id="70264-120">Az eltávolítandó replikációs hivatkozással társított erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70264-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="70264-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="70264-121">-ServerName</span></span>
<span data-ttu-id="70264-122">Annak az SQL-kiszolgálónak a nevét adja meg, amelynek a replikációs hivatkozását el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="70264-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="70264-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70264-123">-Confirm</span></span>
<span data-ttu-id="70264-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70264-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70264-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70264-125">-WhatIf</span></span>
<span data-ttu-id="70264-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70264-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70264-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70264-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70264-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70264-128">CommonParameters</span></span>
<span data-ttu-id="70264-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70264-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70264-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="70264-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70264-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70264-131">INPUTS</span></span>

### <span data-ttu-id="70264-132">System. String</span><span class="sxs-lookup"><span data-stu-id="70264-132">System.String</span></span>

## <span data-ttu-id="70264-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70264-133">OUTPUTS</span></span>

### <span data-ttu-id="70264-134">Microsoft. Azure. Command. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="70264-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="70264-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70264-135">NOTES</span></span>

## <span data-ttu-id="70264-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70264-136">RELATED LINKS</span></span>

[<span data-ttu-id="70264-137">Új – AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="70264-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="70264-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="70264-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="70264-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="70264-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

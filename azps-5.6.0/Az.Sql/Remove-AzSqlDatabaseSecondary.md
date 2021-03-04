---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 566081ea78137c3816ecee58e76a4811c7f54f62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923298"
---
# <span data-ttu-id="c39d7-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c39d7-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="c39d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c39d7-102">SYNOPSIS</span></span>
<span data-ttu-id="c39d7-103">Az SQL-adatbázis és a megadott másodlagos adatbázis közötti adatreplikáció megszüntetése.</span><span class="sxs-lookup"><span data-stu-id="c39d7-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="c39d7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c39d7-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c39d7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c39d7-105">DESCRIPTION</span></span>
<span data-ttu-id="c39d7-106">A **Remove-AzSqlDatabaseSecondary** parancsmag egy georeplikációs kapcsolat megszüntetését kényszeríti.</span><span class="sxs-lookup"><span data-stu-id="c39d7-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="c39d7-107">Ez a parancsmag lecseréli a Stop-AzSqlDatabaseCopy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c39d7-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="c39d7-108">A megszüntetés előtt nincs replikációs szinkronizálás.</span><span class="sxs-lookup"><span data-stu-id="c39d7-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="c39d7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c39d7-109">EXAMPLES</span></span>

## <span data-ttu-id="c39d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c39d7-110">PARAMETERS</span></span>

### <span data-ttu-id="c39d7-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c39d7-111">-DatabaseName</span></span>
<span data-ttu-id="c39d7-112">Annak az elsődleges Azure SQL-adatbázisnak a nevét adja meg, amely a parancsmag által eltávolított replikációs hivatkozást használja.</span><span class="sxs-lookup"><span data-stu-id="c39d7-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c39d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c39d7-113">-DefaultProfile</span></span>
<span data-ttu-id="c39d7-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c39d7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c39d7-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c39d7-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c39d7-116">A partnererőforrás-csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39d7-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="c39d7-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="c39d7-117">-PartnerServerName</span></span>
<span data-ttu-id="c39d7-118">A partner SQL Server-kiszolgálójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39d7-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="c39d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c39d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="c39d7-120">Az eltávolítható replikációs hivatkozással társított erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c39d7-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="c39d7-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c39d7-121">-ServerName</span></span>
<span data-ttu-id="c39d7-122">Annak az SQL Servernek a nevét adja meg, amelyből el kell távolítani a replikációs hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="c39d7-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="c39d7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c39d7-123">-Confirm</span></span>
<span data-ttu-id="c39d7-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c39d7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c39d7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c39d7-125">-WhatIf</span></span>
<span data-ttu-id="c39d7-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c39d7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c39d7-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c39d7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c39d7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39d7-128">CommonParameters</span></span>
<span data-ttu-id="c39d7-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c39d7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c39d7-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c39d7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39d7-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c39d7-131">INPUTS</span></span>

### <span data-ttu-id="c39d7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c39d7-132">System.String</span></span>

## <span data-ttu-id="c39d7-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c39d7-133">OUTPUTS</span></span>

### <span data-ttu-id="c39d7-134">Microsoft.Azure.Commands.Sql.Replikáció.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="c39d7-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="c39d7-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c39d7-135">NOTES</span></span>

## <span data-ttu-id="c39d7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c39d7-136">RELATED LINKS</span></span>

[<span data-ttu-id="c39d7-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c39d7-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c39d7-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c39d7-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c39d7-139">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c39d7-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

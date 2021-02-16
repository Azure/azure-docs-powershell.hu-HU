---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144082"
---
# <span data-ttu-id="c04cd-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c04cd-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="c04cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c04cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c04cd-103">Eltávolít egy Azure SQL-adatbázis feladatátvételi csoportot.</span><span class="sxs-lookup"><span data-stu-id="c04cd-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="c04cd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c04cd-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c04cd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c04cd-105">DESCRIPTION</span></span>
<span data-ttu-id="c04cd-106">Ez a parancs eltávolítja a feladatátvételi csoportot a megadott néven, és az összes adatbázist és replikációs kapcsolatot érintetlenül hagyja.</span><span class="sxs-lookup"><span data-stu-id="c04cd-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="c04cd-107">A figyelő végpont nem lesz regisztrálva a DNS-ről.</span><span class="sxs-lookup"><span data-stu-id="c04cd-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="c04cd-108">A parancs végrehajtásához a feladatátvevő csoport elsődleges kiszolgálóját kell használni.</span><span class="sxs-lookup"><span data-stu-id="c04cd-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="c04cd-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c04cd-109">EXAMPLES</span></span>

### <span data-ttu-id="c04cd-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="c04cd-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="c04cd-111">Feladatátvételi csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="c04cd-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="c04cd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c04cd-112">PARAMETERS</span></span>

### <span data-ttu-id="c04cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c04cd-113">-DefaultProfile</span></span>
<span data-ttu-id="c04cd-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c04cd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c04cd-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="c04cd-115">-FailoverGroupName</span></span>
<span data-ttu-id="c04cd-116">Az eltávolítható Azure SQL-adatbázis feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c04cd-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="c04cd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c04cd-117">-Force</span></span>
<span data-ttu-id="c04cd-118">A művelet végrehajtásához hagyja ki a megerősítő üzenetet.</span><span class="sxs-lookup"><span data-stu-id="c04cd-118">Skip confirmation message for performing the action.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c04cd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c04cd-119">-ResourceGroupName</span></span>
<span data-ttu-id="c04cd-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c04cd-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="c04cd-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c04cd-121">-ServerName</span></span>
<span data-ttu-id="c04cd-122">A feladatátvételi csoport elsődleges Azure SQL Database Server-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="c04cd-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="c04cd-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c04cd-123">-Confirm</span></span>
<span data-ttu-id="c04cd-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c04cd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c04cd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c04cd-125">-WhatIf</span></span>
<span data-ttu-id="c04cd-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c04cd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c04cd-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c04cd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c04cd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c04cd-128">CommonParameters</span></span>
<span data-ttu-id="c04cd-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c04cd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c04cd-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c04cd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c04cd-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c04cd-131">INPUTS</span></span>

### <span data-ttu-id="c04cd-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c04cd-132">System.String</span></span>

## <span data-ttu-id="c04cd-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c04cd-133">OUTPUTS</span></span>

### <span data-ttu-id="c04cd-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c04cd-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="c04cd-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c04cd-135">NOTES</span></span>

## <span data-ttu-id="c04cd-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c04cd-136">RELATED LINKS</span></span>

[<span data-ttu-id="c04cd-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c04cd-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c04cd-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c04cd-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c04cd-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c04cd-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c04cd-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c04cd-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="c04cd-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c04cd-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="c04cd-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c04cd-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c04cd-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c04cd-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

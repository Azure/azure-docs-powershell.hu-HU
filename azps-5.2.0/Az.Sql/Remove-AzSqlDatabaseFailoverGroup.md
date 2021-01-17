---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352985"
---
# <span data-ttu-id="f477b-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f477b-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="f477b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f477b-102">SYNOPSIS</span></span>
<span data-ttu-id="f477b-103">Eltávolít egy Azure SQL-adatbázis feladatátvételi csoportot.</span><span class="sxs-lookup"><span data-stu-id="f477b-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="f477b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f477b-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f477b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f477b-105">DESCRIPTION</span></span>
<span data-ttu-id="f477b-106">Ez a parancs eltávolítja a feladatátvételi csoportot a megadott néven, és az összes adatbázist és replikációs kapcsolatot érintetlenül hagyja.</span><span class="sxs-lookup"><span data-stu-id="f477b-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="f477b-107">A figyelő végpont nem lesz regisztrálva a DNS-ről.</span><span class="sxs-lookup"><span data-stu-id="f477b-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="f477b-108">A feladatátvételi csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="f477b-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="f477b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f477b-109">EXAMPLES</span></span>

### <span data-ttu-id="f477b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="f477b-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="f477b-111">Feladatátvételi csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f477b-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="f477b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f477b-112">PARAMETERS</span></span>

### <span data-ttu-id="f477b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f477b-113">-DefaultProfile</span></span>
<span data-ttu-id="f477b-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f477b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f477b-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="f477b-115">-FailoverGroupName</span></span>
<span data-ttu-id="f477b-116">Az eltávolítható Azure SQL-adatbázis feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f477b-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="f477b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f477b-117">-Force</span></span>
<span data-ttu-id="f477b-118">Hagyja ki a művelet végrehajtásához szükséges megerősítő üzenetet.</span><span class="sxs-lookup"><span data-stu-id="f477b-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="f477b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f477b-119">-ResourceGroupName</span></span>
<span data-ttu-id="f477b-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f477b-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="f477b-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f477b-121">-ServerName</span></span>
<span data-ttu-id="f477b-122">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="f477b-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="f477b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f477b-123">-Confirm</span></span>
<span data-ttu-id="f477b-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f477b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f477b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f477b-125">-WhatIf</span></span>
<span data-ttu-id="f477b-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f477b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f477b-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f477b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f477b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f477b-128">CommonParameters</span></span>
<span data-ttu-id="f477b-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f477b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f477b-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f477b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f477b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f477b-131">INPUTS</span></span>

### <span data-ttu-id="f477b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f477b-132">System.String</span></span>

## <span data-ttu-id="f477b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f477b-133">OUTPUTS</span></span>

### <span data-ttu-id="f477b-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f477b-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="f477b-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f477b-135">NOTES</span></span>

## <span data-ttu-id="f477b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f477b-136">RELATED LINKS</span></span>

[<span data-ttu-id="f477b-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f477b-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f477b-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f477b-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f477b-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f477b-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f477b-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f477b-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="f477b-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f477b-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="f477b-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f477b-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f477b-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="f477b-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

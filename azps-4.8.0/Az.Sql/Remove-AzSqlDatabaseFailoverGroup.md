---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181335"
---
# <span data-ttu-id="dfcfe-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dfcfe-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="dfcfe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfcfe-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcfe-103">Egy Azure SQL-adatbázis feladatátvételi csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="dfcfe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfcfe-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfcfe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfcfe-105">DESCRIPTION</span></span>
<span data-ttu-id="dfcfe-106">Ez a parancs eltávolítja a megadott nevű feladatátvételi csoportot, így az összes adatbázis és replikációs kapcsolat érintetlen marad.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="dfcfe-107">A figyelő végpontját a rendszer nem regisztrálja a DNS-ből.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="dfcfe-108">A feladatátvevő csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="dfcfe-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dfcfe-109">EXAMPLES</span></span>

### <span data-ttu-id="dfcfe-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dfcfe-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="dfcfe-111">Feladatátvételi csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dfcfe-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="dfcfe-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfcfe-112">PARAMETERS</span></span>

### <span data-ttu-id="dfcfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcfe-113">-DefaultProfile</span></span>
<span data-ttu-id="dfcfe-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dfcfe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfcfe-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="dfcfe-115">-FailoverGroupName</span></span>
<span data-ttu-id="dfcfe-116">Az eltávolítani kívánt Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="dfcfe-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dfcfe-117">-Force</span></span>
<span data-ttu-id="dfcfe-118">A művelet elvégzésére vonatkozó megerősítési üzenet kihagyása.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="dfcfe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfcfe-119">-ResourceGroupName</span></span>
<span data-ttu-id="dfcfe-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="dfcfe-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="dfcfe-121">-ServerName</span></span>
<span data-ttu-id="dfcfe-122">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="dfcfe-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dfcfe-123">-Confirm</span></span>
<span data-ttu-id="dfcfe-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfcfe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfcfe-125">-WhatIf</span></span>
<span data-ttu-id="dfcfe-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfcfe-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfcfe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcfe-128">CommonParameters</span></span>
<span data-ttu-id="dfcfe-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfcfe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcfe-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dfcfe-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcfe-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfcfe-131">INPUTS</span></span>

### <span data-ttu-id="dfcfe-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dfcfe-132">System.String</span></span>

## <span data-ttu-id="dfcfe-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfcfe-133">OUTPUTS</span></span>

### <span data-ttu-id="dfcfe-134">Microsoft. Azure. Command. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="dfcfe-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="dfcfe-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfcfe-135">NOTES</span></span>

## <span data-ttu-id="dfcfe-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfcfe-136">RELATED LINKS</span></span>

[<span data-ttu-id="dfcfe-137">Új – AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dfcfe-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dfcfe-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dfcfe-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dfcfe-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dfcfe-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dfcfe-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dfcfe-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="dfcfe-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dfcfe-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="dfcfe-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dfcfe-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dfcfe-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="dfcfe-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

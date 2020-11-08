---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186636"
---
# <span data-ttu-id="3dec7-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3dec7-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="3dec7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3dec7-102">SYNOPSIS</span></span>
<span data-ttu-id="3dec7-103">Egy Azure SQL-adatbázis feladatátvételi csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3dec7-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="3dec7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3dec7-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3dec7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3dec7-105">DESCRIPTION</span></span>
<span data-ttu-id="3dec7-106">Ez a parancs eltávolítja a megadott nevű feladatátvételi csoportot, így az összes adatbázis és replikációs kapcsolat érintetlen marad.</span><span class="sxs-lookup"><span data-stu-id="3dec7-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="3dec7-107">A figyelő végpontját a rendszer nem regisztrálja a DNS-ből.</span><span class="sxs-lookup"><span data-stu-id="3dec7-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="3dec7-108">A feladatátvevő csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="3dec7-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="3dec7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3dec7-109">EXAMPLES</span></span>

### <span data-ttu-id="3dec7-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3dec7-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="3dec7-111">Feladatátvételi csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3dec7-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="3dec7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3dec7-112">PARAMETERS</span></span>

### <span data-ttu-id="3dec7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dec7-113">-DefaultProfile</span></span>
<span data-ttu-id="3dec7-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3dec7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3dec7-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="3dec7-115">-FailoverGroupName</span></span>
<span data-ttu-id="3dec7-116">Az eltávolítani kívánt Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3dec7-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="3dec7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3dec7-117">-Force</span></span>
<span data-ttu-id="3dec7-118">A művelet elvégzésére vonatkozó megerősítési üzenet kihagyása.</span><span class="sxs-lookup"><span data-stu-id="3dec7-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="3dec7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dec7-119">-ResourceGroupName</span></span>
<span data-ttu-id="3dec7-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3dec7-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="3dec7-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3dec7-121">-ServerName</span></span>
<span data-ttu-id="3dec7-122">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="3dec7-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="3dec7-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3dec7-123">-Confirm</span></span>
<span data-ttu-id="3dec7-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3dec7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dec7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dec7-125">-WhatIf</span></span>
<span data-ttu-id="3dec7-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3dec7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dec7-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3dec7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dec7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dec7-128">CommonParameters</span></span>
<span data-ttu-id="3dec7-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3dec7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dec7-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3dec7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dec7-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dec7-131">INPUTS</span></span>

### <span data-ttu-id="3dec7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3dec7-132">System.String</span></span>

## <span data-ttu-id="3dec7-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dec7-133">OUTPUTS</span></span>

### <span data-ttu-id="3dec7-134">Microsoft. Azure. Command. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="3dec7-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="3dec7-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3dec7-135">NOTES</span></span>

## <span data-ttu-id="3dec7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3dec7-136">RELATED LINKS</span></span>

[<span data-ttu-id="3dec7-137">Új – AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3dec7-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3dec7-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3dec7-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3dec7-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3dec7-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3dec7-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3dec7-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="3dec7-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3dec7-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="3dec7-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3dec7-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="3dec7-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="3dec7-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
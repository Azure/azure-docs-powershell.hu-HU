---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 40a193e96bdfa3c209a15e4a7be801e6ce71a3a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680762"
---
# <span data-ttu-id="35307-101">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="35307-101">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="35307-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35307-102">SYNOPSIS</span></span>
<span data-ttu-id="35307-103">Egy Azure SQL-adatbázis feladatátvételi csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="35307-103">Removes an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35307-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35307-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35307-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="35307-105">DESCRIPTION</span></span>
<span data-ttu-id="35307-106">Ez a parancs eltávolítja a megadott nevű feladatátvételi csoportot, így az összes adatbázis és replikációs kapcsolat érintetlen marad.</span><span class="sxs-lookup"><span data-stu-id="35307-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="35307-107">A figyelő végpontját a rendszer nem regisztrálja a DNS-ből.</span><span class="sxs-lookup"><span data-stu-id="35307-107">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="35307-108">A feladatátvevő csoport elsődleges kiszolgálóját kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="35307-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="35307-109">Példák</span><span class="sxs-lookup"><span data-stu-id="35307-109">EXAMPLES</span></span>

### <span data-ttu-id="35307-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="35307-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="35307-111">Feladatátvételi csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="35307-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="35307-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35307-112">PARAMETERS</span></span>

### <span data-ttu-id="35307-113">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="35307-113">-FailoverGroupName</span></span>
<span data-ttu-id="35307-114">Az eltávolítani kívánt Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="35307-114">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="35307-115">-Force</span><span class="sxs-lookup"><span data-stu-id="35307-115">-Force</span></span>
<span data-ttu-id="35307-116">A művelet elvégzésére vonatkozó megerősítési üzenet kihagyása.</span><span class="sxs-lookup"><span data-stu-id="35307-116">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="35307-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35307-117">-ResourceGroupName</span></span>
<span data-ttu-id="35307-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="35307-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="35307-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="35307-119">-ServerName</span></span>
<span data-ttu-id="35307-120">A feladatátvételi csoport elsődleges Azure SQL-adatbázis-kiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="35307-120">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="35307-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="35307-121">-Confirm</span></span>
<span data-ttu-id="35307-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="35307-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35307-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35307-123">-WhatIf</span></span>
<span data-ttu-id="35307-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="35307-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35307-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35307-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35307-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35307-126">-DefaultProfile</span></span>
<span data-ttu-id="35307-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35307-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35307-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35307-128">CommonParameters</span></span>
<span data-ttu-id="35307-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35307-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35307-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35307-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35307-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35307-131">INPUTS</span></span>

### <span data-ttu-id="35307-132">System. String</span><span class="sxs-lookup"><span data-stu-id="35307-132">System.String</span></span>

## <span data-ttu-id="35307-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35307-133">OUTPUTS</span></span>

### <span data-ttu-id="35307-134">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="35307-134">System.Object</span></span>

## <span data-ttu-id="35307-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35307-135">NOTES</span></span>

## <span data-ttu-id="35307-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35307-136">RELATED LINKS</span></span>

[<span data-ttu-id="35307-137">Új – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="35307-137">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="35307-138">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="35307-138">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="35307-139">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="35307-139">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="35307-140">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="35307-140">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="35307-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="35307-141">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="35307-142">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="35307-142">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="35307-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="35307-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

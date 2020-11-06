---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: db85c1f8de00432b3f9213473c89728239099c0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494890"
---
# <span data-ttu-id="cd3bb-101">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd3bb-101">Get-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="cd3bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd3bb-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3bb-103">Azure SQL adatbázis-feladatátvételi csoportok beolvasása vagy listázása.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd3bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd3bb-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd3bb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd3bb-105">DESCRIPTION</span></span>
<span data-ttu-id="cd3bb-106">Egy bizonyos Azure SQL-adatbázis feladatátvételi csoportjának beolvasása vagy a feladatátvételi csoportok listázása a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="cd3bb-107">Előfordulhat, hogy a feladatátvételi csoport kiszolgálója használható a parancs végrehajtására.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="cd3bb-108">A visszatérési értékek a megadott kiszolgáló állapotát tükrözik a feladatátvételi csoporttal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="cd3bb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cd3bb-109">EXAMPLES</span></span>

### <span data-ttu-id="cd3bb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cd3bb-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="cd3bb-111">A kiszolgálón lévő összes feladatátvételi csoport felsorolása.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="cd3bb-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="cd3bb-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="cd3bb-113">Adott feladatátvételi csoport beszerzése</span><span class="sxs-lookup"><span data-stu-id="cd3bb-113">Get a specific Failover Group.</span></span>

## <span data-ttu-id="cd3bb-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd3bb-114">PARAMETERS</span></span>

### <span data-ttu-id="cd3bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd3bb-115">-DefaultProfile</span></span>
<span data-ttu-id="cd3bb-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cd3bb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd3bb-117">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="cd3bb-117">-FailoverGroupName</span></span>
<span data-ttu-id="cd3bb-118">A lekérdezni kívánt Azure SQL adatbázis-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-118">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd3bb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd3bb-119">-ResourceGroupName</span></span>
<span data-ttu-id="cd3bb-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="cd3bb-121">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="cd3bb-121">-ServerName</span></span>
<span data-ttu-id="cd3bb-122">Annak az Azure SQL adatbázis-kiszolgálónak a neve, amelyből a feladatátvételi csoportot be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-122">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="cd3bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3bb-123">CommonParameters</span></span>
<span data-ttu-id="cd3bb-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd3bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3bb-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd3bb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3bb-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd3bb-126">INPUTS</span></span>

### <span data-ttu-id="cd3bb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cd3bb-127">System.String</span></span>

## <span data-ttu-id="cd3bb-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd3bb-128">OUTPUTS</span></span>

### <span data-ttu-id="cd3bb-129">Microsoft. Azure. Command. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="cd3bb-129">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="cd3bb-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd3bb-130">NOTES</span></span>

## <span data-ttu-id="cd3bb-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd3bb-131">RELATED LINKS</span></span>

[<span data-ttu-id="cd3bb-132">Új – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd3bb-132">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cd3bb-133">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd3bb-133">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cd3bb-134">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd3bb-134">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="cd3bb-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd3bb-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="cd3bb-136">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd3bb-136">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cd3bb-137">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cd3bb-137">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cd3bb-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="cd3bb-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

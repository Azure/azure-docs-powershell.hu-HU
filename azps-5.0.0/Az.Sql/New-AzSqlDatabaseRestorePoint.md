---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: d2dc1b6acf1978976ce29adea2e79146828accb1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186983"
---
# <span data-ttu-id="b2647-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="b2647-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="b2647-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2647-102">SYNOPSIS</span></span>
<span data-ttu-id="b2647-103">Új visszaállítási pont létrehozása, amelyből egy SQL-adatbázis visszaadható.</span><span class="sxs-lookup"><span data-stu-id="b2647-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="b2647-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2647-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2647-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2647-105">DESCRIPTION</span></span>
<span data-ttu-id="b2647-106">A **New-AzSqlDatabaseRestorePoint** parancsmag új visszaállítási pontot hoz létre, amelyet egy Azure SQL-adattárházból lehet visszaállítani.</span><span class="sxs-lookup"><span data-stu-id="b2647-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="b2647-107">Ez a parancsmag jelenleg az Azure SQL Data Warehouse alkalmazásban támogatott.</span><span class="sxs-lookup"><span data-stu-id="b2647-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="b2647-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b2647-108">EXAMPLES</span></span>

### <span data-ttu-id="b2647-109">Példa 1: visszaállítási pont létrehozása</span><span class="sxs-lookup"><span data-stu-id="b2647-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="b2647-110">A parancs létrehozza az Azure SQL-adattárház visszaállítási pontját, és a visszaállítási pont részleteit adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b2647-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="b2647-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2647-111">PARAMETERS</span></span>

### <span data-ttu-id="b2647-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b2647-112">-DatabaseName</span></span>
<span data-ttu-id="b2647-113">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2647-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="b2647-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2647-114">-DefaultProfile</span></span>
<span data-ttu-id="b2647-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b2647-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2647-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2647-116">-ResourceGroupName</span></span>
<span data-ttu-id="b2647-117">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b2647-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="b2647-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="b2647-118">-RestorePointLabel</span></span>
<span data-ttu-id="b2647-119">A visszaállítási pont címkét adja meg az egyszerű azonosításhoz.</span><span class="sxs-lookup"><span data-stu-id="b2647-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="b2647-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b2647-120">-ServerName</span></span>
<span data-ttu-id="b2647-121">Az adatbázist tároló AzureSQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2647-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="b2647-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b2647-122">-Confirm</span></span>
<span data-ttu-id="b2647-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b2647-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2647-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2647-124">-WhatIf</span></span>
<span data-ttu-id="b2647-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b2647-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2647-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b2647-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2647-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2647-127">CommonParameters</span></span>
<span data-ttu-id="b2647-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2647-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2647-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b2647-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2647-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2647-130">INPUTS</span></span>

### <span data-ttu-id="b2647-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b2647-131">System.String</span></span>

## <span data-ttu-id="b2647-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2647-132">OUTPUTS</span></span>

### <span data-ttu-id="b2647-133">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="b2647-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="b2647-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2647-134">NOTES</span></span>

## <span data-ttu-id="b2647-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2647-135">RELATED LINKS</span></span>
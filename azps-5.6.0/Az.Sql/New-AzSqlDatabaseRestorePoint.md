---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 8fb320c2caa4993b7880ef719a3d9ea0e0e8c811
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920906"
---
# <span data-ttu-id="74944-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="74944-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="74944-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74944-102">SYNOPSIS</span></span>
<span data-ttu-id="74944-103">Létrehoz egy új visszaállítási pontot, amelyből az SQL-adatbázis visszaállítható.</span><span class="sxs-lookup"><span data-stu-id="74944-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="74944-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="74944-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74944-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="74944-105">DESCRIPTION</span></span>
<span data-ttu-id="74944-106">A **New-AzSqlDatabaseRestorePoint** parancsmag létrehoz egy új visszaállítási pontot, amelyből az Azure SQL-adattárház visszaállítható.</span><span class="sxs-lookup"><span data-stu-id="74944-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="74944-107">Ez a parancsmag jelenleg az Azure SQL Data Warehouse szolgáltatásban támogatott.</span><span class="sxs-lookup"><span data-stu-id="74944-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="74944-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="74944-108">EXAMPLES</span></span>

### <span data-ttu-id="74944-109">1. példa: Visszaállítási pont létrehozása</span><span class="sxs-lookup"><span data-stu-id="74944-109">Example 1: Create a restore point</span></span>
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

<span data-ttu-id="74944-110">Ez a parancs létrehoz egy visszaállítási pontot az Azure SQL Data Warehouse számára, és visszaadja a visszaállítási pont részleteit.</span><span class="sxs-lookup"><span data-stu-id="74944-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="74944-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74944-111">PARAMETERS</span></span>

### <span data-ttu-id="74944-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="74944-112">-DatabaseName</span></span>
<span data-ttu-id="74944-113">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="74944-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="74944-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74944-114">-DefaultProfile</span></span>
<span data-ttu-id="74944-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="74944-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74944-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74944-116">-ResourceGroupName</span></span>
<span data-ttu-id="74944-117">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az SQL-adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="74944-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="74944-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="74944-118">-RestorePointLabel</span></span>
<span data-ttu-id="74944-119">A visszaállítási pont címkéjét adja meg az egyszerű azonosítás érdekében.</span><span class="sxs-lookup"><span data-stu-id="74944-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="74944-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="74944-120">-ServerName</span></span>
<span data-ttu-id="74944-121">Az adatbázist tartalmazó AzureSQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="74944-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="74944-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74944-122">-Confirm</span></span>
<span data-ttu-id="74944-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="74944-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74944-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74944-124">-WhatIf</span></span>
<span data-ttu-id="74944-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="74944-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74944-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74944-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74944-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74944-127">CommonParameters</span></span>
<span data-ttu-id="74944-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74944-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74944-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74944-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74944-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74944-130">INPUTS</span></span>

### <span data-ttu-id="74944-131">System.String</span><span class="sxs-lookup"><span data-stu-id="74944-131">System.String</span></span>

## <span data-ttu-id="74944-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74944-132">OUTPUTS</span></span>

### <span data-ttu-id="74944-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="74944-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="74944-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="74944-134">NOTES</span></span>

## <span data-ttu-id="74944-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74944-135">RELATED LINKS</span></span>

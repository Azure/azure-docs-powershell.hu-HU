---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 2e98f832bd13509a853d85037a413b6fd5895695
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467117"
---
# <span data-ttu-id="d8e50-101">Remove-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="d8e50-101">Remove-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="d8e50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8e50-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e50-103">A megadott visszaállítási pont eltávolítása az SQL-adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="d8e50-103">Removes given restore point from a SQL Database.</span></span>

## <span data-ttu-id="d8e50-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8e50-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8e50-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8e50-105">DESCRIPTION</span></span>
<span data-ttu-id="d8e50-106">A **Remove-AzSqlDatabaseRestorePoint** parancsmag eltávolítja a visszaállítási pontot az Azure SQL-adatbázisból.</span><span class="sxs-lookup"><span data-stu-id="d8e50-106">The **Remove-AzSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="d8e50-107">Ezt a parancsmagot jelenleg az SQL Server Datawarehouse szolgáltatás támogatja az Azure SQL-adatbázisban.</span><span class="sxs-lookup"><span data-stu-id="d8e50-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="d8e50-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8e50-108">EXAMPLES</span></span>

### <span data-ttu-id="d8e50-109">1. példa: Visszaállítási pont eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d8e50-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="d8e50-110">Ez a parancs eltávolítja az Azure SQL-adatbázis visszaállítási pontját a létrehozás adott dátumával.</span><span class="sxs-lookup"><span data-stu-id="d8e50-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="d8e50-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8e50-111">PARAMETERS</span></span>

### <span data-ttu-id="d8e50-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8e50-112">-DatabaseName</span></span>
<span data-ttu-id="d8e50-113">Az SQL-adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8e50-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="d8e50-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e50-114">-DefaultProfile</span></span>
<span data-ttu-id="d8e50-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d8e50-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8e50-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8e50-116">-PassThru</span></span>
<span data-ttu-id="d8e50-117">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d8e50-117">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e50-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e50-118">-ResourceGroupName</span></span>
<span data-ttu-id="d8e50-119">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az SQL-adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="d8e50-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="d8e50-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="d8e50-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="d8e50-121">A visszaállítási pont létrehozásának dátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8e50-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e50-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d8e50-122">-ServerName</span></span>
<span data-ttu-id="d8e50-123">Az adatbázist tartalmazó AzureSQL-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d8e50-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="d8e50-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8e50-124">-Confirm</span></span>
<span data-ttu-id="d8e50-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d8e50-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e50-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e50-126">-WhatIf</span></span>
<span data-ttu-id="d8e50-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d8e50-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e50-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8e50-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e50-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e50-129">CommonParameters</span></span>
<span data-ttu-id="d8e50-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e50-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e50-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8e50-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e50-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8e50-132">INPUTS</span></span>

### <span data-ttu-id="d8e50-133">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="d8e50-133">System.DateTime</span></span>

### <span data-ttu-id="d8e50-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d8e50-134">System.String</span></span>

## <span data-ttu-id="d8e50-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8e50-135">OUTPUTS</span></span>

### <span data-ttu-id="d8e50-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="d8e50-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="d8e50-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8e50-137">NOTES</span></span>

## <span data-ttu-id="d8e50-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8e50-138">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 07836205ec7311eadf7e48dd79b322d00670f337
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465995"
---
# <span data-ttu-id="212ab-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="212ab-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="212ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="212ab-102">SYNOPSIS</span></span>
<span data-ttu-id="212ab-103">Az adatbázis földrajzi biztonsági mentésének házirendet állít be.</span><span class="sxs-lookup"><span data-stu-id="212ab-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="212ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="212ab-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="212ab-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="212ab-105">DESCRIPTION</span></span>
<span data-ttu-id="212ab-106">A **Set-AzSqlDatabaseGeoBackupPolicy** parancsmag beállítja az adatbázishoz regisztrált geo backup házirendet.</span><span class="sxs-lookup"><span data-stu-id="212ab-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="212ab-107">Ez egy Azure biztonságimásolat-erőforrás, amely a biztonságimásolat-tárolási házirend meghatározására szolgál.</span><span class="sxs-lookup"><span data-stu-id="212ab-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="212ab-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="212ab-108">EXAMPLES</span></span>

## <span data-ttu-id="212ab-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="212ab-109">PARAMETERS</span></span>

### <span data-ttu-id="212ab-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="212ab-110">-DatabaseName</span></span>
<span data-ttu-id="212ab-111">Annak az adatbázisnak a nevét adja meg, amelyhez ez a parancsmag beállítja a földrajzi biztonsági mentési házirendet.</span><span class="sxs-lookup"><span data-stu-id="212ab-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="212ab-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="212ab-112">-DefaultProfile</span></span>
<span data-ttu-id="212ab-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="212ab-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="212ab-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="212ab-114">-ResourceGroupName</span></span>
<span data-ttu-id="212ab-115">Az adatbázist tartalmazó kiszolgáló erőforráscsoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="212ab-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="212ab-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="212ab-116">-ServerName</span></span>
<span data-ttu-id="212ab-117">Az adatbázist tartalmazó kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="212ab-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="212ab-118">-State</span><span class="sxs-lookup"><span data-stu-id="212ab-118">-State</span></span>
<span data-ttu-id="212ab-119">A földrajzi biztonsági mentési házirend állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="212ab-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="212ab-120">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="212ab-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="212ab-121">Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="212ab-121">Enabled</span></span> 
- <span data-ttu-id="212ab-122">Letiltva</span><span class="sxs-lookup"><span data-stu-id="212ab-122">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212ab-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="212ab-123">-Confirm</span></span>
<span data-ttu-id="212ab-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="212ab-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="212ab-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="212ab-125">-WhatIf</span></span>
<span data-ttu-id="212ab-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="212ab-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="212ab-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="212ab-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="212ab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="212ab-128">CommonParameters</span></span>
<span data-ttu-id="212ab-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="212ab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="212ab-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="212ab-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="212ab-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="212ab-131">INPUTS</span></span>

### <span data-ttu-id="212ab-132">System.String</span><span class="sxs-lookup"><span data-stu-id="212ab-132">System.String</span></span>

## <span data-ttu-id="212ab-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="212ab-133">OUTPUTS</span></span>

### <span data-ttu-id="212ab-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="212ab-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="212ab-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="212ab-135">NOTES</span></span>

## <span data-ttu-id="212ab-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="212ab-136">RELATED LINKS</span></span>

[<span data-ttu-id="212ab-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="212ab-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="212ab-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="212ab-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


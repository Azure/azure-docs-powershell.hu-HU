---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: caca08a5a9390d3e80fdef8309244a8a4d29aec0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181338"
---
# <span data-ttu-id="508ad-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="508ad-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="508ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="508ad-102">SYNOPSIS</span></span>
<span data-ttu-id="508ad-103">Egy Azure SQL-adatbázis naplózási beállításainak eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="508ad-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="508ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="508ad-104">SYNTAX</span></span>

### <span data-ttu-id="508ad-105">DatabaseParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="508ad-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="508ad-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="508ad-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="508ad-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="508ad-107">DESCRIPTION</span></span>
<span data-ttu-id="508ad-108">A **Remove-AzSqlDatabaseAudit** parancsmag eltávolítja az Azure SQL-adatbázisok naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="508ad-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="508ad-109">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="508ad-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="508ad-110">Példák</span><span class="sxs-lookup"><span data-stu-id="508ad-110">EXAMPLES</span></span>

### <span data-ttu-id="508ad-111">1. példa: az Azure SQL-adatbázisok naplózási beállításainak eltávolítása</span><span class="sxs-lookup"><span data-stu-id="508ad-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="508ad-112">2. példa: az Azure SQL-adatbázisok naplózási beállításainak eltávolítása a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="508ad-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="508ad-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="508ad-113">PARAMETERS</span></span>

### <span data-ttu-id="508ad-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="508ad-114">-DatabaseName</span></span>
<span data-ttu-id="508ad-115">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="508ad-115">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="508ad-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="508ad-116">-DatabaseObject</span></span>
<span data-ttu-id="508ad-117">Az adatbázis-objektum a naplózási házirend kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="508ad-117">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="508ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="508ad-118">-DefaultProfile</span></span>
<span data-ttu-id="508ad-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="508ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="508ad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="508ad-120">-ResourceGroupName</span></span>
<span data-ttu-id="508ad-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="508ad-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="508ad-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="508ad-122">-ServerName</span></span>
<span data-ttu-id="508ad-123">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="508ad-123">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="508ad-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="508ad-124">-Confirm</span></span>
<span data-ttu-id="508ad-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="508ad-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="508ad-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="508ad-126">-WhatIf</span></span>
<span data-ttu-id="508ad-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="508ad-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="508ad-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="508ad-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="508ad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="508ad-129">CommonParameters</span></span>
<span data-ttu-id="508ad-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="508ad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="508ad-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="508ad-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="508ad-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="508ad-132">INPUTS</span></span>

### <span data-ttu-id="508ad-133">System. String</span><span class="sxs-lookup"><span data-stu-id="508ad-133">System.String</span></span>

### <span data-ttu-id="508ad-134">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="508ad-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="508ad-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="508ad-135">OUTPUTS</span></span>

### <span data-ttu-id="508ad-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="508ad-136">System.Boolean</span></span>

## <span data-ttu-id="508ad-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="508ad-137">NOTES</span></span>

## <span data-ttu-id="508ad-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="508ad-138">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: e53857533770d6de0040d2d777020f1a2f9f320a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168714"
---
# <span data-ttu-id="13aaf-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="13aaf-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="13aaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="13aaf-103">Szolgáltatás-célkitűzéseit kapja egy Azure SQL-adatbázis-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="13aaf-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="13aaf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13aaf-104">SYNTAX</span></span>

### <span data-ttu-id="13aaf-105">ByLocation (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13aaf-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13aaf-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="13aaf-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13aaf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13aaf-107">DESCRIPTION</span></span>
<span data-ttu-id="13aaf-108">A **Get-AzSqlServerServiceObjective** parancsmag megkapja az Azure SQL Database-kiszolgálóhoz elérhető szolgáltatási célokat.</span><span class="sxs-lookup"><span data-stu-id="13aaf-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="13aaf-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13aaf-109">EXAMPLES</span></span>

### <span data-ttu-id="13aaf-110">1. példa: Szolgáltatási célok elérése</span><span class="sxs-lookup"><span data-stu-id="13aaf-110">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="13aaf-111">Ez a parancs a Kiszolgáló01 nevű kiszolgáló szolgáltatási céljait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="13aaf-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="13aaf-112">2. példa: Szolgáltatásra vonatkozó célok elérése szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="13aaf-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="13aaf-113">Ez a parancs a "Rendszer" kezdetű Kiszolgáló01 kiszolgáló szolgáltatási céljait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="13aaf-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="13aaf-114">3. példa: Szolgáltatási célok lekérte egy helyhez</span><span class="sxs-lookup"><span data-stu-id="13aaf-114">Example 3: Get service objectives for a location</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -Location "west us"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="13aaf-115">Ez a parancs egy adott Azure-régió szolgáltatási céljait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="13aaf-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="13aaf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13aaf-116">PARAMETERS</span></span>

### <span data-ttu-id="13aaf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13aaf-117">-DefaultProfile</span></span>
<span data-ttu-id="13aaf-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="13aaf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13aaf-119">-Location</span><span class="sxs-lookup"><span data-stu-id="13aaf-119">-Location</span></span>
<span data-ttu-id="13aaf-120">Annak a helynek a neve, amelynek a szolgáltatásra vonatkozó célkitűzéseit ki kell kapnia.</span><span class="sxs-lookup"><span data-stu-id="13aaf-120">The name of the Location for which to get the service objectives.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13aaf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13aaf-121">-ResourceGroupName</span></span>
<span data-ttu-id="13aaf-122">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13aaf-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="13aaf-123">Ez a parancsmag az erőforráshoz hozzárendelt SQL-adatbázis-kiszolgáló szolgáltatási céljait kapja.</span><span class="sxs-lookup"><span data-stu-id="13aaf-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13aaf-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="13aaf-124">-ServerName</span></span>
<span data-ttu-id="13aaf-125">Az SQL-adatbázis SQL-adatbázis-kiszolgálójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13aaf-125">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13aaf-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="13aaf-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="13aaf-127">Egy Azure SQL-adatbázis-kiszolgáló szolgáltatási céljának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13aaf-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="13aaf-128">A paraméter elfogadható értékei: Basic, S0, S1, S2, P1, P2 és P3.</span><span class="sxs-lookup"><span data-stu-id="13aaf-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="13aaf-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13aaf-129">-Confirm</span></span>
<span data-ttu-id="13aaf-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="13aaf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13aaf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13aaf-131">-WhatIf</span></span>
<span data-ttu-id="13aaf-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="13aaf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13aaf-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13aaf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13aaf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13aaf-134">CommonParameters</span></span>
<span data-ttu-id="13aaf-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13aaf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13aaf-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13aaf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13aaf-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13aaf-137">INPUTS</span></span>

### <span data-ttu-id="13aaf-138">System.String</span><span class="sxs-lookup"><span data-stu-id="13aaf-138">System.String</span></span>

## <span data-ttu-id="13aaf-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13aaf-139">OUTPUTS</span></span>

### <span data-ttu-id="13aaf-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="13aaf-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="13aaf-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13aaf-141">NOTES</span></span>

## <span data-ttu-id="13aaf-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13aaf-142">RELATED LINKS</span></span>

[<span data-ttu-id="13aaf-143">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="13aaf-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



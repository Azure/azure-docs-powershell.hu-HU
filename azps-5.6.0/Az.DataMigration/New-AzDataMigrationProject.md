---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: 158ae87c636f0ecf8b8c78d2a6d380640ff49677
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928633"
---
# <span data-ttu-id="12d60-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="12d60-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="12d60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12d60-102">SYNOPSIS</span></span>
<span data-ttu-id="12d60-103">Létrehoz egy új Azure Database Migration Service-projektet.</span><span class="sxs-lookup"><span data-stu-id="12d60-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="12d60-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="12d60-104">SYNTAX</span></span>

### <span data-ttu-id="12d60-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12d60-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12d60-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12d60-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12d60-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12d60-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12d60-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="12d60-108">DESCRIPTION</span></span>
<span data-ttu-id="12d60-109">A New-AzDataMigrationProject parancsmag létrehoz egy új Azure Database Migration Service-projektet.</span><span class="sxs-lookup"><span data-stu-id="12d60-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="12d60-110">Ez a parancsmag az összes szükséges paramétert beveszi, például az Azure Resource Group nevét, az új projekthez szükséges Azure-adatáttelepítési szolgáltatás nevét, a projekt létrehozási régióját, az új projekt egyedi nevét, a forrás- és célkapcsolat-objektumokat, valamint a céltípus-objektumot az áttűnni szükséges adatbázisok listájának bemeneteként.</span><span class="sxs-lookup"><span data-stu-id="12d60-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="12d60-111">A New-AzDataMigrationConnectionInfo parancsmag használatával új ConnectionInfo-objektumot hozhat létre a forrás- és célkapcsolatok számára.</span><span class="sxs-lookup"><span data-stu-id="12d60-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="12d60-112">A Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo lista a kijelölt adatbázisok esetében várható; ez az objektum egy parancsmag használatával New-AzDataMigrationDatabaseInfo létre.</span><span class="sxs-lookup"><span data-stu-id="12d60-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="12d60-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="12d60-113">EXAMPLES</span></span>

### <span data-ttu-id="12d60-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="12d60-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="12d60-115">A fenti példa azt mutatja be, hogy miként hozhat létre egy MyDMSProject nevű új projektet, amely közép-amerikai régióban található a TestService nevű Azure Database Migration Service példányban.</span><span class="sxs-lookup"><span data-stu-id="12d60-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="12d60-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12d60-116">PARAMETERS</span></span>

### <span data-ttu-id="12d60-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="12d60-117">-DatabaseInfo</span></span>
<span data-ttu-id="12d60-118">Adatbázisadatok.</span><span class="sxs-lookup"><span data-stu-id="12d60-118">Database Infos.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d60-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d60-119">-DefaultProfile</span></span>
<span data-ttu-id="12d60-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12d60-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12d60-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12d60-121">-InputObject</span></span>
<span data-ttu-id="12d60-122">PSDataMigrationService objektum.</span><span class="sxs-lookup"><span data-stu-id="12d60-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12d60-123">-Location</span><span class="sxs-lookup"><span data-stu-id="12d60-123">-Location</span></span>
<span data-ttu-id="12d60-124">Az Azure Database Migration Service-példány helye.</span><span class="sxs-lookup"><span data-stu-id="12d60-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d60-125">-Name</span><span class="sxs-lookup"><span data-stu-id="12d60-125">-Name</span></span>
<span data-ttu-id="12d60-126">A projekt neve.</span><span class="sxs-lookup"><span data-stu-id="12d60-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d60-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d60-127">-ResourceGroupName</span></span>
<span data-ttu-id="12d60-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="12d60-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d60-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12d60-129">-ResourceId</span></span>
<span data-ttu-id="12d60-130">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="12d60-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12d60-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="12d60-131">-ServiceName</span></span>
<span data-ttu-id="12d60-132">Az Azure Database Migration Service példány neve.</span><span class="sxs-lookup"><span data-stu-id="12d60-132">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d60-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="12d60-133">-SourceConnection</span></span>
<span data-ttu-id="12d60-134">Forráskapcsolat adatai adatokat.</span><span class="sxs-lookup"><span data-stu-id="12d60-134">Source Connection Info.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d60-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="12d60-135">-SourceType</span></span>
<span data-ttu-id="12d60-136">A projekt forrásplatform-típusa.</span><span class="sxs-lookup"><span data-stu-id="12d60-136">Source platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d60-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="12d60-137">-TargetConnection</span></span>
<span data-ttu-id="12d60-138">Célkapcsolat adatai.</span><span class="sxs-lookup"><span data-stu-id="12d60-138">Target connection information.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d60-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="12d60-139">-TargetType</span></span>
<span data-ttu-id="12d60-140">A projekt célplatform-típusa.</span><span class="sxs-lookup"><span data-stu-id="12d60-140">Target platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d60-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12d60-141">-Confirm</span></span>
<span data-ttu-id="12d60-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="12d60-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12d60-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12d60-143">-WhatIf</span></span>
<span data-ttu-id="12d60-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="12d60-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12d60-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12d60-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12d60-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d60-146">CommonParameters</span></span>
<span data-ttu-id="12d60-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d60-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d60-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d60-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d60-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12d60-149">INPUTS</span></span>

### <span data-ttu-id="12d60-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="12d60-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="12d60-151">System.String</span><span class="sxs-lookup"><span data-stu-id="12d60-151">System.String</span></span>

## <span data-ttu-id="12d60-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12d60-152">OUTPUTS</span></span>

### <span data-ttu-id="12d60-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="12d60-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="12d60-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="12d60-154">NOTES</span></span>

## <span data-ttu-id="12d60-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12d60-155">RELATED LINKS</span></span>

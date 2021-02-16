---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: a496bd4ba68d9d62bdfe65dc293c68377b7d3aa6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155266"
---
# <span data-ttu-id="a4af6-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a4af6-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="a4af6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4af6-102">SYNOPSIS</span></span>
<span data-ttu-id="a4af6-103">Eltávolít egy Azure SQL Managed Instance-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="a4af6-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="a4af6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a4af6-104">SYNTAX</span></span>

### <span data-ttu-id="a4af6-105">RemoveInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4af6-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4af6-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="a4af6-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4af6-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="a4af6-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4af6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a4af6-108">DESCRIPTION</span></span>
<span data-ttu-id="a4af6-109">A **Remove-AzSqlInstanceDatabase** parancsmag eltávolít egy Azure SQL Managed Instance-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="a4af6-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="a4af6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a4af6-110">EXAMPLES</span></span>

### <span data-ttu-id="a4af6-111">1. példa: Adatbázis eltávolítása egy példányból</span><span class="sxs-lookup"><span data-stu-id="a4af6-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a4af6-112">Ez a parancs eltávolítja a Database01 nevű adatbázist a példány managedInstance1 példányból.</span><span class="sxs-lookup"><span data-stu-id="a4af6-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="a4af6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4af6-113">PARAMETERS</span></span>

### <span data-ttu-id="a4af6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4af6-114">-DefaultProfile</span></span>
<span data-ttu-id="a4af6-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4af6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4af6-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a4af6-116">-Force</span></span>
<span data-ttu-id="a4af6-117">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="a4af6-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a4af6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4af6-118">-InputObject</span></span>
<span data-ttu-id="a4af6-119">Az eltávolítható Példányadatbázis-objektum</span><span class="sxs-lookup"><span data-stu-id="a4af6-119">The Instance Database object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4af6-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a4af6-120">-InstanceName</span></span>
<span data-ttu-id="a4af6-121">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="a4af6-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4af6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a4af6-122">-Name</span></span>
<span data-ttu-id="a4af6-123">Az eltávolítható Azure SQL-példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a4af6-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4af6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4af6-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4af6-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4af6-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4af6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4af6-126">-ResourceId</span></span>
<span data-ttu-id="a4af6-127">Az eltávolítható Példányadatbázis-objektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a4af6-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4af6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4af6-128">-Confirm</span></span>
<span data-ttu-id="a4af6-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a4af6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4af6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4af6-130">-WhatIf</span></span>
<span data-ttu-id="a4af6-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a4af6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4af6-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4af6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4af6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4af6-133">CommonParameters</span></span>
<span data-ttu-id="a4af6-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4af6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4af6-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4af6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4af6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4af6-136">INPUTS</span></span>

### <span data-ttu-id="a4af6-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a4af6-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="a4af6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a4af6-138">System.String</span></span>

## <span data-ttu-id="a4af6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4af6-139">OUTPUTS</span></span>

### <span data-ttu-id="a4af6-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a4af6-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="a4af6-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a4af6-141">NOTES</span></span>

## <span data-ttu-id="a4af6-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4af6-142">RELATED LINKS</span></span>

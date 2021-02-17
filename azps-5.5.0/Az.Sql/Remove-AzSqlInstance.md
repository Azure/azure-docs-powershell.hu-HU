---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156155"
---
# <span data-ttu-id="9ac81-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9ac81-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="9ac81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ac81-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac81-103">Eltávolít egy Azure SQL Felügyelt adatbázis-példányt.</span><span class="sxs-lookup"><span data-stu-id="9ac81-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="9ac81-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9ac81-104">SYNTAX</span></span>

### <span data-ttu-id="9ac81-105">RemoveInstanceFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9ac81-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ac81-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="9ac81-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ac81-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="9ac81-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ac81-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9ac81-108">DESCRIPTION</span></span>
<span data-ttu-id="9ac81-109">A **Remove-AzSqlInstance** parancsmag eltávolítja az Azure SQL-adatbázis felügyelt példányát.</span><span class="sxs-lookup"><span data-stu-id="9ac81-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="9ac81-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9ac81-110">EXAMPLES</span></span>

### <span data-ttu-id="9ac81-111">1. példa: Példány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9ac81-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9ac81-112">Ez a parancs eltávolítja a managedInstance1 nevű példányt.</span><span class="sxs-lookup"><span data-stu-id="9ac81-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="9ac81-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ac81-113">PARAMETERS</span></span>

### <span data-ttu-id="9ac81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac81-114">-DefaultProfile</span></span>
<span data-ttu-id="9ac81-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ac81-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ac81-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9ac81-116">-Force</span></span>
<span data-ttu-id="9ac81-117">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="9ac81-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9ac81-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ac81-118">-InputObject</span></span>
<span data-ttu-id="9ac81-119">Az eltávolítható AzureSqlManagedInstanceModel objektum</span><span class="sxs-lookup"><span data-stu-id="9ac81-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac81-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9ac81-120">-Name</span></span>
<span data-ttu-id="9ac81-121">SQL-példány neve.</span><span class="sxs-lookup"><span data-stu-id="9ac81-121">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ac81-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ac81-122">-ResourceGroupName</span></span>
<span data-ttu-id="9ac81-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9ac81-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ac81-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ac81-124">-ResourceId</span></span>
<span data-ttu-id="9ac81-125">Az eltávolítható példányobjektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="9ac81-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac81-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ac81-126">-Confirm</span></span>
<span data-ttu-id="9ac81-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9ac81-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ac81-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ac81-128">-WhatIf</span></span>
<span data-ttu-id="9ac81-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9ac81-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ac81-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ac81-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ac81-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac81-131">CommonParameters</span></span>
<span data-ttu-id="9ac81-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ac81-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac81-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ac81-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac81-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ac81-134">INPUTS</span></span>

### <span data-ttu-id="9ac81-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="9ac81-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="9ac81-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9ac81-136">System.String</span></span>

## <span data-ttu-id="9ac81-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ac81-137">OUTPUTS</span></span>

### <span data-ttu-id="9ac81-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="9ac81-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="9ac81-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9ac81-139">NOTES</span></span>

## <span data-ttu-id="9ac81-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ac81-140">RELATED LINKS</span></span>

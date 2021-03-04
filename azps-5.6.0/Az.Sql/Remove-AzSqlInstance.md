---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: a8985d77ba1bbf33e49f353ad39d287f7bd3979b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920193"
---
# <span data-ttu-id="d7023-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d7023-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="d7023-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7023-102">SYNOPSIS</span></span>
<span data-ttu-id="d7023-103">Eltávolít egy Azure SQL Felügyelt adatbázis-példányt.</span><span class="sxs-lookup"><span data-stu-id="d7023-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="d7023-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d7023-104">SYNTAX</span></span>

### <span data-ttu-id="d7023-105">RemoveInstanceFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7023-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7023-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d7023-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7023-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="d7023-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7023-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d7023-108">DESCRIPTION</span></span>
<span data-ttu-id="d7023-109">A **Remove-AzSqlInstance** parancsmag eltávolít egy Azure SQL-adatbázis felügyelt példányát.</span><span class="sxs-lookup"><span data-stu-id="d7023-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="d7023-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d7023-110">EXAMPLES</span></span>

### <span data-ttu-id="d7023-111">1. példa: Példány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d7023-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d7023-112">Ez a parancs eltávolítja a managedInstance1 nevű példányt.</span><span class="sxs-lookup"><span data-stu-id="d7023-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="d7023-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7023-113">PARAMETERS</span></span>

### <span data-ttu-id="d7023-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7023-114">-DefaultProfile</span></span>
<span data-ttu-id="d7023-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7023-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7023-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d7023-116">-Force</span></span>
<span data-ttu-id="d7023-117">A művelet végrehajtásához szükséges megerősítő üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="d7023-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d7023-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7023-118">-InputObject</span></span>
<span data-ttu-id="d7023-119">Az eltávolítható AzureSqlManagedInstanceModel objektum</span><span class="sxs-lookup"><span data-stu-id="d7023-119">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="d7023-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d7023-120">-Name</span></span>
<span data-ttu-id="d7023-121">SQL-példány neve.</span><span class="sxs-lookup"><span data-stu-id="d7023-121">SQL instance name.</span></span>

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

### <span data-ttu-id="d7023-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7023-122">-ResourceGroupName</span></span>
<span data-ttu-id="d7023-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d7023-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="d7023-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7023-124">-ResourceId</span></span>
<span data-ttu-id="d7023-125">Az eltávolítható példányobjektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d7023-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="d7023-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7023-126">-Confirm</span></span>
<span data-ttu-id="d7023-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d7023-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7023-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7023-128">-WhatIf</span></span>
<span data-ttu-id="d7023-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d7023-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7023-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7023-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7023-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7023-131">CommonParameters</span></span>
<span data-ttu-id="d7023-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7023-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7023-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7023-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7023-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7023-134">INPUTS</span></span>

### <span data-ttu-id="d7023-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d7023-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="d7023-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d7023-136">System.String</span></span>

## <span data-ttu-id="d7023-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7023-137">OUTPUTS</span></span>

### <span data-ttu-id="d7023-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d7023-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="d7023-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d7023-139">NOTES</span></span>

## <span data-ttu-id="d7023-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7023-140">RELATED LINKS</span></span>

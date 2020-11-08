---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: a496bd4ba68d9d62bdfe65dc293c68377b7d3aa6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012809"
---
# <span data-ttu-id="1dad4-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1dad4-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="1dad4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1dad4-102">SYNOPSIS</span></span>
<span data-ttu-id="1dad4-103">Egy Azure SQL Managed instance-adatbázis eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1dad4-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="1dad4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1dad4-104">SYNTAX</span></span>

### <span data-ttu-id="1dad4-105">RemoveInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1dad4-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dad4-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="1dad4-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dad4-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="1dad4-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dad4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1dad4-108">DESCRIPTION</span></span>
<span data-ttu-id="1dad4-109">A **Remove-AzSqlInstanceDatabase** parancsmag eltávolítja az Azure SQL-alapú felügyelt példányok adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="1dad4-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="1dad4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1dad4-110">EXAMPLES</span></span>

### <span data-ttu-id="1dad4-111">1. példa: adatbázis eltávolítása egy példányból</span><span class="sxs-lookup"><span data-stu-id="1dad4-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1dad4-112">Ez a parancs eltávolítja a Database01 nevű adatbázist a példány managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="1dad4-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="1dad4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1dad4-113">PARAMETERS</span></span>

### <span data-ttu-id="1dad4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dad4-114">-DefaultProfile</span></span>
<span data-ttu-id="1dad4-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1dad4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dad4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1dad4-116">-Force</span></span>
<span data-ttu-id="1dad4-117">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="1dad4-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1dad4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dad4-118">-InputObject</span></span>
<span data-ttu-id="1dad4-119">Az eltávolítani kívánt példány adatbázis-objektuma</span><span class="sxs-lookup"><span data-stu-id="1dad4-119">The Instance Database object to remove</span></span>

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

### <span data-ttu-id="1dad4-120">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="1dad4-120">-InstanceName</span></span>
<span data-ttu-id="1dad4-121">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="1dad4-121">The instance name.</span></span>

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

### <span data-ttu-id="1dad4-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1dad4-122">-Name</span></span>
<span data-ttu-id="1dad4-123">Az eltávolítani kívánt Azure SQL-példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="1dad4-123">The name of the Azure SQL Instance Database to remove.</span></span>

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

### <span data-ttu-id="1dad4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dad4-124">-ResourceGroupName</span></span>
<span data-ttu-id="1dad4-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1dad4-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="1dad4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dad4-126">-ResourceId</span></span>
<span data-ttu-id="1dad4-127">Az eltávolítandó adatbázis-objektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1dad4-127">The resource id of Instance Database object to remove</span></span>

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

### <span data-ttu-id="1dad4-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1dad4-128">-Confirm</span></span>
<span data-ttu-id="1dad4-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1dad4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dad4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dad4-130">-WhatIf</span></span>
<span data-ttu-id="1dad4-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1dad4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dad4-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1dad4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dad4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dad4-133">CommonParameters</span></span>
<span data-ttu-id="1dad4-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1dad4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dad4-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1dad4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dad4-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1dad4-136">INPUTS</span></span>

### <span data-ttu-id="1dad4-137">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1dad4-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="1dad4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1dad4-138">System.String</span></span>

## <span data-ttu-id="1dad4-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1dad4-139">OUTPUTS</span></span>

### <span data-ttu-id="1dad4-140">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1dad4-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="1dad4-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1dad4-141">NOTES</span></span>

## <span data-ttu-id="1dad4-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1dad4-142">RELATED LINKS</span></span>

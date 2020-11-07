---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: 09aa7daaa3a583e42481e29675a08e8e1dd94d3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839116"
---
# <span data-ttu-id="8e9c1-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8e9c1-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="8e9c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e9c1-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9c1-103">Az Azure SQL felügyelt adatbázis-példány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8e9c1-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="8e9c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e9c1-104">SYNTAX</span></span>

### <span data-ttu-id="8e9c1-105">RemoveInstanceFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e9c1-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e9c1-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="8e9c1-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e9c1-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="8e9c1-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e9c1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e9c1-108">DESCRIPTION</span></span>
<span data-ttu-id="8e9c1-109">A **Remove-AzSqlInstance** parancsmag eltávolítja az Azure SQL-adatbázis felügyelt példányát.</span><span class="sxs-lookup"><span data-stu-id="8e9c1-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="8e9c1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8e9c1-110">EXAMPLES</span></span>

### <span data-ttu-id="8e9c1-111">Példa 1: példány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8e9c1-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8e9c1-112">Ez a parancs eltávolítja a managedInstance1 nevű példányt.</span><span class="sxs-lookup"><span data-stu-id="8e9c1-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="8e9c1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e9c1-113">PARAMETERS</span></span>

### <span data-ttu-id="8e9c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9c1-114">-DefaultProfile</span></span>
<span data-ttu-id="8e9c1-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e9c1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e9c1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8e9c1-116">-Force</span></span>
<span data-ttu-id="8e9c1-117">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="8e9c1-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="8e9c1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e9c1-118">-InputObject</span></span>
<span data-ttu-id="8e9c1-119">Az eltávolítandó AzureSqlManagedInstanceModel objektum</span><span class="sxs-lookup"><span data-stu-id="8e9c1-119">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="8e9c1-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e9c1-120">-Name</span></span>
<span data-ttu-id="8e9c1-121">SQL-példány neve</span><span class="sxs-lookup"><span data-stu-id="8e9c1-121">SQL instance name.</span></span>

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

### <span data-ttu-id="8e9c1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e9c1-122">-ResourceGroupName</span></span>
<span data-ttu-id="8e9c1-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8e9c1-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="8e9c1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e9c1-124">-ResourceId</span></span>
<span data-ttu-id="8e9c1-125">Az eltávolítandó példány-objektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8e9c1-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="8e9c1-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e9c1-126">-Confirm</span></span>
<span data-ttu-id="8e9c1-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e9c1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e9c1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e9c1-128">-WhatIf</span></span>
<span data-ttu-id="8e9c1-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e9c1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e9c1-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e9c1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e9c1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9c1-131">CommonParameters</span></span>
<span data-ttu-id="8e9c1-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e9c1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9c1-133">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8e9c1-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9c1-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e9c1-134">INPUTS</span></span>

### <span data-ttu-id="8e9c1-135">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="8e9c1-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="8e9c1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8e9c1-136">System.String</span></span>

## <span data-ttu-id="8e9c1-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e9c1-137">OUTPUTS</span></span>

### <span data-ttu-id="8e9c1-138">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="8e9c1-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="8e9c1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e9c1-139">NOTES</span></span>

## <span data-ttu-id="8e9c1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e9c1-140">RELATED LINKS</span></span>

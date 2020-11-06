---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: f391dbb5d3e70e486a91c1dbb9e6517936bd2b3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501959"
---
# <span data-ttu-id="17e79-101">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="17e79-101">Remove-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="17e79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="17e79-102">SYNOPSIS</span></span>
<span data-ttu-id="17e79-103">Egy Azure SQL Managed instance-adatbázis eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="17e79-103">Removes an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17e79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="17e79-104">SYNTAX</span></span>

### <span data-ttu-id="17e79-105">RemoveInstanceDatabaseFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="17e79-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzureRmSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17e79-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="17e79-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzureRmSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17e79-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="17e79-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzureRmSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17e79-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="17e79-108">DESCRIPTION</span></span>
<span data-ttu-id="17e79-109">A **Remove-AzureRmSqlInstanceDatabase** parancsmag eltávolítja az Azure SQL-alapú felügyelt példányok adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="17e79-109">The **Remove-AzureRmSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="17e79-110">Példák</span><span class="sxs-lookup"><span data-stu-id="17e79-110">EXAMPLES</span></span>

### <span data-ttu-id="17e79-111">1. példa: adatbázis eltávolítása egy példányból</span><span class="sxs-lookup"><span data-stu-id="17e79-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="17e79-112">Ez a parancs eltávolítja a Database01 nevű adatbázist a példány managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="17e79-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="17e79-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="17e79-113">PARAMETERS</span></span>

### <span data-ttu-id="17e79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e79-114">-DefaultProfile</span></span>
<span data-ttu-id="17e79-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17e79-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e79-116">-Force</span><span class="sxs-lookup"><span data-stu-id="17e79-116">-Force</span></span>
<span data-ttu-id="17e79-117">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="17e79-117">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e79-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17e79-118">-InputObject</span></span>
<span data-ttu-id="17e79-119">Az eltávolítani kívánt példány adatbázis-objektuma</span><span class="sxs-lookup"><span data-stu-id="17e79-119">The Instance Database object to remove</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17e79-120">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="17e79-120">-InstanceName</span></span>
<span data-ttu-id="17e79-121">A példány neve.</span><span class="sxs-lookup"><span data-stu-id="17e79-121">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e79-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="17e79-122">-Name</span></span>
<span data-ttu-id="17e79-123">Az eltávolítani kívánt Azure SQL-példány-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="17e79-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e79-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17e79-124">-ResourceGroupName</span></span>
<span data-ttu-id="17e79-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="17e79-125">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e79-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17e79-126">-ResourceId</span></span>
<span data-ttu-id="17e79-127">Az eltávolítandó adatbázis-objektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="17e79-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e79-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="17e79-128">-Confirm</span></span>
<span data-ttu-id="17e79-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="17e79-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e79-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17e79-130">-WhatIf</span></span>
<span data-ttu-id="17e79-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="17e79-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17e79-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="17e79-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e79-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e79-133">CommonParameters</span></span>
<span data-ttu-id="17e79-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="17e79-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e79-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17e79-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e79-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="17e79-136">INPUTS</span></span>

### <span data-ttu-id="17e79-137">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="17e79-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>
<span data-ttu-id="17e79-138">System. String</span><span class="sxs-lookup"><span data-stu-id="17e79-138">System.String</span></span>

## <span data-ttu-id="17e79-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17e79-139">OUTPUTS</span></span>

### <span data-ttu-id="17e79-140">Microsoft. Azure. Command. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="17e79-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="17e79-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="17e79-141">NOTES</span></span>

## <span data-ttu-id="17e79-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17e79-142">RELATED LINKS</span></span>

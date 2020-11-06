---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlmanagedinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
ms.openlocfilehash: 1da1c431d41c7277a8291bb9a012218057b9c678
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501960"
---
# <span data-ttu-id="064a1-101">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="064a1-101">Remove-AzureRmSqlInstance</span></span>

## <span data-ttu-id="064a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="064a1-102">SYNOPSIS</span></span>
<span data-ttu-id="064a1-103">Az Azure SQL felügyelt adatbázis-példány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="064a1-103">Removes an Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="064a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="064a1-104">SYNTAX</span></span>

### <span data-ttu-id="064a1-105">RemoveInstanceFromInputParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="064a1-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="064a1-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="064a1-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="064a1-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="064a1-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzureRmSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="064a1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="064a1-108">DESCRIPTION</span></span>
<span data-ttu-id="064a1-109">A **Remove-AzureRmSqlInstance** parancsmag eltávolítja az Azure SQL-adatbázis felügyelt példányát.</span><span class="sxs-lookup"><span data-stu-id="064a1-109">The **Remove-AzureRmSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="064a1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="064a1-110">EXAMPLES</span></span>

### <span data-ttu-id="064a1-111">Példa 1: példány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="064a1-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="064a1-112">Ez a parancs eltávolítja a managedInstance1 nevű példányt.</span><span class="sxs-lookup"><span data-stu-id="064a1-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="064a1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="064a1-113">PARAMETERS</span></span>

### <span data-ttu-id="064a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="064a1-114">-DefaultProfile</span></span>
<span data-ttu-id="064a1-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="064a1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="064a1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="064a1-116">-Force</span></span>
<span data-ttu-id="064a1-117">A művelet végrehajtásához szükséges megerősítési üzenet kihagyása</span><span class="sxs-lookup"><span data-stu-id="064a1-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="064a1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="064a1-118">-InputObject</span></span>
<span data-ttu-id="064a1-119">Az eltávolítandó AzureSqlManagedInstanceModel objektum</span><span class="sxs-lookup"><span data-stu-id="064a1-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="064a1-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="064a1-120">-Name</span></span>
<span data-ttu-id="064a1-121">SQL-példány neve</span><span class="sxs-lookup"><span data-stu-id="064a1-121">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="064a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="064a1-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="064a1-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="064a1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="064a1-124">-ResourceId</span></span>
<span data-ttu-id="064a1-125">Az eltávolítandó példány-objektum erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="064a1-125">The resource id of instance object to remove</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="064a1-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="064a1-126">-Confirm</span></span>
<span data-ttu-id="064a1-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="064a1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="064a1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="064a1-128">-WhatIf</span></span>
<span data-ttu-id="064a1-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="064a1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="064a1-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="064a1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="064a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="064a1-131">CommonParameters</span></span>
<span data-ttu-id="064a1-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="064a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="064a1-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="064a1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="064a1-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="064a1-134">INPUTS</span></span>

### <span data-ttu-id="064a1-135">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="064a1-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="064a1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="064a1-136">System.String</span></span>

## <span data-ttu-id="064a1-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="064a1-137">OUTPUTS</span></span>

### <span data-ttu-id="064a1-138">Microsoft. Azure. Command. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="064a1-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="064a1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="064a1-139">NOTES</span></span>

## <span data-ttu-id="064a1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="064a1-140">RELATED LINKS</span></span>

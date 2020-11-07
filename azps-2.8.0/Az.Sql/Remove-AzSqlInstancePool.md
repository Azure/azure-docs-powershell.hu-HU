---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: 97f6417bf2d58009e7a656dca280db4be2994879
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839110"
---
# <span data-ttu-id="21b75-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="21b75-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="21b75-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21b75-102">SYNOPSIS</span></span>
<span data-ttu-id="21b75-103">Azure SQL-példányok készletének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="21b75-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="21b75-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21b75-104">SYNTAX</span></span>

### <span data-ttu-id="21b75-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21b75-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21b75-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21b75-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21b75-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21b75-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21b75-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="21b75-108">DESCRIPTION</span></span>
<span data-ttu-id="21b75-109">A **Remove-AzSqlInstancePool** parancsmag eltávolítja az Azure SQL-példányok készletét.</span><span class="sxs-lookup"><span data-stu-id="21b75-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="21b75-110">Példák</span><span class="sxs-lookup"><span data-stu-id="21b75-110">EXAMPLES</span></span>

### <span data-ttu-id="21b75-111">1. példa: a példányok készletének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="21b75-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="21b75-112">2. példa: a példány-készlet eltávolítása az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="21b75-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="21b75-113">3. példa: egy példány készletének eltávolítása egy példány-gyűjtő objektummal</span><span class="sxs-lookup"><span data-stu-id="21b75-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="21b75-114">Ez a parancs eltávolítja a instancePool0 nevű példány-készletet.</span><span class="sxs-lookup"><span data-stu-id="21b75-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="21b75-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21b75-115">PARAMETERS</span></span>

### <span data-ttu-id="21b75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21b75-116">-DefaultProfile</span></span>
<span data-ttu-id="21b75-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21b75-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21b75-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21b75-118">-InputObject</span></span>
<span data-ttu-id="21b75-119">A példánynév objektum, amelyet el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="21b75-119">The instance pool object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21b75-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="21b75-120">-Name</span></span>
<span data-ttu-id="21b75-121">A példány-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="21b75-121">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b75-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21b75-122">-ResourceGroupName</span></span>
<span data-ttu-id="21b75-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="21b75-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b75-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21b75-124">-ResourceId</span></span>
<span data-ttu-id="21b75-125">A példány-készlet erőforrás-azonosítója, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="21b75-125">The instance pool resource id to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21b75-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="21b75-126">-Confirm</span></span>
<span data-ttu-id="21b75-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21b75-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21b75-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21b75-128">-WhatIf</span></span>
<span data-ttu-id="21b75-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="21b75-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21b75-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21b75-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21b75-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21b75-131">CommonParameters</span></span>
<span data-ttu-id="21b75-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21b75-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21b75-133">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="21b75-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21b75-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21b75-134">INPUTS</span></span>

### <span data-ttu-id="21b75-135">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="21b75-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="21b75-136">System. String</span><span class="sxs-lookup"><span data-stu-id="21b75-136">System.String</span></span>

## <span data-ttu-id="21b75-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21b75-137">OUTPUTS</span></span>

### <span data-ttu-id="21b75-138">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="21b75-138">System.Object</span></span>
## <span data-ttu-id="21b75-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21b75-139">NOTES</span></span>

## <span data-ttu-id="21b75-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21b75-140">RELATED LINKS</span></span>

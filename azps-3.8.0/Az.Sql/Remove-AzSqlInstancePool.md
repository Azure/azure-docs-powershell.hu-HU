---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: b10187938613f9ab6e0c12cb0d83162450be8445
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012945"
---
# <span data-ttu-id="3256e-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="3256e-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="3256e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3256e-102">SYNOPSIS</span></span>
<span data-ttu-id="3256e-103">Azure SQL-példányok készletének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3256e-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="3256e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3256e-104">SYNTAX</span></span>

### <span data-ttu-id="3256e-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3256e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3256e-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3256e-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3256e-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3256e-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3256e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3256e-108">DESCRIPTION</span></span>
<span data-ttu-id="3256e-109">A **Remove-AzSqlInstancePool** parancsmag eltávolítja az Azure SQL-példányok készletét.</span><span class="sxs-lookup"><span data-stu-id="3256e-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="3256e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3256e-110">EXAMPLES</span></span>

### <span data-ttu-id="3256e-111">1. példa: a példányok készletének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3256e-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="3256e-112">2. példa: a példány-készlet eltávolítása az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="3256e-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="3256e-113">3. példa: egy példány készletének eltávolítása egy példány-gyűjtő objektummal</span><span class="sxs-lookup"><span data-stu-id="3256e-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="3256e-114">Ez a parancs eltávolítja a instancePool0 nevű példány-készletet.</span><span class="sxs-lookup"><span data-stu-id="3256e-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="3256e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3256e-115">PARAMETERS</span></span>

### <span data-ttu-id="3256e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3256e-116">-DefaultProfile</span></span>
<span data-ttu-id="3256e-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3256e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3256e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3256e-118">-InputObject</span></span>
<span data-ttu-id="3256e-119">A példánynév objektum, amelyet el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="3256e-119">The instance pool object to remove.</span></span>

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

### <span data-ttu-id="3256e-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3256e-120">-Name</span></span>
<span data-ttu-id="3256e-121">A példány-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="3256e-121">The name of the instance pool.</span></span>

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

### <span data-ttu-id="3256e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3256e-122">-ResourceGroupName</span></span>
<span data-ttu-id="3256e-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3256e-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="3256e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3256e-124">-ResourceId</span></span>
<span data-ttu-id="3256e-125">A példány-készlet erőforrás-azonosítója, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="3256e-125">The instance pool resource id to remove.</span></span>

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

### <span data-ttu-id="3256e-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3256e-126">-Confirm</span></span>
<span data-ttu-id="3256e-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3256e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3256e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3256e-128">-WhatIf</span></span>
<span data-ttu-id="3256e-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3256e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3256e-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3256e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3256e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3256e-131">CommonParameters</span></span>
<span data-ttu-id="3256e-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3256e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3256e-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3256e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3256e-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3256e-134">INPUTS</span></span>

### <span data-ttu-id="3256e-135">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="3256e-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="3256e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3256e-136">System.String</span></span>

## <span data-ttu-id="3256e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3256e-137">OUTPUTS</span></span>

### <span data-ttu-id="3256e-138">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="3256e-138">System.Object</span></span>
## <span data-ttu-id="3256e-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3256e-139">NOTES</span></span>

## <span data-ttu-id="3256e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3256e-140">RELATED LINKS</span></span>

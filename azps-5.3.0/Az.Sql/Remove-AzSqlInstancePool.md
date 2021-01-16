---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: b10187938613f9ab6e0c12cb0d83162450be8445
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374526"
---
# <span data-ttu-id="8d67e-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="8d67e-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="8d67e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d67e-102">SYNOPSIS</span></span>
<span data-ttu-id="8d67e-103">Eltávolít egy Azure SQL-példánykészletet.</span><span class="sxs-lookup"><span data-stu-id="8d67e-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="8d67e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d67e-104">SYNTAX</span></span>

### <span data-ttu-id="8d67e-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d67e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d67e-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d67e-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d67e-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d67e-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d67e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d67e-108">DESCRIPTION</span></span>
<span data-ttu-id="8d67e-109">A **Remove-AzSqlInstancePool** parancsmag eltávolít egy Azure SQL-példánykészletet.</span><span class="sxs-lookup"><span data-stu-id="8d67e-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="8d67e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d67e-110">EXAMPLES</span></span>

### <span data-ttu-id="8d67e-111">1. példa: Példánykészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8d67e-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="8d67e-112">2. példa: Példánykészlet eltávolítása az erőforrás-azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="8d67e-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="8d67e-113">3. példa: Példánykészlet eltávolítása egy példánykészlet-objektum alapján</span><span class="sxs-lookup"><span data-stu-id="8d67e-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="8d67e-114">Ez a parancs eltávolítja az InstancePool0 nevű példánykészletet.</span><span class="sxs-lookup"><span data-stu-id="8d67e-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="8d67e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d67e-115">PARAMETERS</span></span>

### <span data-ttu-id="8d67e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d67e-116">-DefaultProfile</span></span>
<span data-ttu-id="8d67e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d67e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d67e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d67e-118">-InputObject</span></span>
<span data-ttu-id="8d67e-119">Az eltávolítható példánykészlet-objektum.</span><span class="sxs-lookup"><span data-stu-id="8d67e-119">The instance pool object to remove.</span></span>

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

### <span data-ttu-id="8d67e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8d67e-120">-Name</span></span>
<span data-ttu-id="8d67e-121">A példánykészlet neve.</span><span class="sxs-lookup"><span data-stu-id="8d67e-121">The name of the instance pool.</span></span>

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

### <span data-ttu-id="8d67e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d67e-122">-ResourceGroupName</span></span>
<span data-ttu-id="8d67e-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8d67e-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d67e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d67e-124">-ResourceId</span></span>
<span data-ttu-id="8d67e-125">Az eltávolítható példánykészlet erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="8d67e-125">The instance pool resource id to remove.</span></span>

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

### <span data-ttu-id="8d67e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d67e-126">-Confirm</span></span>
<span data-ttu-id="8d67e-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8d67e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d67e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d67e-128">-WhatIf</span></span>
<span data-ttu-id="8d67e-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8d67e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d67e-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d67e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d67e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d67e-131">CommonParameters</span></span>
<span data-ttu-id="8d67e-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d67e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d67e-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d67e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d67e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d67e-134">INPUTS</span></span>

### <span data-ttu-id="8d67e-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="8d67e-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="8d67e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8d67e-136">System.String</span></span>

## <span data-ttu-id="8d67e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d67e-137">OUTPUTS</span></span>

### <span data-ttu-id="8d67e-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="8d67e-138">System.Object</span></span>
## <span data-ttu-id="8d67e-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d67e-139">NOTES</span></span>

## <span data-ttu-id="8d67e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d67e-140">RELATED LINKS</span></span>

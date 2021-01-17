---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/export-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Export-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 1e50bba7c00c94daac983511f6fcea0ed1319759
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466601"
---
# <span data-ttu-id="92825-101">Export-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="92825-101">Export-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="92825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92825-102">SYNOPSIS</span></span>
<span data-ttu-id="92825-103">Adatbázisfájl exportálása a céladatbázisból</span><span class="sxs-lookup"><span data-stu-id="92825-103">Exports a database file from target database.</span></span>

## <span data-ttu-id="92825-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="92825-104">SYNTAX</span></span>

```
Export-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="92825-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="92825-105">DESCRIPTION</span></span>
<span data-ttu-id="92825-106">Adatbázisfájl exportálása a céladatbázisból</span><span class="sxs-lookup"><span data-stu-id="92825-106">Exports a database file from target database.</span></span>

## <span data-ttu-id="92825-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="92825-107">EXAMPLES</span></span>

### <span data-ttu-id="92825-108">1. példa: Adatbázis exportálása</span><span class="sxs-lookup"><span data-stu-id="92825-108">Example 1: Export database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Export-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="92825-109">Ez a parancs egy adatbázisfájlba exportálja a MyCache nevű Redis Enterprise Cache adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="92825-109">This command exports the database of the Redis Enterprise Cache named MyCache to a database file.</span></span>

## <span data-ttu-id="92825-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92825-110">PARAMETERS</span></span>

### <span data-ttu-id="92825-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92825-111">-AsJob</span></span>
<span data-ttu-id="92825-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="92825-112">Run the command as a job</span></span>

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

### <span data-ttu-id="92825-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="92825-113">-ClusterName</span></span>
<span data-ttu-id="92825-114">A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="92825-114">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92825-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92825-115">-DefaultProfile</span></span>
<span data-ttu-id="92825-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92825-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92825-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="92825-117">-NoWait</span></span>
<span data-ttu-id="92825-118">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="92825-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="92825-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92825-119">-PassThru</span></span>
<span data-ttu-id="92825-120">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="92825-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="92825-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92825-121">-ResourceGroupName</span></span>
<span data-ttu-id="92825-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92825-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92825-123">-SasUri</span><span class="sxs-lookup"><span data-stu-id="92825-123">-SasUri</span></span>
<span data-ttu-id="92825-124">SAS Uri ahhoz a célcímtárhoz, amelybe exportálni kell</span><span class="sxs-lookup"><span data-stu-id="92825-124">SAS Uri for the target directory to export to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92825-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92825-125">-SubscriptionId</span></span>
<span data-ttu-id="92825-126">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="92825-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="92825-127">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="92825-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92825-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92825-128">-Confirm</span></span>
<span data-ttu-id="92825-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="92825-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92825-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92825-130">-WhatIf</span></span>
<span data-ttu-id="92825-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="92825-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92825-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92825-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92825-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92825-133">CommonParameters</span></span>
<span data-ttu-id="92825-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92825-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92825-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92825-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92825-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92825-136">INPUTS</span></span>

## <span data-ttu-id="92825-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92825-137">OUTPUTS</span></span>

### <span data-ttu-id="92825-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92825-138">System.Boolean</span></span>

## <span data-ttu-id="92825-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="92825-139">NOTES</span></span>

<span data-ttu-id="92825-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="92825-140">ALIASES</span></span>

## <span data-ttu-id="92825-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92825-141">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/import-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Import-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: b7258c552d14a9c7cdeafae5c23908321b0705c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000774"
---
# <span data-ttu-id="b7946-101">Import-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="b7946-101">Import-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="b7946-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7946-102">SYNOPSIS</span></span>
<span data-ttu-id="b7946-103">Adatbázisfájlt importál a céladatbázisba.</span><span class="sxs-lookup"><span data-stu-id="b7946-103">Imports a database file to target database.</span></span>

## <span data-ttu-id="b7946-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7946-104">SYNTAX</span></span>

```
Import-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String> -SasUri <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b7946-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7946-105">DESCRIPTION</span></span>
<span data-ttu-id="b7946-106">Adatbázisfájlt importál a céladatbázisba.</span><span class="sxs-lookup"><span data-stu-id="b7946-106">Imports a database file to target database.</span></span>

## <span data-ttu-id="b7946-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7946-107">EXAMPLES</span></span>

### <span data-ttu-id="b7946-108">1. példa: Adatbázis importálása</span><span class="sxs-lookup"><span data-stu-id="b7946-108">Example 1: Import database</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/myfilename?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="b7946-109">Ez a parancs importál egy adatbázisfájlt a MyCache nevű Nagyvállalati gyorsítótár adatbázisába.</span><span class="sxs-lookup"><span data-stu-id="b7946-109">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="b7946-110">2. példa: Adatbázis importálása (példafájlnév használatával)</span><span class="sxs-lookup"><span data-stu-id="b7946-110">Example 2: Import database (using example filename)</span></span>
```powershell
#[SuppressMessage("Microsoft.Security", "CS002:SecretInNextLine", Justification="Invalid SAS token")]
PS C:\> Import-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -SasUri "https://mystorageaccount.blob.core.windows.net/mycontainer/bk20201130-223654-1-db-1_of_1-2-0-16383.rdb.gz?sp=rwdl&se=2020-09-02T11:17:15Z&sv=2019-12-12&sr=c&sig=Us%2FGshOUTKCSzTOi8dLtt1to2L32rcDr3Nn0WFFMdDM%3D;mystoragekey"
```

<span data-ttu-id="b7946-111">Ez a parancs importál egy adatbázisfájlt a MyCache nevű Nagyvállalati gyorsítótár adatbázisába.</span><span class="sxs-lookup"><span data-stu-id="b7946-111">This command imports a database file into the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="b7946-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7946-112">PARAMETERS</span></span>

### <span data-ttu-id="b7946-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7946-113">-AsJob</span></span>
<span data-ttu-id="b7946-114">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="b7946-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b7946-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b7946-115">-ClusterName</span></span>
<span data-ttu-id="b7946-116">A RedisEnterprise fürt neve.</span><span class="sxs-lookup"><span data-stu-id="b7946-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="b7946-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7946-117">-DefaultProfile</span></span>
<span data-ttu-id="b7946-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7946-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7946-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b7946-119">-NoWait</span></span>
<span data-ttu-id="b7946-120">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="b7946-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b7946-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7946-121">-PassThru</span></span>
<span data-ttu-id="b7946-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="b7946-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b7946-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7946-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7946-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b7946-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7946-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="b7946-125">-SasUri</span></span>
<span data-ttu-id="b7946-126">SAS Uri ahhoz a cél blobhoz, amelyből importálni kell</span><span class="sxs-lookup"><span data-stu-id="b7946-126">SAS Uri for the target blob to import from</span></span>

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

### <span data-ttu-id="b7946-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7946-127">-SubscriptionId</span></span>
<span data-ttu-id="b7946-128">Olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b7946-128">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b7946-129">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b7946-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b7946-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7946-130">-Confirm</span></span>
<span data-ttu-id="b7946-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b7946-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7946-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7946-132">-WhatIf</span></span>
<span data-ttu-id="b7946-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b7946-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7946-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7946-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7946-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7946-135">CommonParameters</span></span>
<span data-ttu-id="b7946-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7946-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7946-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7946-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7946-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7946-138">INPUTS</span></span>

## <span data-ttu-id="b7946-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7946-139">OUTPUTS</span></span>

### <span data-ttu-id="b7946-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b7946-140">System.Boolean</span></span>

## <span data-ttu-id="b7946-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7946-141">NOTES</span></span>

<span data-ttu-id="b7946-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b7946-142">ALIASES</span></span>

## <span data-ttu-id="b7946-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7946-143">RELATED LINKS</span></span>


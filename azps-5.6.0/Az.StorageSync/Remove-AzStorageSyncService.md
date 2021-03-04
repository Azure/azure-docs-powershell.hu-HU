---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 648ef711d030f7600863d286df24cfdf1d2f7927
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929625"
---
# <span data-ttu-id="78fd4-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="78fd4-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="78fd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="78fd4-103">Ez a parancs törli a megadott tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="78fd4-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="78fd4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="78fd4-104">SYNTAX</span></span>

### <span data-ttu-id="78fd4-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78fd4-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78fd4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78fd4-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78fd4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78fd4-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78fd4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="78fd4-108">DESCRIPTION</span></span>
<span data-ttu-id="78fd4-109">Ez a parancs törli a megadott tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="78fd4-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="78fd4-110">A tárterület-szinkronizálási szolgáltatás csak akkor távolítható el, ha először az összes tartalmazott szinkronizálási csoportot és regisztrált kiszolgálót törli.</span><span class="sxs-lookup"><span data-stu-id="78fd4-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="78fd4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="78fd4-111">EXAMPLES</span></span>

### <span data-ttu-id="78fd4-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="78fd4-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="78fd4-113">Ez a parancs eltávolítja a tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="78fd4-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="78fd4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78fd4-114">PARAMETERS</span></span>

### <span data-ttu-id="78fd4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78fd4-115">-AsJob</span></span>
<span data-ttu-id="78fd4-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="78fd4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78fd4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78fd4-117">-DefaultProfile</span></span>
<span data-ttu-id="78fd4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78fd4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78fd4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="78fd4-119">-Force</span></span>
<span data-ttu-id="78fd4-120">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="78fd4-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78fd4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78fd4-121">-InputObject</span></span>
<span data-ttu-id="78fd4-122">StorageSyncService input object, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="78fd4-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78fd4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="78fd4-123">-Name</span></span>
<span data-ttu-id="78fd4-124">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="78fd4-124">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78fd4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78fd4-125">-PassThru</span></span>
<span data-ttu-id="78fd4-126">Normál végrehajtáskor ez a parancsmag nem ad vissza értéket a sikerhez.</span><span class="sxs-lookup"><span data-stu-id="78fd4-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="78fd4-127">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után értéket ír a folyamatba.</span><span class="sxs-lookup"><span data-stu-id="78fd4-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="78fd4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78fd4-128">-ResourceGroupName</span></span>
<span data-ttu-id="78fd4-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="78fd4-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78fd4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78fd4-130">-ResourceId</span></span>
<span data-ttu-id="78fd4-131">StorageSyncService erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="78fd4-131">StorageSyncService Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78fd4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78fd4-132">-Confirm</span></span>
<span data-ttu-id="78fd4-133">A parancsmag futtatása előtt megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="78fd4-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78fd4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78fd4-134">-WhatIf</span></span>
<span data-ttu-id="78fd4-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="78fd4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78fd4-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78fd4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78fd4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78fd4-137">CommonParameters</span></span>
<span data-ttu-id="78fd4-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78fd4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78fd4-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78fd4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78fd4-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78fd4-140">INPUTS</span></span>

### <span data-ttu-id="78fd4-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="78fd4-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="78fd4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="78fd4-142">System.String</span></span>

### <span data-ttu-id="78fd4-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="78fd4-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="78fd4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78fd4-144">OUTPUTS</span></span>

### <span data-ttu-id="78fd4-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="78fd4-145">System.Object</span></span>
## <span data-ttu-id="78fd4-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="78fd4-146">NOTES</span></span>

## <span data-ttu-id="78fd4-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78fd4-147">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479366"
---
# <span data-ttu-id="d779a-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="d779a-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="d779a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d779a-102">SYNOPSIS</span></span>
<span data-ttu-id="d779a-103">Ez a parancs törli a megadott tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d779a-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="d779a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d779a-104">SYNTAX</span></span>

### <span data-ttu-id="d779a-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d779a-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d779a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d779a-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d779a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d779a-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d779a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d779a-108">DESCRIPTION</span></span>
<span data-ttu-id="d779a-109">Ez a parancs törli a megadott tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d779a-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="d779a-110">A tárterület-szinkronizálási szolgáltatás csak akkor távolítható el, ha először az összes tartalmazott szinkronizálási csoportot és regisztrált kiszolgálót törli.</span><span class="sxs-lookup"><span data-stu-id="d779a-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="d779a-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d779a-111">EXAMPLES</span></span>

### <span data-ttu-id="d779a-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="d779a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="d779a-113">Ez a parancs eltávolítja a tárterület-szinkronizálási szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="d779a-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="d779a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d779a-114">PARAMETERS</span></span>

### <span data-ttu-id="d779a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d779a-115">-AsJob</span></span>
<span data-ttu-id="d779a-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d779a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d779a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d779a-117">-DefaultProfile</span></span>
<span data-ttu-id="d779a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d779a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d779a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d779a-119">-Force</span></span>
<span data-ttu-id="d779a-120">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="d779a-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="d779a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d779a-121">-InputObject</span></span>
<span data-ttu-id="d779a-122">StorageSyncService input object, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="d779a-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="d779a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d779a-123">-Name</span></span>
<span data-ttu-id="d779a-124">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="d779a-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="d779a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d779a-125">-PassThru</span></span>
<span data-ttu-id="d779a-126">Normál végrehajtáskor ez a parancsmag nem ad vissza értéket a sikerhez.</span><span class="sxs-lookup"><span data-stu-id="d779a-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="d779a-127">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után értéket ír a folyamatba.</span><span class="sxs-lookup"><span data-stu-id="d779a-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="d779a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d779a-128">-ResourceGroupName</span></span>
<span data-ttu-id="d779a-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d779a-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="d779a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d779a-130">-ResourceId</span></span>
<span data-ttu-id="d779a-131">StorageSyncService erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="d779a-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="d779a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d779a-132">-Confirm</span></span>
<span data-ttu-id="d779a-133">A parancsmag futtatása előtt megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d779a-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d779a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d779a-134">-WhatIf</span></span>
<span data-ttu-id="d779a-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d779a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d779a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d779a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d779a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d779a-137">CommonParameters</span></span>
<span data-ttu-id="d779a-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d779a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d779a-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d779a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d779a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d779a-140">INPUTS</span></span>

### <span data-ttu-id="d779a-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="d779a-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="d779a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d779a-142">System.String</span></span>

### <span data-ttu-id="d779a-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d779a-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d779a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d779a-144">OUTPUTS</span></span>

### <span data-ttu-id="d779a-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="d779a-145">System.Object</span></span>
## <span data-ttu-id="d779a-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d779a-146">NOTES</span></span>

## <span data-ttu-id="d779a-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d779a-147">RELATED LINKS</span></span>

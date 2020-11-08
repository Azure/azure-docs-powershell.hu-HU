---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: f64c085f742eeabea235660d4af7ba6bd5970fdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186001"
---
# <span data-ttu-id="705d2-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="705d2-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="705d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="705d2-102">SYNOPSIS</span></span>
<span data-ttu-id="705d2-103">Ezzel a paranccsal törlődik a megadott tárterület-szinkronizálási szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="705d2-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="705d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="705d2-104">SYNTAX</span></span>

### <span data-ttu-id="705d2-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="705d2-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="705d2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="705d2-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="705d2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="705d2-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="705d2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="705d2-108">DESCRIPTION</span></span>
<span data-ttu-id="705d2-109">Ezzel a paranccsal törlődik a megadott tárterület-szinkronizálási szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="705d2-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="705d2-110">A tárterület-szinkronizálási szolgáltatás csak akkor távolítható el, ha az összes tárolt szinkronizálási csoport és regisztrált kiszolgáló törlődik először.</span><span class="sxs-lookup"><span data-stu-id="705d2-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="705d2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="705d2-111">EXAMPLES</span></span>

### <span data-ttu-id="705d2-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="705d2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="705d2-113">Ezzel a paranccsal törlődik a tárterület-szinkronizálási szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="705d2-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="705d2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="705d2-114">PARAMETERS</span></span>

### <span data-ttu-id="705d2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="705d2-115">-AsJob</span></span>
<span data-ttu-id="705d2-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="705d2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="705d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="705d2-117">-DefaultProfile</span></span>
<span data-ttu-id="705d2-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="705d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="705d2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="705d2-119">-Force</span></span>
<span data-ttu-id="705d2-120">Supply-Force: a parancs megerősítésének mellőzése.</span><span class="sxs-lookup"><span data-stu-id="705d2-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="705d2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="705d2-121">-InputObject</span></span>
<span data-ttu-id="705d2-122">A StorageSyncService bemeneti objektuma, normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="705d2-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="705d2-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="705d2-123">-Name</span></span>
<span data-ttu-id="705d2-124">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="705d2-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="705d2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="705d2-125">-PassThru</span></span>
<span data-ttu-id="705d2-126">A normál végrehajtásban ez a parancsmag nem ad értéket a sikernek.</span><span class="sxs-lookup"><span data-stu-id="705d2-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="705d2-127">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után a csővezetéknek ad értéket.</span><span class="sxs-lookup"><span data-stu-id="705d2-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="705d2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="705d2-128">-ResourceGroupName</span></span>
<span data-ttu-id="705d2-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="705d2-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="705d2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="705d2-130">-ResourceId</span></span>
<span data-ttu-id="705d2-131">StorageSyncService erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="705d2-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="705d2-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="705d2-132">-Confirm</span></span>
<span data-ttu-id="705d2-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="705d2-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="705d2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="705d2-134">-WhatIf</span></span>
<span data-ttu-id="705d2-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="705d2-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="705d2-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="705d2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="705d2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="705d2-137">CommonParameters</span></span>
<span data-ttu-id="705d2-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="705d2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="705d2-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="705d2-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="705d2-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="705d2-140">INPUTS</span></span>

### <span data-ttu-id="705d2-141">Microsoft. Azure. Command. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="705d2-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="705d2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="705d2-142">System.String</span></span>

### <span data-ttu-id="705d2-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="705d2-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="705d2-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="705d2-144">OUTPUTS</span></span>

### <span data-ttu-id="705d2-145">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="705d2-145">System.Object</span></span>
## <span data-ttu-id="705d2-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="705d2-146">NOTES</span></span>

## <span data-ttu-id="705d2-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="705d2-147">RELATED LINKS</span></span>

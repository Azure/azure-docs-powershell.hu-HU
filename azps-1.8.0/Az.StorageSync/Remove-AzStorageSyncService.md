---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 5116ead7111902b1009517ff42ff6594ac87d8c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668475"
---
# <span data-ttu-id="ad55c-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ad55c-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="ad55c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad55c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad55c-103">Ezzel a paranccsal törlődik a megadott tárterület-szinkronizálási szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="ad55c-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="ad55c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad55c-104">SYNTAX</span></span>

### <span data-ttu-id="ad55c-105">InputObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad55c-105">InputObjectParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad55c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad55c-106">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad55c-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad55c-107">StringParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad55c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad55c-108">DESCRIPTION</span></span>
<span data-ttu-id="ad55c-109">Ezzel a paranccsal törlődik a megadott tárterület-szinkronizálási szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="ad55c-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="ad55c-110">A tárterület-szinkronizálási szolgáltatás csak akkor távolítható el, ha az összes tárolt szinkronizálási csoport és regisztrált kiszolgáló törlődik először.</span><span class="sxs-lookup"><span data-stu-id="ad55c-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="ad55c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ad55c-111">EXAMPLES</span></span>

### <span data-ttu-id="ad55c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ad55c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="ad55c-113">Ezzel a paranccsal törlődik a tárterület-szinkronizálási szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="ad55c-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="ad55c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad55c-114">PARAMETERS</span></span>

### <span data-ttu-id="ad55c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad55c-115">-AsJob</span></span>
<span data-ttu-id="ad55c-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ad55c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad55c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad55c-117">-DefaultProfile</span></span>
<span data-ttu-id="ad55c-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad55c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad55c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ad55c-119">-Force</span></span>
<span data-ttu-id="ad55c-120">Supply-Force: a parancs megerősítésének mellőzése.</span><span class="sxs-lookup"><span data-stu-id="ad55c-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="ad55c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad55c-121">-InputObject</span></span>
<span data-ttu-id="ad55c-122">A StorageSyncService bemeneti objektuma, normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="ad55c-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ad55c-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad55c-123">-Name</span></span>
<span data-ttu-id="ad55c-124">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="ad55c-124">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ad55c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad55c-125">-PassThru</span></span>
<span data-ttu-id="ad55c-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ad55c-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ad55c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad55c-127">-ResourceGroupName</span></span>
<span data-ttu-id="ad55c-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ad55c-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="ad55c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad55c-129">-ResourceId</span></span>
<span data-ttu-id="ad55c-130">StorageSyncService erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="ad55c-130">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="ad55c-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad55c-131">-Confirm</span></span>
<span data-ttu-id="ad55c-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad55c-132">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad55c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad55c-133">-WhatIf</span></span>
<span data-ttu-id="ad55c-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad55c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad55c-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad55c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad55c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad55c-136">CommonParameters</span></span>
<span data-ttu-id="ad55c-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad55c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad55c-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad55c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad55c-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad55c-139">INPUTS</span></span>

### <span data-ttu-id="ad55c-140">Microsoft. Azure. Command. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ad55c-140">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="ad55c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ad55c-141">System.String</span></span>

### <span data-ttu-id="ad55c-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ad55c-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ad55c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad55c-143">OUTPUTS</span></span>

### <span data-ttu-id="ad55c-144">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="ad55c-144">System.Object</span></span>
## <span data-ttu-id="ad55c-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad55c-145">NOTES</span></span>

## <span data-ttu-id="ad55c-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad55c-146">RELATED LINKS</span></span>

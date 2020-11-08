---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: fb199887edcc3a9895095101870856d15f86ac08
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013126"
---
# <span data-ttu-id="ff505-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ff505-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="ff505-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff505-102">SYNOPSIS</span></span>
<span data-ttu-id="ff505-103">A parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="ff505-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="ff505-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff505-104">SYNTAX</span></span>

### <span data-ttu-id="ff505-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ff505-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff505-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff505-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff505-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff505-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff505-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff505-108">DESCRIPTION</span></span>
<span data-ttu-id="ff505-109">A parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="ff505-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="ff505-110">A szinkronizálási csoportok segítségével leírhatja a helyek topológiáját (például végpontként), amely az egyik végponton belül tárolt fájlokat szinkronizálja.</span><span class="sxs-lookup"><span data-stu-id="ff505-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="ff505-111">A szinkronizálási csoport olyan Felhőbeli végpontokat tartalmaz, amelyek az Azure-fájlok megosztására szolgálnak, és olyan kiszolgálói végpontokat is tartalmaznak, amelyek egy adott helyi elérési útra hivatkoznak egy regisztrált kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="ff505-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="ff505-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ff505-112">EXAMPLES</span></span>

### <span data-ttu-id="ff505-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ff505-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="ff505-114">A parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="ff505-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="ff505-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff505-115">PARAMETERS</span></span>

### <span data-ttu-id="ff505-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff505-116">-DefaultProfile</span></span>
<span data-ttu-id="ff505-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff505-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff505-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ff505-118">-Name</span></span>
<span data-ttu-id="ff505-119">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="ff505-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff505-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ff505-120">-ParentObject</span></span>
<span data-ttu-id="ff505-121">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="ff505-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff505-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ff505-122">-ParentResourceId</span></span>
<span data-ttu-id="ff505-123">A StorageSyncService szülő erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ff505-123">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff505-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff505-124">-ResourceGroupName</span></span>
<span data-ttu-id="ff505-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ff505-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff505-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ff505-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="ff505-127">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="ff505-127">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff505-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff505-128">-Confirm</span></span>
<span data-ttu-id="ff505-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff505-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff505-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff505-130">-WhatIf</span></span>
<span data-ttu-id="ff505-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff505-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff505-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff505-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff505-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff505-133">CommonParameters</span></span>
<span data-ttu-id="ff505-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff505-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff505-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff505-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff505-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff505-136">INPUTS</span></span>

### <span data-ttu-id="ff505-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ff505-137">System.String</span></span>

### <span data-ttu-id="ff505-138">Microsoft. Azure. Command. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ff505-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="ff505-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff505-139">OUTPUTS</span></span>

### <span data-ttu-id="ff505-140">Microsoft. Azure. Command. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ff505-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="ff505-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff505-141">NOTES</span></span>

## <span data-ttu-id="ff505-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff505-142">RELATED LINKS</span></span>

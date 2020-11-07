---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: 2913cbece59687516aa7e2aa83e3cea035218fd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839889"
---
# <span data-ttu-id="c8310-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c8310-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="c8310-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8310-102">SYNOPSIS</span></span>
<span data-ttu-id="c8310-103">A parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="c8310-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="c8310-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8310-104">SYNTAX</span></span>

### <span data-ttu-id="c8310-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8310-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8310-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8310-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8310-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8310-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8310-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8310-108">DESCRIPTION</span></span>
<span data-ttu-id="c8310-109">A parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="c8310-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="c8310-110">A szinkronizálási csoportok segítségével leírhatja a helyek topológiáját (például végpontként), amely az egyik végponton belül tárolt fájlokat szinkronizálja.</span><span class="sxs-lookup"><span data-stu-id="c8310-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="c8310-111">A szinkronizálási csoport olyan Felhőbeli végpontokat tartalmaz, amelyek az Azure-fájlok megosztására szolgálnak, és olyan kiszolgálói végpontokat is tartalmaznak, amelyek egy adott helyi elérési útra hivatkoznak egy regisztrált kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="c8310-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="c8310-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c8310-112">EXAMPLES</span></span>

### <span data-ttu-id="c8310-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c8310-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="c8310-114">A parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="c8310-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="c8310-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8310-115">PARAMETERS</span></span>

### <span data-ttu-id="c8310-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8310-116">-DefaultProfile</span></span>
<span data-ttu-id="c8310-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8310-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8310-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c8310-118">-Name</span></span>
<span data-ttu-id="c8310-119">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="c8310-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="c8310-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c8310-120">-ParentObject</span></span>
<span data-ttu-id="c8310-121">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="c8310-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c8310-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c8310-122">-ParentResourceId</span></span>
<span data-ttu-id="c8310-123">A StorageSyncService szülő erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c8310-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="c8310-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8310-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8310-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c8310-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c8310-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c8310-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="c8310-127">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="c8310-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c8310-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c8310-128">-Confirm</span></span>
<span data-ttu-id="c8310-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8310-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8310-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8310-130">-WhatIf</span></span>
<span data-ttu-id="c8310-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c8310-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8310-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8310-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8310-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8310-133">CommonParameters</span></span>
<span data-ttu-id="c8310-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8310-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8310-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8310-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8310-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8310-136">INPUTS</span></span>

### <span data-ttu-id="c8310-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c8310-137">System.String</span></span>

### <span data-ttu-id="c8310-138">Microsoft. Azure. Command. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c8310-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="c8310-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8310-139">OUTPUTS</span></span>

### <span data-ttu-id="c8310-140">Microsoft. Azure. Command. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c8310-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="c8310-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8310-141">NOTES</span></span>

## <span data-ttu-id="c8310-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8310-142">RELATED LINKS</span></span>

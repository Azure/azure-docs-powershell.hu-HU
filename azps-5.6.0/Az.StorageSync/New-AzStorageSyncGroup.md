---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: e96b4360247937ace5a0e2894f3bfac19fc1da0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011413"
---
# <span data-ttu-id="15cc3-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="15cc3-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="15cc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="15cc3-103">Ez a parancs egy új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="15cc3-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="15cc3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="15cc3-104">SYNTAX</span></span>

### <span data-ttu-id="15cc3-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15cc3-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15cc3-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15cc3-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15cc3-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="15cc3-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15cc3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="15cc3-108">DESCRIPTION</span></span>
<span data-ttu-id="15cc3-109">Ez a parancs egy új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="15cc3-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="15cc3-110">A szinkronizálási csoportok a helyek (más néven végpontok) topológiájának leírására használhatók, amelyek a végpontok bármelyikében tárolt fájlokat szinkronizálják.</span><span class="sxs-lookup"><span data-stu-id="15cc3-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="15cc3-111">A szinkronizálási csoportok felhőbeli végpontokat tartalmaznak, amelyek Azure-fájlmegosztásokra hivatkoznak, valamint olyan kiszolgálói végpontokat is tartalmaznak, amelyek egy regisztrált kiszolgálón egy adott helyi elérési útvonalra hivatkoznak.</span><span class="sxs-lookup"><span data-stu-id="15cc3-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="15cc3-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="15cc3-112">EXAMPLES</span></span>

### <span data-ttu-id="15cc3-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="15cc3-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="15cc3-114">Ez a parancs egy új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="15cc3-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="15cc3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15cc3-115">PARAMETERS</span></span>

### <span data-ttu-id="15cc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15cc3-116">-DefaultProfile</span></span>
<span data-ttu-id="15cc3-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15cc3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15cc3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="15cc3-118">-Name</span></span>
<span data-ttu-id="15cc3-119">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="15cc3-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="15cc3-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="15cc3-120">-ParentObject</span></span>
<span data-ttu-id="15cc3-121">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="15cc3-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="15cc3-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="15cc3-122">-ParentResourceId</span></span>
<span data-ttu-id="15cc3-123">StorageSyncService szülőerőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="15cc3-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="15cc3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15cc3-124">-ResourceGroupName</span></span>
<span data-ttu-id="15cc3-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="15cc3-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="15cc3-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="15cc3-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="15cc3-127">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="15cc3-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="15cc3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15cc3-128">-Confirm</span></span>
<span data-ttu-id="15cc3-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="15cc3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15cc3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15cc3-130">-WhatIf</span></span>
<span data-ttu-id="15cc3-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="15cc3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15cc3-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15cc3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15cc3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15cc3-133">CommonParameters</span></span>
<span data-ttu-id="15cc3-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15cc3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15cc3-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15cc3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15cc3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15cc3-136">INPUTS</span></span>

### <span data-ttu-id="15cc3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="15cc3-137">System.String</span></span>

### <span data-ttu-id="15cc3-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="15cc3-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="15cc3-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15cc3-139">OUTPUTS</span></span>

### <span data-ttu-id="15cc3-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="15cc3-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="15cc3-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="15cc3-141">NOTES</span></span>

## <span data-ttu-id="15cc3-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15cc3-142">RELATED LINKS</span></span>

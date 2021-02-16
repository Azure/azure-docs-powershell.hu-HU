---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: fb199887edcc3a9895095101870856d15f86ac08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150307"
---
# <span data-ttu-id="731ea-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="731ea-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="731ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="731ea-102">SYNOPSIS</span></span>
<span data-ttu-id="731ea-103">Ez a parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="731ea-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="731ea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="731ea-104">SYNTAX</span></span>

### <span data-ttu-id="731ea-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="731ea-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731ea-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="731ea-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731ea-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="731ea-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="731ea-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="731ea-108">DESCRIPTION</span></span>
<span data-ttu-id="731ea-109">Ez a parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="731ea-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="731ea-110">A szinkronizálási csoportok a helyek (más néven végpontok) topológiájának leírására használhatók, amelyek a végpontok bármelyikében tárolt fájlokat szinkronizálják.</span><span class="sxs-lookup"><span data-stu-id="731ea-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="731ea-111">A szinkronizálási csoportok felhőbeli végpontokat tartalmaznak, amelyek Azure-fájlmegosztásokra hivatkoznak, valamint olyan kiszolgálói végpontokat is tartalmaznak, amelyek egy regisztrált kiszolgálón egy adott helyi elérési útvonalra hivatkoznak.</span><span class="sxs-lookup"><span data-stu-id="731ea-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="731ea-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="731ea-112">EXAMPLES</span></span>

### <span data-ttu-id="731ea-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="731ea-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="731ea-114">Ez a parancs új szinkronizálási csoportot hoz létre egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="731ea-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="731ea-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="731ea-115">PARAMETERS</span></span>

### <span data-ttu-id="731ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="731ea-116">-DefaultProfile</span></span>
<span data-ttu-id="731ea-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="731ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="731ea-118">-Name</span><span class="sxs-lookup"><span data-stu-id="731ea-118">-Name</span></span>
<span data-ttu-id="731ea-119">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="731ea-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="731ea-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="731ea-120">-ParentObject</span></span>
<span data-ttu-id="731ea-121">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="731ea-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="731ea-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="731ea-122">-ParentResourceId</span></span>
<span data-ttu-id="731ea-123">StorageSyncService szülőerőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="731ea-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="731ea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="731ea-124">-ResourceGroupName</span></span>
<span data-ttu-id="731ea-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="731ea-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="731ea-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="731ea-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="731ea-127">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="731ea-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="731ea-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="731ea-128">-Confirm</span></span>
<span data-ttu-id="731ea-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="731ea-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="731ea-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="731ea-130">-WhatIf</span></span>
<span data-ttu-id="731ea-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="731ea-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="731ea-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="731ea-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="731ea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731ea-133">CommonParameters</span></span>
<span data-ttu-id="731ea-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="731ea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731ea-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="731ea-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731ea-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="731ea-136">INPUTS</span></span>

### <span data-ttu-id="731ea-137">System.String</span><span class="sxs-lookup"><span data-stu-id="731ea-137">System.String</span></span>

### <span data-ttu-id="731ea-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="731ea-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="731ea-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="731ea-139">OUTPUTS</span></span>

### <span data-ttu-id="731ea-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="731ea-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="731ea-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="731ea-141">NOTES</span></span>

## <span data-ttu-id="731ea-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="731ea-142">RELATED LINKS</span></span>

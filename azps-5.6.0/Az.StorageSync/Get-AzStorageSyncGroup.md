---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: 53ee755daeb0e483b98c9e8449720acce6e38233
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929194"
---
# <span data-ttu-id="a4dc8-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a4dc8-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="a4dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="a4dc8-103">Ez a parancs felsorolja az adott tár szinkronizálási szolgáltatásában található összes szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="a4dc8-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="a4dc8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a4dc8-104">SYNTAX</span></span>

### <span data-ttu-id="a4dc8-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4dc8-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4dc8-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4dc8-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4dc8-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4dc8-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4dc8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a4dc8-108">DESCRIPTION</span></span>
<span data-ttu-id="a4dc8-109">Ez a parancs felsorolja az adott tár szinkronizálási szolgáltatásában található összes szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="a4dc8-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="a4dc8-110">Az egyes szinkronizálási csoportok attribútumainak felsorolásához is használható.</span><span class="sxs-lookup"><span data-stu-id="a4dc8-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="a4dc8-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a4dc8-111">EXAMPLES</span></span>

### <span data-ttu-id="a4dc8-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="a4dc8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="a4dc8-113">Ez a parancs a megadott tárterület-szinkronizálási szolgáltatásban található összes szinkronizálási csoportot lekérte.</span><span class="sxs-lookup"><span data-stu-id="a4dc8-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="a4dc8-114">A -Name érték megadásával adott értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="a4dc8-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="a4dc8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4dc8-115">PARAMETERS</span></span>

### <span data-ttu-id="a4dc8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4dc8-116">-DefaultProfile</span></span>
<span data-ttu-id="a4dc8-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4dc8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4dc8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a4dc8-118">-Name</span></span>
<span data-ttu-id="a4dc8-119">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="a4dc8-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4dc8-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a4dc8-120">-ParentObject</span></span>
<span data-ttu-id="a4dc8-121">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="a4dc8-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="a4dc8-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a4dc8-122">-ParentResourceId</span></span>
<span data-ttu-id="a4dc8-123">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="a4dc8-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="a4dc8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4dc8-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4dc8-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4dc8-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a4dc8-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="a4dc8-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="a4dc8-127">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="a4dc8-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="a4dc8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4dc8-128">CommonParameters</span></span>
<span data-ttu-id="a4dc8-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4dc8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4dc8-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4dc8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4dc8-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4dc8-131">INPUTS</span></span>

### <span data-ttu-id="a4dc8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a4dc8-132">System.String</span></span>

### <span data-ttu-id="a4dc8-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="a4dc8-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="a4dc8-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4dc8-134">OUTPUTS</span></span>

### <span data-ttu-id="a4dc8-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a4dc8-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="a4dc8-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a4dc8-136">NOTES</span></span>

## <span data-ttu-id="a4dc8-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4dc8-137">RELATED LINKS</span></span>

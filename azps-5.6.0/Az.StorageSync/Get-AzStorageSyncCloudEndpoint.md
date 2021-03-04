---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: b4dbee18ef0fad33180e9cc9c3d04a49e1288b74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929201"
---
# <span data-ttu-id="92007-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="92007-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="92007-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92007-102">SYNOPSIS</span></span>
<span data-ttu-id="92007-103">Ez a parancs felsorolja egy adott szinkronizálási csoport összes felhőbeli végpontját.</span><span class="sxs-lookup"><span data-stu-id="92007-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="92007-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="92007-104">SYNTAX</span></span>

### <span data-ttu-id="92007-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92007-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92007-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92007-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92007-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="92007-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92007-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="92007-108">DESCRIPTION</span></span>
<span data-ttu-id="92007-109">Ez a parancs felsorolja egy adott szinkronizálási csoport összes felhőbeli végpontját.</span><span class="sxs-lookup"><span data-stu-id="92007-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="92007-110">Az egyes felhőbeli végpontok attribútumainak felsorolásához is használható.</span><span class="sxs-lookup"><span data-stu-id="92007-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="92007-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="92007-111">EXAMPLES</span></span>

### <span data-ttu-id="92007-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="92007-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="92007-113">Ez a parancs a megadott szinkronizálási csoportban található összes felhőbeli végpontot lekérte.</span><span class="sxs-lookup"><span data-stu-id="92007-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="92007-114">A -CloudEndpointName paramétert megadásával adott értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="92007-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="92007-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92007-115">PARAMETERS</span></span>

### <span data-ttu-id="92007-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92007-116">-DefaultProfile</span></span>
<span data-ttu-id="92007-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92007-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92007-118">-Name</span><span class="sxs-lookup"><span data-stu-id="92007-118">-Name</span></span>
<span data-ttu-id="92007-119">A CloudEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="92007-119">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92007-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="92007-120">-ParentObject</span></span>
<span data-ttu-id="92007-121">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="92007-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92007-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="92007-122">-ParentResourceId</span></span>
<span data-ttu-id="92007-123">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="92007-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92007-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92007-124">-ResourceGroupName</span></span>
<span data-ttu-id="92007-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92007-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="92007-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="92007-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="92007-127">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="92007-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="92007-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="92007-128">-SyncGroupName</span></span>
<span data-ttu-id="92007-129">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="92007-129">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92007-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92007-130">CommonParameters</span></span>
<span data-ttu-id="92007-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92007-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92007-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92007-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92007-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92007-133">INPUTS</span></span>

### <span data-ttu-id="92007-134">System.String</span><span class="sxs-lookup"><span data-stu-id="92007-134">System.String</span></span>

### <span data-ttu-id="92007-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="92007-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="92007-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92007-136">OUTPUTS</span></span>

### <span data-ttu-id="92007-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="92007-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="92007-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="92007-138">NOTES</span></span>

## <span data-ttu-id="92007-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92007-139">RELATED LINKS</span></span>

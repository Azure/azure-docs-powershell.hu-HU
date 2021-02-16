---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 076a1393365e93a8008f15137d078a49491d81f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150354"
---
# <span data-ttu-id="084d6-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="084d6-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="084d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="084d6-102">SYNOPSIS</span></span>
<span data-ttu-id="084d6-103">Ez a parancs felsorolja egy adott szinkronizálási csoport összes felhőbeli végpontját.</span><span class="sxs-lookup"><span data-stu-id="084d6-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="084d6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="084d6-104">SYNTAX</span></span>

### <span data-ttu-id="084d6-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="084d6-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="084d6-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="084d6-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="084d6-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="084d6-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="084d6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="084d6-108">DESCRIPTION</span></span>
<span data-ttu-id="084d6-109">Ez a parancs felsorolja egy adott szinkronizálási csoport összes felhőbeli végpontját.</span><span class="sxs-lookup"><span data-stu-id="084d6-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="084d6-110">Az egyes felhőbeli végpontok attribútumainak felsorolásához is használható.</span><span class="sxs-lookup"><span data-stu-id="084d6-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="084d6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="084d6-111">EXAMPLES</span></span>

### <span data-ttu-id="084d6-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="084d6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="084d6-113">Ez a parancs a megadott szinkronizálási csoportban található összes felhőbeli végpontot lekérte.</span><span class="sxs-lookup"><span data-stu-id="084d6-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="084d6-114">A -CloudEndpointName paramétert megadásával adott értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="084d6-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="084d6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="084d6-115">PARAMETERS</span></span>

### <span data-ttu-id="084d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="084d6-116">-DefaultProfile</span></span>
<span data-ttu-id="084d6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="084d6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="084d6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="084d6-118">-Name</span></span>
<span data-ttu-id="084d6-119">A CloudEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="084d6-119">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="084d6-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="084d6-120">-ParentObject</span></span>
<span data-ttu-id="084d6-121">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="084d6-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="084d6-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="084d6-122">-ParentResourceId</span></span>
<span data-ttu-id="084d6-123">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="084d6-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="084d6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="084d6-124">-ResourceGroupName</span></span>
<span data-ttu-id="084d6-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="084d6-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="084d6-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="084d6-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="084d6-127">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="084d6-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="084d6-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="084d6-128">-SyncGroupName</span></span>
<span data-ttu-id="084d6-129">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="084d6-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="084d6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084d6-130">CommonParameters</span></span>
<span data-ttu-id="084d6-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="084d6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="084d6-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="084d6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084d6-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="084d6-133">INPUTS</span></span>

### <span data-ttu-id="084d6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="084d6-134">System.String</span></span>

### <span data-ttu-id="084d6-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="084d6-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="084d6-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="084d6-136">OUTPUTS</span></span>

### <span data-ttu-id="084d6-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="084d6-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="084d6-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="084d6-138">NOTES</span></span>

## <span data-ttu-id="084d6-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="084d6-139">RELATED LINKS</span></span>

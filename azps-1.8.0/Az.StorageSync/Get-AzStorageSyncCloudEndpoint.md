---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: decf935cd61c052e2e77dd8fd2eadacd7a548974
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668505"
---
# <span data-ttu-id="334e3-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="334e3-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="334e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="334e3-102">SYNOPSIS</span></span>
<span data-ttu-id="334e3-103">Ez a parancs felsorolja az összes Felhőbeli végpontot egy adott szinkronizálási csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="334e3-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="334e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="334e3-104">SYNTAX</span></span>

### <span data-ttu-id="334e3-105">ObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="334e3-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="334e3-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="334e3-106">StringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="334e3-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="334e3-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="334e3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="334e3-108">DESCRIPTION</span></span>
<span data-ttu-id="334e3-109">Ez a parancs felsorolja az összes Felhőbeli végpontot egy adott szinkronizálási csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="334e3-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="334e3-110">Az egyes Felhőbeli végpontok attribútumait is használhatja.</span><span class="sxs-lookup"><span data-stu-id="334e3-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="334e3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="334e3-111">EXAMPLES</span></span>

### <span data-ttu-id="334e3-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="334e3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="334e3-113">Ez a parancs a megadott szinkronizálási csoportban található összes Felhőbeli végpontot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="334e3-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="334e3-114">A-CloudEndpointName, ha egy adott értéket szeretne visszaadni.</span><span class="sxs-lookup"><span data-stu-id="334e3-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="334e3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="334e3-115">PARAMETERS</span></span>

### <span data-ttu-id="334e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="334e3-116">-DefaultProfile</span></span>
<span data-ttu-id="334e3-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="334e3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="334e3-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="334e3-118">-Name</span></span>
<span data-ttu-id="334e3-119">A CloudEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="334e3-119">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="334e3-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="334e3-120">-ParentObject</span></span>
<span data-ttu-id="334e3-121">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="334e3-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="334e3-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="334e3-122">-ParentResourceId</span></span>
<span data-ttu-id="334e3-123">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="334e3-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="334e3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="334e3-124">-ResourceGroupName</span></span>
<span data-ttu-id="334e3-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="334e3-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="334e3-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="334e3-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="334e3-127">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="334e3-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="334e3-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="334e3-128">-SyncGroupName</span></span>
<span data-ttu-id="334e3-129">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="334e3-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="334e3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="334e3-130">CommonParameters</span></span>
<span data-ttu-id="334e3-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="334e3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="334e3-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="334e3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="334e3-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="334e3-133">INPUTS</span></span>

### <span data-ttu-id="334e3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="334e3-134">System.String</span></span>

### <span data-ttu-id="334e3-135">Microsoft. Azure. Command. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="334e3-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="334e3-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="334e3-136">OUTPUTS</span></span>

### <span data-ttu-id="334e3-137">Microsoft. Azure. Command. StorageSync. models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="334e3-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="334e3-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="334e3-138">NOTES</span></span>

## <span data-ttu-id="334e3-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="334e3-139">RELATED LINKS</span></span>

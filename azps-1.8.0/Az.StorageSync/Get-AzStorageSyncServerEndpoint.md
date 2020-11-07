---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b71da416d7609f05d4716090dc8f09bf0ec0b084
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668500"
---
# <span data-ttu-id="dc39e-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc39e-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="dc39e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc39e-102">SYNOPSIS</span></span>
<span data-ttu-id="dc39e-103">Ez a parancs felsorolja az összes kiszolgáló-végpontot egy adott szinkronizálási csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="dc39e-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="dc39e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc39e-104">SYNTAX</span></span>

### <span data-ttu-id="dc39e-105">ObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc39e-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc39e-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc39e-106">StringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc39e-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc39e-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc39e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc39e-108">DESCRIPTION</span></span>
<span data-ttu-id="dc39e-109">Ez a parancs felsorolja az összes kiszolgáló-végpontot egy adott szinkronizálási csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="dc39e-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="dc39e-110">Az egyes kiszolgálói végpontok attribútumait is használhatja.</span><span class="sxs-lookup"><span data-stu-id="dc39e-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="dc39e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="dc39e-111">EXAMPLES</span></span>

### <span data-ttu-id="dc39e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dc39e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="dc39e-113">Ez a parancs a megadott szinkronizálási csoportban található összes kiszolgálói végpontot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="dc39e-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="dc39e-114">A-ServerEndpointName, ha egy adott értéket szeretne visszaadni.</span><span class="sxs-lookup"><span data-stu-id="dc39e-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="dc39e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc39e-115">PARAMETERS</span></span>

### <span data-ttu-id="dc39e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc39e-116">-DefaultProfile</span></span>
<span data-ttu-id="dc39e-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc39e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc39e-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dc39e-118">-Name</span></span>
<span data-ttu-id="dc39e-119">A kiszolgáló végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="dc39e-119">Name of the server endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc39e-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dc39e-120">-ParentObject</span></span>
<span data-ttu-id="dc39e-121">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="dc39e-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="dc39e-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dc39e-122">-ParentResourceId</span></span>
<span data-ttu-id="dc39e-123">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="dc39e-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="dc39e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc39e-124">-ResourceGroupName</span></span>
<span data-ttu-id="dc39e-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="dc39e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="dc39e-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="dc39e-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="dc39e-127">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="dc39e-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="dc39e-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="dc39e-128">-SyncGroupName</span></span>
<span data-ttu-id="dc39e-129">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="dc39e-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="dc39e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc39e-130">CommonParameters</span></span>
<span data-ttu-id="dc39e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc39e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc39e-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc39e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc39e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc39e-133">INPUTS</span></span>

### <span data-ttu-id="dc39e-134">Microsoft. Azure. Command. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="dc39e-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="dc39e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dc39e-135">System.String</span></span>

## <span data-ttu-id="dc39e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc39e-136">OUTPUTS</span></span>

### <span data-ttu-id="dc39e-137">Microsoft. Azure. Command. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc39e-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="dc39e-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc39e-138">NOTES</span></span>

## <span data-ttu-id="dc39e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc39e-139">RELATED LINKS</span></span>

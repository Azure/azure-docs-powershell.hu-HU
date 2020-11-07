---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 35a3e8c3eecfe8e710addde0eb2080aa20333f0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845782"
---
# <span data-ttu-id="59e21-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="59e21-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="59e21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59e21-102">SYNOPSIS</span></span>
<span data-ttu-id="59e21-103">Ez a parancs felsorolja az összes kiszolgáló-végpontot egy adott szinkronizálási csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="59e21-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="59e21-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59e21-104">SYNTAX</span></span>

### <span data-ttu-id="59e21-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="59e21-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59e21-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59e21-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59e21-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="59e21-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59e21-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="59e21-108">DESCRIPTION</span></span>
<span data-ttu-id="59e21-109">Ez a parancs felsorolja az összes kiszolgáló-végpontot egy adott szinkronizálási csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="59e21-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="59e21-110">Az egyes kiszolgálói végpontok attribútumait is használhatja.</span><span class="sxs-lookup"><span data-stu-id="59e21-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="59e21-111">Példák</span><span class="sxs-lookup"><span data-stu-id="59e21-111">EXAMPLES</span></span>

### <span data-ttu-id="59e21-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="59e21-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="59e21-113">Ez a parancs a megadott szinkronizálási csoportban található összes kiszolgálói végpontot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="59e21-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="59e21-114">A-ServerEndpointName, ha egy adott értéket szeretne visszaadni.</span><span class="sxs-lookup"><span data-stu-id="59e21-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="59e21-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59e21-115">PARAMETERS</span></span>

### <span data-ttu-id="59e21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59e21-116">-DefaultProfile</span></span>
<span data-ttu-id="59e21-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59e21-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59e21-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59e21-118">-Name</span></span>
<span data-ttu-id="59e21-119">A kiszolgáló végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="59e21-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="59e21-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="59e21-120">-ParentObject</span></span>
<span data-ttu-id="59e21-121">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="59e21-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="59e21-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="59e21-122">-ParentResourceId</span></span>
<span data-ttu-id="59e21-123">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="59e21-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="59e21-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59e21-124">-ResourceGroupName</span></span>
<span data-ttu-id="59e21-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="59e21-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="59e21-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="59e21-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="59e21-127">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="59e21-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="59e21-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="59e21-128">-SyncGroupName</span></span>
<span data-ttu-id="59e21-129">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="59e21-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="59e21-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e21-130">CommonParameters</span></span>
<span data-ttu-id="59e21-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59e21-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e21-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59e21-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e21-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59e21-133">INPUTS</span></span>

### <span data-ttu-id="59e21-134">Microsoft. Azure. Command. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="59e21-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="59e21-135">System. String</span><span class="sxs-lookup"><span data-stu-id="59e21-135">System.String</span></span>

## <span data-ttu-id="59e21-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59e21-136">OUTPUTS</span></span>

### <span data-ttu-id="59e21-137">Microsoft. Azure. Command. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="59e21-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="59e21-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59e21-138">NOTES</span></span>

## <span data-ttu-id="59e21-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59e21-139">RELATED LINKS</span></span>

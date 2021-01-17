---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 35a3e8c3eecfe8e710addde0eb2080aa20333f0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466868"
---
# <span data-ttu-id="9bd62-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9bd62-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="9bd62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bd62-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd62-103">Ez a parancs felsorolja egy adott szinkronizálási csoport összes kiszolgálói végpontját.</span><span class="sxs-lookup"><span data-stu-id="9bd62-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="9bd62-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9bd62-104">SYNTAX</span></span>

### <span data-ttu-id="9bd62-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9bd62-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bd62-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd62-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bd62-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd62-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bd62-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9bd62-108">DESCRIPTION</span></span>
<span data-ttu-id="9bd62-109">Ez a parancs felsorolja egy adott szinkronizálási csoport összes kiszolgálói végpontját.</span><span class="sxs-lookup"><span data-stu-id="9bd62-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="9bd62-110">Az egyes kiszolgálói végpontok attribútumainak felsorolásához is használható.</span><span class="sxs-lookup"><span data-stu-id="9bd62-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="9bd62-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9bd62-111">EXAMPLES</span></span>

### <span data-ttu-id="9bd62-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="9bd62-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="9bd62-113">Ez a parancs a megadott szinkronizálási csoportban található összes kiszolgálói végpontot beveszi.</span><span class="sxs-lookup"><span data-stu-id="9bd62-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="9bd62-114">A -ServerEndpointName paramétert megadásával adott értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="9bd62-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="9bd62-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bd62-115">PARAMETERS</span></span>

### <span data-ttu-id="9bd62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd62-116">-DefaultProfile</span></span>
<span data-ttu-id="9bd62-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9bd62-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bd62-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9bd62-118">-Name</span></span>
<span data-ttu-id="9bd62-119">A kiszolgáló végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="9bd62-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="9bd62-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9bd62-120">-ParentObject</span></span>
<span data-ttu-id="9bd62-121">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="9bd62-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="9bd62-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9bd62-122">-ParentResourceId</span></span>
<span data-ttu-id="9bd62-123">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="9bd62-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="9bd62-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd62-124">-ResourceGroupName</span></span>
<span data-ttu-id="9bd62-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9bd62-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="9bd62-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="9bd62-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="9bd62-127">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="9bd62-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="9bd62-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd62-128">-SyncGroupName</span></span>
<span data-ttu-id="9bd62-129">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="9bd62-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="9bd62-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd62-130">CommonParameters</span></span>
<span data-ttu-id="9bd62-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd62-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd62-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd62-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd62-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9bd62-133">INPUTS</span></span>

### <span data-ttu-id="9bd62-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9bd62-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="9bd62-135">System.String</span><span class="sxs-lookup"><span data-stu-id="9bd62-135">System.String</span></span>

## <span data-ttu-id="9bd62-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bd62-136">OUTPUTS</span></span>

### <span data-ttu-id="9bd62-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9bd62-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="9bd62-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9bd62-138">NOTES</span></span>

## <span data-ttu-id="9bd62-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bd62-139">RELATED LINKS</span></span>

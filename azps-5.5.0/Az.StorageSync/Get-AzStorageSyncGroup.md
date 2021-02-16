---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150347"
---
# <span data-ttu-id="38bc2-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="38bc2-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="38bc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="38bc2-103">Ez a parancs felsorolja az adott tár szinkronizálási szolgáltatásában található összes szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="38bc2-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="38bc2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="38bc2-104">SYNTAX</span></span>

### <span data-ttu-id="38bc2-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38bc2-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38bc2-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38bc2-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38bc2-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="38bc2-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38bc2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="38bc2-108">DESCRIPTION</span></span>
<span data-ttu-id="38bc2-109">Ez a parancs felsorolja az adott tár szinkronizálási szolgáltatásában található összes szinkronizálási csoportot.</span><span class="sxs-lookup"><span data-stu-id="38bc2-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="38bc2-110">Az egyes szinkronizálási csoportok attribútumainak felsorolásához is használható.</span><span class="sxs-lookup"><span data-stu-id="38bc2-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="38bc2-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="38bc2-111">EXAMPLES</span></span>

### <span data-ttu-id="38bc2-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="38bc2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="38bc2-113">Ez a parancs a megadott tár szinkronizálási szolgáltatásban található összes szinkronizálási csoportot lekérte.</span><span class="sxs-lookup"><span data-stu-id="38bc2-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="38bc2-114">A -Name értéket megadásával adott értéket ad vissza.</span><span class="sxs-lookup"><span data-stu-id="38bc2-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="38bc2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38bc2-115">PARAMETERS</span></span>

### <span data-ttu-id="38bc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bc2-116">-DefaultProfile</span></span>
<span data-ttu-id="38bc2-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38bc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38bc2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="38bc2-118">-Name</span></span>
<span data-ttu-id="38bc2-119">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="38bc2-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="38bc2-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="38bc2-120">-ParentObject</span></span>
<span data-ttu-id="38bc2-121">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="38bc2-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="38bc2-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="38bc2-122">-ParentResourceId</span></span>
<span data-ttu-id="38bc2-123">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="38bc2-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="38bc2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38bc2-124">-ResourceGroupName</span></span>
<span data-ttu-id="38bc2-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="38bc2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="38bc2-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="38bc2-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="38bc2-127">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="38bc2-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="38bc2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bc2-128">CommonParameters</span></span>
<span data-ttu-id="38bc2-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38bc2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bc2-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38bc2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bc2-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38bc2-131">INPUTS</span></span>

### <span data-ttu-id="38bc2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="38bc2-132">System.String</span></span>

### <span data-ttu-id="38bc2-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="38bc2-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="38bc2-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38bc2-134">OUTPUTS</span></span>

### <span data-ttu-id="38bc2-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="38bc2-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="38bc2-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="38bc2-136">NOTES</span></span>

## <span data-ttu-id="38bc2-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38bc2-137">RELATED LINKS</span></span>

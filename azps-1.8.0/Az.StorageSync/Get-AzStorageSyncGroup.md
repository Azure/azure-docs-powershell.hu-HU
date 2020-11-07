---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: 34e3033d1f5ce76d6d6c42aaacd5ced690b5d47c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668502"
---
# <span data-ttu-id="9b220-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9b220-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="9b220-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b220-102">SYNOPSIS</span></span>
<span data-ttu-id="9b220-103">Ez a parancs felsorolja az összes szinkronizálási csoportot egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="9b220-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="9b220-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b220-104">SYNTAX</span></span>

### <span data-ttu-id="9b220-105">ObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b220-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b220-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b220-106">StringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b220-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b220-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b220-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b220-108">DESCRIPTION</span></span>
<span data-ttu-id="9b220-109">Ez a parancs felsorolja az összes szinkronizálási csoportot egy adott tárterület-szinkronizálási szolgáltatáson belül.</span><span class="sxs-lookup"><span data-stu-id="9b220-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="9b220-110">Használható az egyes szinkronizálási csoportok attribútumainak a felsorolására is.</span><span class="sxs-lookup"><span data-stu-id="9b220-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="9b220-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9b220-111">EXAMPLES</span></span>

### <span data-ttu-id="9b220-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9b220-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="9b220-113">Ez a parancs a megadott tárterület-szinkronizálási szolgáltatásban található összes szinkronizálási csoportot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="9b220-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="9b220-114">Adja meg a nevet egy adott érték visszaadásához.</span><span class="sxs-lookup"><span data-stu-id="9b220-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="9b220-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b220-115">PARAMETERS</span></span>

### <span data-ttu-id="9b220-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b220-116">-DefaultProfile</span></span>
<span data-ttu-id="9b220-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b220-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b220-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9b220-118">-Name</span></span>
<span data-ttu-id="9b220-119">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="9b220-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="9b220-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9b220-120">-ParentObject</span></span>
<span data-ttu-id="9b220-121">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="9b220-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="9b220-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9b220-122">-ParentResourceId</span></span>
<span data-ttu-id="9b220-123">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="9b220-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="9b220-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b220-124">-ResourceGroupName</span></span>
<span data-ttu-id="9b220-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9b220-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="9b220-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="9b220-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="9b220-127">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="9b220-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="9b220-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b220-128">CommonParameters</span></span>
<span data-ttu-id="9b220-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b220-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b220-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b220-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b220-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b220-131">INPUTS</span></span>

### <span data-ttu-id="9b220-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9b220-132">System.String</span></span>

### <span data-ttu-id="9b220-133">Microsoft. Azure. Command. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="9b220-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="9b220-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b220-134">OUTPUTS</span></span>

### <span data-ttu-id="9b220-135">Microsoft. Azure. Command. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9b220-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="9b220-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b220-136">NOTES</span></span>

## <span data-ttu-id="9b220-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b220-137">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: 0476a881ec1ee479b97dad4ab8dcf95121dd5302
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302887"
---
# <span data-ttu-id="270dc-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="270dc-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="270dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="270dc-102">SYNOPSIS</span></span>
<span data-ttu-id="270dc-103">A parancs új tárterület-szinkronizálási szolgáltatást hoz létre egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="270dc-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="270dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="270dc-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-IncomingTrafficPolicy] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="270dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="270dc-105">DESCRIPTION</span></span>
<span data-ttu-id="270dc-106">A tárterület-szinkronizálási szolgáltatás a legfelső szintű erőforrás az Azure-fájlok szinkronizálásához. A parancs új tárterület-szinkronizálási szolgáltatást hoz létre egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="270dc-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="270dc-107">Azt javasoljuk, hogy minden olyan tárterület-szinkronizáló szolgáltatást hozzon létre, amely feltétlenül szükséges a szervezet különböző csoportjai közötti különbségtételhez.</span><span class="sxs-lookup"><span data-stu-id="270dc-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="270dc-108">A tárterület-szinkronizálási szolgáltatás szinkronizálási csoportokat tartalmaz, és a kiszolgálók regisztrálására szolgáló célként is használható.</span><span class="sxs-lookup"><span data-stu-id="270dc-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="270dc-109">A kiszolgálók csak egyetlen tárterület-szinkronizáló szolgáltatásban regisztrálhatók.</span><span class="sxs-lookup"><span data-stu-id="270dc-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="270dc-110">Ha a kiszolgálókhoz ugyanazon fájlok szinkronizálásához is szüksége van, regisztrálja őket ugyanabba a tárterület-szinkronizálási szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="270dc-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="270dc-111">Példák</span><span class="sxs-lookup"><span data-stu-id="270dc-111">EXAMPLES</span></span>

### <span data-ttu-id="270dc-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="270dc-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="270dc-113">Ez a parancs tárterület-szinkronizálási szolgáltatást fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="270dc-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="270dc-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="270dc-114">PARAMETERS</span></span>

### <span data-ttu-id="270dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="270dc-115">-DefaultProfile</span></span>
<span data-ttu-id="270dc-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="270dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="270dc-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="270dc-117">-Location</span></span>
<span data-ttu-id="270dc-118">A tárterület-szinkronizálási szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="270dc-118">Storage Sync Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270dc-119">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="270dc-119">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="270dc-120">A tárterület-szinkronizálási szolgáltatás IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="270dc-120">Storage Sync Service IncomingTrafficPolicy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270dc-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="270dc-121">-Name</span></span>
<span data-ttu-id="270dc-122">A tárterület-szinkronizálási szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="270dc-122">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270dc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="270dc-123">-ResourceGroupName</span></span>
<span data-ttu-id="270dc-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="270dc-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270dc-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="270dc-125">-Tag</span></span>
<span data-ttu-id="270dc-126">A tárterület-szinkronizálási szolgáltatás címkéi.</span><span class="sxs-lookup"><span data-stu-id="270dc-126">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="270dc-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="270dc-127">-Confirm</span></span>
<span data-ttu-id="270dc-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="270dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="270dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="270dc-129">-WhatIf</span></span>
<span data-ttu-id="270dc-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="270dc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="270dc-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="270dc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="270dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270dc-132">CommonParameters</span></span>
<span data-ttu-id="270dc-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="270dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270dc-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="270dc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270dc-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="270dc-135">INPUTS</span></span>

### <span data-ttu-id="270dc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="270dc-136">System.String</span></span>

## <span data-ttu-id="270dc-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="270dc-137">OUTPUTS</span></span>

### <span data-ttu-id="270dc-138">Microsoft. Azure. Command. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="270dc-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="270dc-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="270dc-139">NOTES</span></span>

## <span data-ttu-id="270dc-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="270dc-140">RELATED LINKS</span></span>

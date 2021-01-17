---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: 0476a881ec1ee479b97dad4ab8dcf95121dd5302
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466854"
---
# <span data-ttu-id="f6fa2-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f6fa2-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="f6fa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="f6fa2-103">Ez a parancs új tárterület-szinkronizálási szolgáltatást hoz létre egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="f6fa2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f6fa2-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-IncomingTrafficPolicy] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6fa2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f6fa2-105">DESCRIPTION</span></span>
<span data-ttu-id="f6fa2-106">A tárterület-szinkronizálási szolgáltatás az Azure File Sync legfelső szintű erőforrása. Ez a parancs új tárterület-szinkronizálási szolgáltatást hoz létre egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="f6fa2-107">Azt javasoljuk, hogy hozzon létre annyi tárterület-szinkronizálási szolgáltatást, amennyit feltétlenül szükséges a szervezet kiszolgálói csoportjainak megkülönböztetésére.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="f6fa2-108">A tárterület-szinkronizálási szolgáltatás szinkronizálási csoportokat tartalmaz, és célként is működik a kiszolgálók regisztrálására.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="f6fa2-109">Egy kiszolgáló csak egyetlen tárterület-szinkronizálási szolgáltatásba regisztrálható.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="f6fa2-110">Ha a kiszolgálóknak részt kell venniük ugyanazon fájlkészlet szinkronizálásában, regisztrálja őket ugyanannak a tárhelyszinkronizálási szolgáltatásnak.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="f6fa2-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f6fa2-111">EXAMPLES</span></span>

### <span data-ttu-id="f6fa2-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="f6fa2-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="f6fa2-113">Ez a parancs tárterület-szinkronizálási szolgáltatást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="f6fa2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6fa2-114">PARAMETERS</span></span>

### <span data-ttu-id="f6fa2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6fa2-115">-DefaultProfile</span></span>
<span data-ttu-id="f6fa2-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6fa2-117">-Location</span><span class="sxs-lookup"><span data-stu-id="f6fa2-117">-Location</span></span>
<span data-ttu-id="f6fa2-118">Tárterület-szinkronizálási szolgáltatás helye.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-118">Storage Sync Service location.</span></span>

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

### <span data-ttu-id="f6fa2-119">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="f6fa2-119">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="f6fa2-120">Storage Sync Service IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="f6fa2-120">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="f6fa2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f6fa2-121">-Name</span></span>
<span data-ttu-id="f6fa2-122">A tárterület-szinkronizálási szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-122">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="f6fa2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6fa2-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6fa2-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="f6fa2-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="f6fa2-125">-Tag</span></span>
<span data-ttu-id="f6fa2-126">Tárterület-szinkronizálási szolgáltatás címkéi.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-126">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="f6fa2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6fa2-127">-Confirm</span></span>
<span data-ttu-id="f6fa2-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6fa2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6fa2-129">-WhatIf</span></span>
<span data-ttu-id="f6fa2-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6fa2-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6fa2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6fa2-132">CommonParameters</span></span>
<span data-ttu-id="f6fa2-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6fa2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6fa2-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6fa2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6fa2-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6fa2-135">INPUTS</span></span>

### <span data-ttu-id="f6fa2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f6fa2-136">System.String</span></span>

## <span data-ttu-id="f6fa2-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6fa2-137">OUTPUTS</span></span>

### <span data-ttu-id="f6fa2-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f6fa2-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="f6fa2-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f6fa2-139">NOTES</span></span>

## <span data-ttu-id="f6fa2-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6fa2-140">RELATED LINKS</span></span>

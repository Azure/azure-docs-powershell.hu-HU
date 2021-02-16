---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150306"
---
# <span data-ttu-id="d6c3b-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="d6c3b-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="d6c3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="d6c3b-103">Ez a parancs beállítja a tárterület-szinkronizálási szolgáltatást egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="d6c3b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d6c3b-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6c3b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d6c3b-105">DESCRIPTION</span></span>
<span data-ttu-id="d6c3b-106">A tárterület-szinkronizálási szolgáltatás az Azure File Sync legfelső szintű erőforrása. Ez a parancs beállítja a tárterület-szinkronizálási szolgáltatást egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="d6c3b-107">Azt javasoljuk, hogy hozzon létre annyi tárterület-szinkronizálási szolgáltatást, amennyit feltétlenül szükséges a szervezet kiszolgálói csoportjainak megkülönböztetésére.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="d6c3b-108">A tárterület-szinkronizálási szolgáltatás szinkronizálási csoportokat tartalmaz, és célként is működik a kiszolgálók regisztrálására.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="d6c3b-109">Egy kiszolgáló csak egyetlen tárterület-szinkronizálási szolgáltatásba regisztrálható.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="d6c3b-110">Ha a kiszolgálóknak részt kell venniük ugyanazon fájlkészlet szinkronizálásában, regisztrálja őket ugyanannak a tárhelyszinkronizálási szolgáltatásnak.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="d6c3b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d6c3b-111">EXAMPLES</span></span>

### <span data-ttu-id="d6c3b-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="d6c3b-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="d6c3b-113">Ezzel a paranccsal tárhelyszinkronizálási szolgáltatást állíthat be.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="d6c3b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6c3b-114">PARAMETERS</span></span>

### <span data-ttu-id="d6c3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6c3b-115">-DefaultProfile</span></span>
<span data-ttu-id="d6c3b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="d6c3b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d6c3b-117">-Name</span></span>
<span data-ttu-id="d6c3b-118">A tárterület-szinkronizálási szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="d6c3b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6c3b-119">-ResourceGroupName</span></span>
<span data-ttu-id="d6c3b-120">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="d6c3b-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="d6c3b-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="d6c3b-122">Storage Sync Service IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="d6c3b-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="d6c3b-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="d6c3b-123">-Tag</span></span>
<span data-ttu-id="d6c3b-124">Tárterület-szinkronizálási szolgáltatás címkéi.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="d6c3b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6c3b-125">-Confirm</span></span>
<span data-ttu-id="d6c3b-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6c3b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6c3b-127">-WhatIf</span></span>
<span data-ttu-id="d6c3b-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6c3b-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6c3b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6c3b-130">CommonParameters</span></span>
<span data-ttu-id="d6c3b-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6c3b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6c3b-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6c3b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6c3b-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6c3b-133">INPUTS</span></span>

### <span data-ttu-id="d6c3b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d6c3b-134">System.String</span></span>

## <span data-ttu-id="d6c3b-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6c3b-135">OUTPUTS</span></span>

### <span data-ttu-id="d6c3b-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="d6c3b-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="d6c3b-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d6c3b-137">NOTES</span></span>

## <span data-ttu-id="d6c3b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6c3b-138">RELATED LINKS</span></span>

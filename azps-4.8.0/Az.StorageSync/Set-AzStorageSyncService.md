---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181252"
---
# <span data-ttu-id="63df5-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="63df5-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="63df5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63df5-102">SYNOPSIS</span></span>
<span data-ttu-id="63df5-103">Ez a parancs egy erőforráscsoport tárterület-szinkronizálási szolgáltatását állítja be.</span><span class="sxs-lookup"><span data-stu-id="63df5-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="63df5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63df5-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63df5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="63df5-105">DESCRIPTION</span></span>
<span data-ttu-id="63df5-106">A tárterület-szinkronizálási szolgáltatás a legfelső szintű erőforrás az Azure-fájlok szinkronizálásához. Ez a parancs egy erőforráscsoport tárterület-szinkronizálási szolgáltatását állítja be.</span><span class="sxs-lookup"><span data-stu-id="63df5-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="63df5-107">Azt javasoljuk, hogy minden olyan tárterület-szinkronizáló szolgáltatást hozzon létre, amely feltétlenül szükséges a szervezet különböző csoportjai közötti különbségtételhez.</span><span class="sxs-lookup"><span data-stu-id="63df5-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="63df5-108">A tárterület-szinkronizálási szolgáltatás szinkronizálási csoportokat tartalmaz, és a kiszolgálók regisztrálására szolgáló célként is használható.</span><span class="sxs-lookup"><span data-stu-id="63df5-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="63df5-109">A kiszolgálók csak egyetlen tárterület-szinkronizáló szolgáltatásban regisztrálhatók.</span><span class="sxs-lookup"><span data-stu-id="63df5-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="63df5-110">Ha a kiszolgálókhoz ugyanazon fájlok szinkronizálásához is szüksége van, regisztrálja őket ugyanabba a tárterület-szinkronizálási szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="63df5-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="63df5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="63df5-111">EXAMPLES</span></span>

### <span data-ttu-id="63df5-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="63df5-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="63df5-113">Ez a parancs a tárterület-szinkronizálási szolgáltatást fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="63df5-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="63df5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63df5-114">PARAMETERS</span></span>

### <span data-ttu-id="63df5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63df5-115">-DefaultProfile</span></span>
<span data-ttu-id="63df5-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63df5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="63df5-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="63df5-117">-Name</span></span>
<span data-ttu-id="63df5-118">A tárterület-szinkronizálási szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="63df5-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="63df5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63df5-119">-ResourceGroupName</span></span>
<span data-ttu-id="63df5-120">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="63df5-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="63df5-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="63df5-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="63df5-122">A tárterület-szinkronizálási szolgáltatás IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="63df5-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="63df5-123">-Címke</span><span class="sxs-lookup"><span data-stu-id="63df5-123">-Tag</span></span>
<span data-ttu-id="63df5-124">A tárterület-szinkronizálási szolgáltatás címkéi.</span><span class="sxs-lookup"><span data-stu-id="63df5-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="63df5-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="63df5-125">-Confirm</span></span>
<span data-ttu-id="63df5-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="63df5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63df5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63df5-127">-WhatIf</span></span>
<span data-ttu-id="63df5-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="63df5-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63df5-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63df5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63df5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63df5-130">CommonParameters</span></span>
<span data-ttu-id="63df5-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63df5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63df5-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63df5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63df5-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63df5-133">INPUTS</span></span>

### <span data-ttu-id="63df5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="63df5-134">System.String</span></span>

## <span data-ttu-id="63df5-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63df5-135">OUTPUTS</span></span>

### <span data-ttu-id="63df5-136">Microsoft. Azure. Command. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="63df5-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="63df5-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63df5-137">NOTES</span></span>

## <span data-ttu-id="63df5-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63df5-138">RELATED LINKS</span></span>

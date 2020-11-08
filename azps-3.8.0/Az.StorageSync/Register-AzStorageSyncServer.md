---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: bb1ce6f9ff7e846c2f485665cafad700fa4c825b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013121"
---
# <span data-ttu-id="8986f-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="8986f-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="8986f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8986f-102">SYNOPSIS</span></span>
<span data-ttu-id="8986f-103">Ez a parancs a kiszolgálót egy olyan tárterület-szinkronizáló szolgáltatáshoz regisztrálja, amely bizalmi kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8986f-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="8986f-104">Ezt követően a PowerShell vagy az Azure portál segítségével konfigurálhatja a szinkronizálást a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="8986f-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="8986f-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8986f-105">SYNTAX</span></span>

### <span data-ttu-id="8986f-106">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8986f-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8986f-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8986f-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8986f-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="8986f-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8986f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="8986f-109">DESCRIPTION</span></span>
<span data-ttu-id="8986f-110">Ez a parancs a kiszolgálót egy tárterület-szinkronizáló szolgáltatáshoz, az Azure-fájlok szinkronizálásához szükséges legfelső szintű erőforráshoz regisztrálja. Létrejön egy bizalmi kapcsolat a kiszolgáló és a tárterület-szinkronizáló szolgáltatás között, amely biztosítja az adatátviteli és-kezelési csatornák biztonságát.</span><span class="sxs-lookup"><span data-stu-id="8986f-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="8986f-111">A PowerShell vagy az Azure portál segítségével beállíthatja, hogy a kiszolgálón milyen szinkronizálások legyenek.</span><span class="sxs-lookup"><span data-stu-id="8986f-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="8986f-112">A kiszolgálók csak egyetlen tárterület-szinkronizáló szolgáltatásban regisztrálhatók.</span><span class="sxs-lookup"><span data-stu-id="8986f-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="8986f-113">Ha a kiszolgálókhoz ugyanazon fájlok szinkronizálásához is szüksége van, regisztrálja őket ugyanabba a tárterület-szinkronizálási szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="8986f-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="8986f-114">A parancsot helyileg kell futtatni abban a kiszolgálón, amelyet regisztrálni kell, vagy közvetlenül vagy távoli PowerShell-munkameneten keresztül kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="8986f-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="8986f-115">A távoli számítógép-objektum nem fogadható el.</span><span class="sxs-lookup"><span data-stu-id="8986f-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="8986f-116">Példák</span><span class="sxs-lookup"><span data-stu-id="8986f-116">EXAMPLES</span></span>

### <span data-ttu-id="8986f-117">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8986f-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="8986f-118">Ez a parancs rögzíti a helyi kiszolgálót, amelyre a parancs fut.</span><span class="sxs-lookup"><span data-stu-id="8986f-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="8986f-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8986f-119">PARAMETERS</span></span>

### <span data-ttu-id="8986f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8986f-120">-AsJob</span></span>
<span data-ttu-id="8986f-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8986f-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8986f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8986f-122">-DefaultProfile</span></span>
<span data-ttu-id="8986f-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8986f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8986f-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8986f-124">-ParentObject</span></span>
<span data-ttu-id="8986f-125">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="8986f-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="8986f-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8986f-126">-ParentResourceId</span></span>
<span data-ttu-id="8986f-127">A StorageSyncService szülő erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8986f-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="8986f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8986f-128">-ResourceGroupName</span></span>
<span data-ttu-id="8986f-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="8986f-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="8986f-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="8986f-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="8986f-131">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="8986f-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="8986f-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8986f-132">-Confirm</span></span>
<span data-ttu-id="8986f-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8986f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8986f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8986f-134">-WhatIf</span></span>
<span data-ttu-id="8986f-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8986f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8986f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8986f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8986f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8986f-137">CommonParameters</span></span>
<span data-ttu-id="8986f-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8986f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8986f-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8986f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8986f-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8986f-140">INPUTS</span></span>

### <span data-ttu-id="8986f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8986f-141">System.String</span></span>

### <span data-ttu-id="8986f-142">Microsoft. Azure. Command. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="8986f-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="8986f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8986f-143">OUTPUTS</span></span>

### <span data-ttu-id="8986f-144">Microsoft. Azure. Command. StorageSync. models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="8986f-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="8986f-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8986f-145">NOTES</span></span>

## <span data-ttu-id="8986f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8986f-146">RELATED LINKS</span></span>

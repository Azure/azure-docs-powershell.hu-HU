---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: bb1ce6f9ff7e846c2f485665cafad700fa4c825b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366602"
---
# <span data-ttu-id="ba656-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="ba656-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="ba656-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba656-102">SYNOPSIS</span></span>
<span data-ttu-id="ba656-103">Ez a parancs regisztrál egy kiszolgálót egy tárterület-szinkronizálási szolgáltatásban, amely megbízhatósági kapcsolatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ba656-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="ba656-104">Ezután a PowerShell vagy az Azure Portal segítségével konfigurálhatja a szinkronizálást ezen a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="ba656-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="ba656-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ba656-105">SYNTAX</span></span>

### <span data-ttu-id="ba656-106">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba656-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba656-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba656-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba656-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba656-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba656-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ba656-109">DESCRIPTION</span></span>
<span data-ttu-id="ba656-110">Ez a parancs regisztrál egy kiszolgálót egy tárterület-szinkronizálási szolgáltatásban, amely az Azure File Sync legfelső szintű erőforrása. Létrejön egy megbízhatósági kapcsolat a kiszolgáló és a tárterület-szinkronizálási szolgáltatás között, amely biztosítja a biztonságos adatátviteli és kezelési csatornákat.</span><span class="sxs-lookup"><span data-stu-id="ba656-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="ba656-111">Ezután a PowerShell vagy az Azure Portal segítségével konfigurálhatja a kiszolgálón található szinkronizálásokat.</span><span class="sxs-lookup"><span data-stu-id="ba656-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="ba656-112">Egy kiszolgáló csak egyetlen tárterület-szinkronizálási szolgáltatásba regisztrálható.</span><span class="sxs-lookup"><span data-stu-id="ba656-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="ba656-113">Ha a kiszolgálóknak részt kell venniük ugyanazon fájlkészlet szinkronizálásában, regisztrálja őket ugyanannak a tárhelyszinkronizálási szolgáltatásnak.</span><span class="sxs-lookup"><span data-stu-id="ba656-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="ba656-114">A parancsot helyben kell futtatni a regisztrálandó kiszolgálón – vagy közvetlenül, vagy egy távoli PowerShell-munkameneten keresztül.</span><span class="sxs-lookup"><span data-stu-id="ba656-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="ba656-115">Távoli számítógépes objektum nem fogadható el.</span><span class="sxs-lookup"><span data-stu-id="ba656-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="ba656-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ba656-116">EXAMPLES</span></span>

### <span data-ttu-id="ba656-117">1. példa</span><span class="sxs-lookup"><span data-stu-id="ba656-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="ba656-118">Ez a parancs regisztrálja azt a helyi kiszolgálót, amelyen a parancs fut.</span><span class="sxs-lookup"><span data-stu-id="ba656-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="ba656-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba656-119">PARAMETERS</span></span>

### <span data-ttu-id="ba656-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba656-120">-AsJob</span></span>
<span data-ttu-id="ba656-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ba656-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba656-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba656-122">-DefaultProfile</span></span>
<span data-ttu-id="ba656-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba656-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba656-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ba656-124">-ParentObject</span></span>
<span data-ttu-id="ba656-125">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="ba656-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ba656-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ba656-126">-ParentResourceId</span></span>
<span data-ttu-id="ba656-127">StorageSyncService szülőerőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="ba656-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="ba656-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba656-128">-ResourceGroupName</span></span>
<span data-ttu-id="ba656-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ba656-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="ba656-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ba656-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="ba656-131">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="ba656-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ba656-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba656-132">-Confirm</span></span>
<span data-ttu-id="ba656-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ba656-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba656-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba656-134">-WhatIf</span></span>
<span data-ttu-id="ba656-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ba656-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba656-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba656-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba656-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba656-137">CommonParameters</span></span>
<span data-ttu-id="ba656-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba656-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba656-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba656-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba656-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba656-140">INPUTS</span></span>

### <span data-ttu-id="ba656-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ba656-141">System.String</span></span>

### <span data-ttu-id="ba656-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ba656-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="ba656-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba656-143">OUTPUTS</span></span>

### <span data-ttu-id="ba656-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="ba656-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="ba656-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ba656-145">NOTES</span></span>

## <span data-ttu-id="ba656-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba656-146">RELATED LINKS</span></span>

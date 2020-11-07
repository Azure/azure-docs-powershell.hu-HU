---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 87734d63d28785282ad3285ef8cce0a574ba30e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668468"
---
# <span data-ttu-id="70260-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="70260-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="70260-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70260-102">SYNOPSIS</span></span>
<span data-ttu-id="70260-103">Figyelmeztetés: a kiszolgálók regisztrációjának megszüntetése a kiszolgálón futó összes kiszolgáló-végpontok lépcsőzetes törlését eredményezi.</span><span class="sxs-lookup"><span data-stu-id="70260-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="70260-104">Ez a parancs egy kiszolgáló regisztrációját fogja lemaradni a tárterület-szinkronizálási szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="70260-104">This command will unregister a server it's the storage sync service.</span></span>

## <span data-ttu-id="70260-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70260-105">SYNTAX</span></span>

### <span data-ttu-id="70260-106">InputObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70260-106">InputObjectParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70260-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70260-107">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70260-108">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="70260-108">StringParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70260-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="70260-109">DESCRIPTION</span></span>
<span data-ttu-id="70260-110">Ez a parancs a kiszolgáló regisztrációját a tárterület-szinkronizálási szolgáltatásból fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="70260-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="70260-111">Figyelmeztetés: a kiszolgálók regisztrációjának megszüntetése a kiszolgálón futó összes kiszolgáló-végpontok lépcsőzetes törlését eredményezi.</span><span class="sxs-lookup"><span data-stu-id="70260-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="70260-112">Csak akkor érdemes megnevezni, ha biztos benne, hogy a kiszolgálón nincs elérési út szinkronizálva van.</span><span class="sxs-lookup"><span data-stu-id="70260-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="70260-113">Példák</span><span class="sxs-lookup"><span data-stu-id="70260-113">EXAMPLES</span></span>

### <span data-ttu-id="70260-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="70260-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="70260-115">Ez a parancs megszünteti a kiszolgáló regisztrálását, így a kiszolgálón futó összes kiszolgálói végpont kaszkádolt törlését okozhatja.</span><span class="sxs-lookup"><span data-stu-id="70260-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="70260-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70260-116">PARAMETERS</span></span>

### <span data-ttu-id="70260-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70260-117">-AsJob</span></span>
<span data-ttu-id="70260-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="70260-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70260-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70260-119">-DefaultProfile</span></span>
<span data-ttu-id="70260-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70260-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70260-121">-Force</span><span class="sxs-lookup"><span data-stu-id="70260-121">-Force</span></span>
<span data-ttu-id="70260-122">Supply-Force: a parancs megerősítésének mellőzése.</span><span class="sxs-lookup"><span data-stu-id="70260-122">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70260-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70260-123">-InputObject</span></span>
<span data-ttu-id="70260-124">A RegisteredServer bemeneti objektuma, normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="70260-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70260-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70260-125">-PassThru</span></span>
<span data-ttu-id="70260-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="70260-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="70260-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70260-127">-ResourceGroupName</span></span>
<span data-ttu-id="70260-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="70260-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70260-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70260-129">-ResourceId</span></span>
<span data-ttu-id="70260-130">RegisteredServer erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="70260-130">RegisteredServer Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70260-131">-ServerId</span><span class="sxs-lookup"><span data-stu-id="70260-131">-ServerId</span></span>
<span data-ttu-id="70260-132">A RegisteredServer neve.</span><span class="sxs-lookup"><span data-stu-id="70260-132">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: StringParameterSet
Aliases: RegisteredServerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70260-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="70260-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="70260-134">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="70260-134">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70260-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70260-135">-Confirm</span></span>
<span data-ttu-id="70260-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70260-136">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70260-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70260-137">-WhatIf</span></span>
<span data-ttu-id="70260-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70260-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70260-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70260-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70260-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70260-140">CommonParameters</span></span>
<span data-ttu-id="70260-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70260-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70260-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70260-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70260-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70260-143">INPUTS</span></span>

### <span data-ttu-id="70260-144">Microsoft. Azure. Command. StorageSync. models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="70260-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="70260-145">System. String</span><span class="sxs-lookup"><span data-stu-id="70260-145">System.String</span></span>

### <span data-ttu-id="70260-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="70260-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="70260-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70260-147">OUTPUTS</span></span>

### <span data-ttu-id="70260-148">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="70260-148">System.Object</span></span>
## <span data-ttu-id="70260-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70260-149">NOTES</span></span>

## <span data-ttu-id="70260-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70260-150">RELATED LINKS</span></span>

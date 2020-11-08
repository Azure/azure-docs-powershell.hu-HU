---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: f6de2bf731bc11a4b0ec8b6c894e6d77569ec9ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185997"
---
# <span data-ttu-id="cb2ca-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="cb2ca-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="cb2ca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb2ca-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2ca-103">Figyelmeztetés: a kiszolgálók regisztrációjának megszüntetése a kiszolgálón futó összes kiszolgáló-végpontok lépcsőzetes törlését eredményezi.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="cb2ca-104">Ez a parancs töröl egy kiszolgálót a tárterület-szinkronizálási szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="cb2ca-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb2ca-105">SYNTAX</span></span>

### <span data-ttu-id="cb2ca-106">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb2ca-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb2ca-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb2ca-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb2ca-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb2ca-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb2ca-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb2ca-109">DESCRIPTION</span></span>
<span data-ttu-id="cb2ca-110">Ez a parancs a kiszolgáló regisztrációját a tárterület-szinkronizálási szolgáltatásból fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="cb2ca-111">Figyelmeztetés: a kiszolgálók regisztrációjának megszüntetése a kiszolgálón futó összes kiszolgáló-végpontok lépcsőzetes törlését eredményezi.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="cb2ca-112">Csak akkor érdemes megnevezni, ha biztos benne, hogy a kiszolgálón nincs elérési út szinkronizálva van.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="cb2ca-113">Példák</span><span class="sxs-lookup"><span data-stu-id="cb2ca-113">EXAMPLES</span></span>

### <span data-ttu-id="cb2ca-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cb2ca-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="cb2ca-115">Ez a parancs megszünteti a kiszolgáló regisztrálását, így a kiszolgálón futó összes kiszolgálói végpont kaszkádolt törlését okozhatja.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="cb2ca-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb2ca-116">PARAMETERS</span></span>

### <span data-ttu-id="cb2ca-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb2ca-117">-AsJob</span></span>
<span data-ttu-id="cb2ca-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cb2ca-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb2ca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2ca-119">-DefaultProfile</span></span>
<span data-ttu-id="cb2ca-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb2ca-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cb2ca-121">-Force</span></span>
<span data-ttu-id="cb2ca-122">Supply-Force: a parancs megerősítésének mellőzése.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="cb2ca-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb2ca-123">-InputObject</span></span>
<span data-ttu-id="cb2ca-124">A RegisteredServer bemeneti objektuma, normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="cb2ca-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb2ca-125">-PassThru</span></span>
<span data-ttu-id="cb2ca-126">A normál végrehajtásban ez a parancsmag nem ad értéket a sikernek.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="cb2ca-127">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után a csővezetéknek ad értéket.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="cb2ca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb2ca-128">-ResourceGroupName</span></span>
<span data-ttu-id="cb2ca-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="cb2ca-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb2ca-130">-ResourceId</span></span>
<span data-ttu-id="cb2ca-131">RegisteredServer erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="cb2ca-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="cb2ca-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="cb2ca-132">-ServerId</span></span>
<span data-ttu-id="cb2ca-133">A RegisteredServer neve.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="cb2ca-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="cb2ca-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="cb2ca-135">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="cb2ca-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cb2ca-136">-Confirm</span></span>
<span data-ttu-id="cb2ca-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb2ca-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb2ca-138">-WhatIf</span></span>
<span data-ttu-id="cb2ca-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb2ca-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb2ca-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb2ca-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2ca-141">CommonParameters</span></span>
<span data-ttu-id="cb2ca-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb2ca-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2ca-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb2ca-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2ca-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb2ca-144">INPUTS</span></span>

### <span data-ttu-id="cb2ca-145">Microsoft. Azure. Command. StorageSync. models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="cb2ca-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="cb2ca-146">System. String</span><span class="sxs-lookup"><span data-stu-id="cb2ca-146">System.String</span></span>

### <span data-ttu-id="cb2ca-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cb2ca-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cb2ca-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb2ca-148">OUTPUTS</span></span>

### <span data-ttu-id="cb2ca-149">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="cb2ca-149">System.Object</span></span>
## <span data-ttu-id="cb2ca-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb2ca-150">NOTES</span></span>

## <span data-ttu-id="cb2ca-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb2ca-151">RELATED LINKS</span></span>

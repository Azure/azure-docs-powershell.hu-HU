---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 5ebcdee62997ed678b9696264a40076a40c36342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929602"
---
# <span data-ttu-id="6bddf-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="6bddf-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="6bddf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bddf-102">SYNOPSIS</span></span>
<span data-ttu-id="6bddf-103">Figyelmeztetés: A kiszolgáló regisztrációjának törlése kaszkádolt törlést eredményez a kiszolgáló összes kiszolgálói végpontjának.</span><span class="sxs-lookup"><span data-stu-id="6bddf-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="6bddf-104">Ez a parancs a kiszolgáló tárhelyszinkronizálási szolgáltatásában való regisztrációját is visszaveszi.</span><span class="sxs-lookup"><span data-stu-id="6bddf-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="6bddf-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6bddf-105">SYNTAX</span></span>

### <span data-ttu-id="6bddf-106">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6bddf-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bddf-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bddf-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bddf-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bddf-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bddf-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6bddf-109">DESCRIPTION</span></span>
<span data-ttu-id="6bddf-110">Ez a parancs a kiszolgáló tárhelyszinkronizálási szolgáltatásból való regisztrációját is visszaveszi.</span><span class="sxs-lookup"><span data-stu-id="6bddf-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="6bddf-111">Figyelmeztetés: A kiszolgáló regisztrációjának törlése kaszkádolt törlést eredményez a kiszolgáló összes kiszolgálói végpontjának.</span><span class="sxs-lookup"><span data-stu-id="6bddf-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="6bddf-112">A rendszer csak akkor hívhatja ezt a kiszolgálót, ha biztos abban, hogy ezen a kiszolgálón már nincs szinkronizálva elérési út.</span><span class="sxs-lookup"><span data-stu-id="6bddf-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="6bddf-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6bddf-113">EXAMPLES</span></span>

### <span data-ttu-id="6bddf-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="6bddf-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="6bddf-115">Ez a parancs törli a kiszolgáló regisztrációját, és kaszkádolt törlést okoz a kiszolgáló összes kiszolgálói végpontjának.</span><span class="sxs-lookup"><span data-stu-id="6bddf-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="6bddf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bddf-116">PARAMETERS</span></span>

### <span data-ttu-id="6bddf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bddf-117">-AsJob</span></span>
<span data-ttu-id="6bddf-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6bddf-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6bddf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bddf-119">-DefaultProfile</span></span>
<span data-ttu-id="6bddf-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6bddf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bddf-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6bddf-121">-Force</span></span>
<span data-ttu-id="6bddf-122">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="6bddf-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="6bddf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bddf-123">-InputObject</span></span>
<span data-ttu-id="6bddf-124">RegisteredServer Input Object, amely általában áthalad a folyamaton.</span><span class="sxs-lookup"><span data-stu-id="6bddf-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6bddf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bddf-125">-PassThru</span></span>
<span data-ttu-id="6bddf-126">Normál végrehajtáskor ez a parancsmag nem ad vissza értéket a sikerhez.</span><span class="sxs-lookup"><span data-stu-id="6bddf-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="6bddf-127">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után értéket ír a folyamatba.</span><span class="sxs-lookup"><span data-stu-id="6bddf-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="6bddf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bddf-128">-ResourceGroupName</span></span>
<span data-ttu-id="6bddf-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6bddf-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="6bddf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bddf-130">-ResourceId</span></span>
<span data-ttu-id="6bddf-131">RegisteredServer Resource Id</span><span class="sxs-lookup"><span data-stu-id="6bddf-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="6bddf-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="6bddf-132">-ServerId</span></span>
<span data-ttu-id="6bddf-133">A RegisteredServer neve.</span><span class="sxs-lookup"><span data-stu-id="6bddf-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="6bddf-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="6bddf-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="6bddf-135">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="6bddf-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="6bddf-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bddf-136">-Confirm</span></span>
<span data-ttu-id="6bddf-137">A parancsmag futtatása előtt megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6bddf-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bddf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bddf-138">-WhatIf</span></span>
<span data-ttu-id="6bddf-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6bddf-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bddf-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6bddf-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bddf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bddf-141">CommonParameters</span></span>
<span data-ttu-id="6bddf-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bddf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bddf-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bddf-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bddf-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bddf-144">INPUTS</span></span>

### <span data-ttu-id="6bddf-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="6bddf-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="6bddf-146">System.String</span><span class="sxs-lookup"><span data-stu-id="6bddf-146">System.String</span></span>

### <span data-ttu-id="6bddf-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6bddf-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6bddf-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bddf-148">OUTPUTS</span></span>

### <span data-ttu-id="6bddf-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="6bddf-149">System.Object</span></span>
## <span data-ttu-id="6bddf-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6bddf-150">NOTES</span></span>

## <span data-ttu-id="6bddf-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6bddf-151">RELATED LINKS</span></span>

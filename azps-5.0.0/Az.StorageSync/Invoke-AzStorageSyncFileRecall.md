---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: fb053da61aabd9328f4ff3d848243ff9b84d6d09
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302912"
---
# <span data-ttu-id="06e19-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="06e19-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="06e19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06e19-102">SYNOPSIS</span></span>
<span data-ttu-id="06e19-103">Ez a parancs visszahívja az összes többszintű fájlt a helyi merevlemezre.</span><span class="sxs-lookup"><span data-stu-id="06e19-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="06e19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06e19-104">SYNTAX</span></span>

### <span data-ttu-id="06e19-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="06e19-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06e19-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06e19-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06e19-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06e19-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06e19-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="06e19-108">DESCRIPTION</span></span>
<span data-ttu-id="06e19-109">Ha a felhőalapú réteg beállítás engedélyezve van egy kiszolgáló-végponton (egy regisztrált kiszolgálón lévő adott helyen), akkor ez a parancs segítségével visszahívhatja az összes többszintű fájlt a helyi merevlemezre.</span><span class="sxs-lookup"><span data-stu-id="06e19-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="06e19-110">Javasoljuk, hogy a visszahívás megkezdése előtt tiltsa le a Felhőbeli rétegeket a kiszolgálón futó végponton.</span><span class="sxs-lookup"><span data-stu-id="06e19-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="06e19-111">Ha a többszintű beállítás továbbra is fennáll, a visszahívás a többszintű fájlok elérését okozó egyéb fájlok elérését eredményezi, ami nem éri el a helyi lemezen tartózkodó összes tartalom kívánt célját.</span><span class="sxs-lookup"><span data-stu-id="06e19-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="06e19-112">Példák</span><span class="sxs-lookup"><span data-stu-id="06e19-112">EXAMPLES</span></span>

### <span data-ttu-id="06e19-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06e19-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="06e19-114">Ez a parancs rekurzívan visszahívja az összes olyan többszintű fájlt, amely a megadott kiszolgálói végpont gyökerének elérési útján található.</span><span class="sxs-lookup"><span data-stu-id="06e19-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="06e19-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06e19-115">PARAMETERS</span></span>

### <span data-ttu-id="06e19-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06e19-116">-AsJob</span></span>
<span data-ttu-id="06e19-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="06e19-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06e19-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e19-118">-DefaultProfile</span></span>
<span data-ttu-id="06e19-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06e19-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06e19-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06e19-120">-InputObject</span></span>
<span data-ttu-id="06e19-121">SyncGroup objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="06e19-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer, ServerEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06e19-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="06e19-122">-Name</span></span>
<span data-ttu-id="06e19-123">A ServerEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="06e19-123">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e19-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06e19-124">-PassThru</span></span>
<span data-ttu-id="06e19-125">A normál végrehajtásban ez a parancsmag nem ad értéket a sikernek.</span><span class="sxs-lookup"><span data-stu-id="06e19-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="06e19-126">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után a csővezetéknek ad értéket.</span><span class="sxs-lookup"><span data-stu-id="06e19-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="06e19-127">-Minta</span><span class="sxs-lookup"><span data-stu-id="06e19-127">-Pattern</span></span>
<span data-ttu-id="06e19-128">A fájl nevének mintája</span><span class="sxs-lookup"><span data-stu-id="06e19-128">Pattern of the file name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e19-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="06e19-129">-RecallPath</span></span>
<span data-ttu-id="06e19-130">Visszahívási útvonal, amelyet vissza kell hívni.</span><span class="sxs-lookup"><span data-stu-id="06e19-130">Recall path which need to be recalled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e19-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e19-131">-ResourceGroupName</span></span>
<span data-ttu-id="06e19-132">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="06e19-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="06e19-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06e19-133">-ResourceId</span></span>
<span data-ttu-id="06e19-134">ServerEndpoint erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="06e19-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="06e19-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="06e19-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="06e19-136">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="06e19-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="06e19-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="06e19-137">-SyncGroupName</span></span>
<span data-ttu-id="06e19-138">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="06e19-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e19-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06e19-139">-Confirm</span></span>
<span data-ttu-id="06e19-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06e19-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e19-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e19-141">-WhatIf</span></span>
<span data-ttu-id="06e19-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06e19-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06e19-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06e19-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e19-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e19-144">CommonParameters</span></span>
<span data-ttu-id="06e19-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06e19-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e19-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e19-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e19-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06e19-147">INPUTS</span></span>

### <span data-ttu-id="06e19-148">System. String</span><span class="sxs-lookup"><span data-stu-id="06e19-148">System.String</span></span>

### <span data-ttu-id="06e19-149">Microsoft. Azure. Command. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06e19-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="06e19-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06e19-150">OUTPUTS</span></span>

### <span data-ttu-id="06e19-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06e19-151">System.Boolean</span></span>

## <span data-ttu-id="06e19-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06e19-152">NOTES</span></span>

## <span data-ttu-id="06e19-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06e19-153">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 5463c20274f60c2d6fb6c4807bf2c4d27da76808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668493"
---
# <span data-ttu-id="a2a81-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="a2a81-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="a2a81-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2a81-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a81-103">Ez a parancs visszahívja az összes többszintű fájlt a helyi merevlemezre.</span><span class="sxs-lookup"><span data-stu-id="a2a81-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="a2a81-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2a81-104">SYNTAX</span></span>

### <span data-ttu-id="a2a81-105">ObjectParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2a81-105">ObjectParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2a81-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2a81-106">StringParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2a81-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2a81-107">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2a81-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2a81-108">DESCRIPTION</span></span>
<span data-ttu-id="a2a81-109">Ha a felhőalapú réteg beállítás engedélyezve van egy kiszolgáló-végponton (egy regisztrált kiszolgálón lévő adott helyen), akkor ez a parancs segítségével visszahívhatja az összes többszintű fájlt a helyi merevlemezre.</span><span class="sxs-lookup"><span data-stu-id="a2a81-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="a2a81-110">Javasoljuk, hogy a visszahívás megkezdése előtt tiltsa le a Felhőbeli rétegeket a kiszolgálón futó végponton.</span><span class="sxs-lookup"><span data-stu-id="a2a81-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="a2a81-111">Ha a többszintű beállítás továbbra is fennáll, a visszahívás a többszintű fájlok elérését okozó egyéb fájlok elérését eredményezi, ami nem éri el a helyi lemezen tartózkodó összes tartalom kívánt célját.</span><span class="sxs-lookup"><span data-stu-id="a2a81-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="a2a81-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a2a81-112">EXAMPLES</span></span>

### <span data-ttu-id="a2a81-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a2a81-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="a2a81-114">Ez a parancs rekurzívan visszahívja az összes olyan többszintű fájlt, amely a megadott kiszolgálói végpont gyökerének elérési útján található.</span><span class="sxs-lookup"><span data-stu-id="a2a81-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="a2a81-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2a81-115">PARAMETERS</span></span>

### <span data-ttu-id="a2a81-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2a81-116">-AsJob</span></span>
<span data-ttu-id="a2a81-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a2a81-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2a81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2a81-118">-DefaultProfile</span></span>
<span data-ttu-id="a2a81-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2a81-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2a81-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2a81-120">-InputObject</span></span>
<span data-ttu-id="a2a81-121">SyncGroup objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="a2a81-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a81-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2a81-122">-Name</span></span>
<span data-ttu-id="a2a81-123">A ServerEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="a2a81-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="a2a81-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2a81-124">-PassThru</span></span>
<span data-ttu-id="a2a81-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a2a81-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a2a81-126">-Minta</span><span class="sxs-lookup"><span data-stu-id="a2a81-126">-Pattern</span></span>
<span data-ttu-id="a2a81-127">A fájl nevének mintája</span><span class="sxs-lookup"><span data-stu-id="a2a81-127">Pattern of the file name</span></span>

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

### <span data-ttu-id="a2a81-128">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="a2a81-128">-RecallPath</span></span>
<span data-ttu-id="a2a81-129">Visszahívási útvonal, amelyet vissza kell hívni.</span><span class="sxs-lookup"><span data-stu-id="a2a81-129">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="a2a81-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2a81-130">-ResourceGroupName</span></span>
<span data-ttu-id="a2a81-131">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="a2a81-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="a2a81-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2a81-132">-ResourceId</span></span>
<span data-ttu-id="a2a81-133">ServerEndpoint erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a2a81-133">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="a2a81-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="a2a81-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="a2a81-135">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="a2a81-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="a2a81-136">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a2a81-136">-SyncGroupName</span></span>
<span data-ttu-id="a2a81-137">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="a2a81-137">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="a2a81-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a81-138">CommonParameters</span></span>
<span data-ttu-id="a2a81-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2a81-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a81-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2a81-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a81-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2a81-141">INPUTS</span></span>

### <span data-ttu-id="a2a81-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a2a81-142">System.String</span></span>

### <span data-ttu-id="a2a81-143">Microsoft. Azure. Command. StorageSync. models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a2a81-143">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="a2a81-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2a81-144">OUTPUTS</span></span>

### <span data-ttu-id="a2a81-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2a81-145">System.Boolean</span></span>

## <span data-ttu-id="a2a81-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2a81-146">NOTES</span></span>

## <span data-ttu-id="a2a81-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2a81-147">RELATED LINKS</span></span>

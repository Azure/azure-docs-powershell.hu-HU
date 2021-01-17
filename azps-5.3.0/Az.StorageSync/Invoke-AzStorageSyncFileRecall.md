---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: fb053da61aabd9328f4ff3d848243ff9b84d6d09
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466861"
---
# <span data-ttu-id="18ff5-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="18ff5-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="18ff5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="18ff5-103">Ez a parancs visszahívja az összes réteges fájlt a helyi lemezre.</span><span class="sxs-lookup"><span data-stu-id="18ff5-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="18ff5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18ff5-104">SYNTAX</span></span>

### <span data-ttu-id="18ff5-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18ff5-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18ff5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18ff5-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18ff5-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18ff5-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18ff5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18ff5-108">DESCRIPTION</span></span>
<span data-ttu-id="18ff5-109">Ha egy kiszolgálói végponton (egy regisztrált kiszolgálón egy adott helyen) engedélyezve van a felhőszintű rétegezés, ezzel a paranccsal visszahívhatja az összes réteges fájlt a helyi lemezre.</span><span class="sxs-lookup"><span data-stu-id="18ff5-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="18ff5-110">A visszahívás megkezdése előtt erősen ajánlott letiltani a felhőréteget ezen a kiszolgálói végponton.</span><span class="sxs-lookup"><span data-stu-id="18ff5-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="18ff5-111">Ha a rétegezés továbbra is be van maradva, a visszahívás más fájlok rétegezéséhez vezethet, amelyek nem érjék el a kívánt célokat a helyi lemezen lévő összes tartalom eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="18ff5-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="18ff5-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18ff5-112">EXAMPLES</span></span>

### <span data-ttu-id="18ff5-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="18ff5-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="18ff5-114">Ez a parancs rekurzív módon visszahívja a megadott kiszolgáló végpontjának gyökér elérési útja alatt található összes réteges fájlt.</span><span class="sxs-lookup"><span data-stu-id="18ff5-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="18ff5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18ff5-115">PARAMETERS</span></span>

### <span data-ttu-id="18ff5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18ff5-116">-AsJob</span></span>
<span data-ttu-id="18ff5-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="18ff5-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18ff5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ff5-118">-DefaultProfile</span></span>
<span data-ttu-id="18ff5-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18ff5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18ff5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18ff5-120">-InputObject</span></span>
<span data-ttu-id="18ff5-121">SyncGroup-objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="18ff5-121">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="18ff5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="18ff5-122">-Name</span></span>
<span data-ttu-id="18ff5-123">A ServerEndpoint neve.</span><span class="sxs-lookup"><span data-stu-id="18ff5-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="18ff5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18ff5-124">-PassThru</span></span>
<span data-ttu-id="18ff5-125">Normál végrehajtáskor ez a parancsmag nem ad vissza értéket a sikerhez.</span><span class="sxs-lookup"><span data-stu-id="18ff5-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="18ff5-126">Ha a PassThru paramétert adja meg, akkor a parancsmag a sikeres végrehajtás után értéket ír a folyamatba.</span><span class="sxs-lookup"><span data-stu-id="18ff5-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="18ff5-127">-Pattern</span><span class="sxs-lookup"><span data-stu-id="18ff5-127">-Pattern</span></span>
<span data-ttu-id="18ff5-128">A fájlnév mintája</span><span class="sxs-lookup"><span data-stu-id="18ff5-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="18ff5-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="18ff5-129">-RecallPath</span></span>
<span data-ttu-id="18ff5-130">Visszahívási útvonal, amelyet vissza kell visszahívni.</span><span class="sxs-lookup"><span data-stu-id="18ff5-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="18ff5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18ff5-131">-ResourceGroupName</span></span>
<span data-ttu-id="18ff5-132">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="18ff5-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="18ff5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18ff5-133">-ResourceId</span></span>
<span data-ttu-id="18ff5-134">ServerEndpoint Resource Id</span><span class="sxs-lookup"><span data-stu-id="18ff5-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="18ff5-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="18ff5-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="18ff5-136">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="18ff5-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="18ff5-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="18ff5-137">-SyncGroupName</span></span>
<span data-ttu-id="18ff5-138">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="18ff5-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="18ff5-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18ff5-139">-Confirm</span></span>
<span data-ttu-id="18ff5-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="18ff5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18ff5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18ff5-141">-WhatIf</span></span>
<span data-ttu-id="18ff5-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="18ff5-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18ff5-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18ff5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18ff5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ff5-144">CommonParameters</span></span>
<span data-ttu-id="18ff5-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18ff5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ff5-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18ff5-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ff5-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18ff5-147">INPUTS</span></span>

### <span data-ttu-id="18ff5-148">System.String</span><span class="sxs-lookup"><span data-stu-id="18ff5-148">System.String</span></span>

### <span data-ttu-id="18ff5-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="18ff5-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="18ff5-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18ff5-150">OUTPUTS</span></span>

### <span data-ttu-id="18ff5-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="18ff5-151">System.Boolean</span></span>

## <span data-ttu-id="18ff5-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18ff5-152">NOTES</span></span>

## <span data-ttu-id="18ff5-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18ff5-153">RELATED LINKS</span></span>

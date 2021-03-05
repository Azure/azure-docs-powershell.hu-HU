---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: c55b49052ae34eba9dfff960c85e9ade7617d2a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011414"
---
# <span data-ttu-id="428c1-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="428c1-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="428c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="428c1-102">SYNOPSIS</span></span>
<span data-ttu-id="428c1-103">Ez a parancs egy Azure File Sync felhőbeli végpontot hoz létre egy szinkronizálási csoportban.</span><span class="sxs-lookup"><span data-stu-id="428c1-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="428c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="428c1-104">SYNTAX</span></span>

### <span data-ttu-id="428c1-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="428c1-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="428c1-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="428c1-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="428c1-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="428c1-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="428c1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="428c1-108">DESCRIPTION</span></span>
<span data-ttu-id="428c1-109">Ez a parancs egy Azure File Sync felhőbeli végpontot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="428c1-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="428c1-110">A felhőbeli végpont egy meglévő Azure-fájlmegosztásra való hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="428c1-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="428c1-111">A fájlmegosztást képviseli, és meghatározza, hogy részt vesz a felhőbeli végpont által létrehozott szinkronizálási csoport összes fájlrészének szinkronizálásában.</span><span class="sxs-lookup"><span data-stu-id="428c1-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="428c1-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="428c1-112">EXAMPLES</span></span>

### <span data-ttu-id="428c1-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="428c1-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="428c1-114">A felhőbeli végpont a szinkronizálási csoport szerves tagja, ez egy példa arra, hogy létrehoz egy "mySyncGroupName" nevű meglévő szinkronizálási csoporton belül egyet.</span><span class="sxs-lookup"><span data-stu-id="428c1-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="428c1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="428c1-115">PARAMETERS</span></span>

### <span data-ttu-id="428c1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="428c1-116">-AsJob</span></span>
<span data-ttu-id="428c1-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="428c1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="428c1-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="428c1-118">-AzureFileShareName</span></span>
<span data-ttu-id="428c1-119">Tárfiók megosztási neve (Azure-fájlmegosztás neve)</span><span class="sxs-lookup"><span data-stu-id="428c1-119">Storage Account Share Name (Azure file share name)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428c1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428c1-120">-DefaultProfile</span></span>
<span data-ttu-id="428c1-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="428c1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="428c1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="428c1-122">-Name</span></span>
<span data-ttu-id="428c1-123">A felhőbeli végpont neve.</span><span class="sxs-lookup"><span data-stu-id="428c1-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="428c1-124">Amikor az Azure Portalon keresztül jön létre, a Név az Azure-fájl megosztási hivatkozásának nevére van beállítva.</span><span class="sxs-lookup"><span data-stu-id="428c1-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428c1-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="428c1-125">-ParentObject</span></span>
<span data-ttu-id="428c1-126">SyncGroup-objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="428c1-126">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="428c1-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="428c1-127">-ParentResourceId</span></span>
<span data-ttu-id="428c1-128">SyncGroup szülőerőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="428c1-128">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="428c1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="428c1-129">-ResourceGroupName</span></span>
<span data-ttu-id="428c1-130">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="428c1-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="428c1-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="428c1-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="428c1-132">Tárfiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="428c1-132">Storage Account Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428c1-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="428c1-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="428c1-134">Tárfiók bérlőazonosítója (vállalati címtárazonosító)</span><span class="sxs-lookup"><span data-stu-id="428c1-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="428c1-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="428c1-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="428c1-136">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="428c1-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="428c1-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="428c1-137">-SyncGroupName</span></span>
<span data-ttu-id="428c1-138">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="428c1-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="428c1-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="428c1-139">-Confirm</span></span>
<span data-ttu-id="428c1-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="428c1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="428c1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="428c1-141">-WhatIf</span></span>
<span data-ttu-id="428c1-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="428c1-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="428c1-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="428c1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="428c1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428c1-144">CommonParameters</span></span>
<span data-ttu-id="428c1-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="428c1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428c1-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="428c1-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428c1-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="428c1-147">INPUTS</span></span>

### <span data-ttu-id="428c1-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="428c1-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="428c1-149">System.String</span><span class="sxs-lookup"><span data-stu-id="428c1-149">System.String</span></span>

## <span data-ttu-id="428c1-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="428c1-150">OUTPUTS</span></span>

### <span data-ttu-id="428c1-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="428c1-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="428c1-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="428c1-152">NOTES</span></span>

## <span data-ttu-id="428c1-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="428c1-153">RELATED LINKS</span></span>

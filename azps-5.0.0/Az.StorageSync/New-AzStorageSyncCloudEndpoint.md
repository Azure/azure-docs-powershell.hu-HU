---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302911"
---
# <span data-ttu-id="3093d-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="3093d-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="3093d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3093d-102">SYNOPSIS</span></span>
<span data-ttu-id="3093d-103">Ez a parancs Azure-szinkronizálási Felhőbeli végpontot hoz létre a szinkronizálási csoportban.</span><span class="sxs-lookup"><span data-stu-id="3093d-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="3093d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3093d-104">SYNTAX</span></span>

### <span data-ttu-id="3093d-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3093d-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3093d-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3093d-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3093d-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3093d-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3093d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3093d-108">DESCRIPTION</span></span>
<span data-ttu-id="3093d-109">A parancs Azure-szinkronizálási Felhőbeli végpontot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3093d-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="3093d-110">A Felhőbeli végpontok egy meglévő Azure-fájlmegosztás hivatkozásai.</span><span class="sxs-lookup"><span data-stu-id="3093d-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="3093d-111">Ez a fájl a megosztást jelöli, és a szinkronizálási csoport összes fájljának szinkronizálásakor a részvételi hozzájárulást adja meg.</span><span class="sxs-lookup"><span data-stu-id="3093d-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="3093d-112">Példák</span><span class="sxs-lookup"><span data-stu-id="3093d-112">EXAMPLES</span></span>

### <span data-ttu-id="3093d-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3093d-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="3093d-114">A Felhőbeli végpontok a szinkronizálási csoportok elválaszthatatlan tagjai, ez a példa a "mySyncGroupName" nevű meglévő szinkronizálási csoporton belül létrehoz egy meglévőt.</span><span class="sxs-lookup"><span data-stu-id="3093d-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="3093d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3093d-115">PARAMETERS</span></span>

### <span data-ttu-id="3093d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3093d-116">-AsJob</span></span>
<span data-ttu-id="3093d-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3093d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3093d-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="3093d-118">-AzureFileShareName</span></span>
<span data-ttu-id="3093d-119">Tárhely-megosztási fiók neve (Azure fájlmegosztás neve)</span><span class="sxs-lookup"><span data-stu-id="3093d-119">Storage Account Share Name (Azure file share name)</span></span>

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

### <span data-ttu-id="3093d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3093d-120">-DefaultProfile</span></span>
<span data-ttu-id="3093d-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3093d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3093d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3093d-122">-Name</span></span>
<span data-ttu-id="3093d-123">A felhő végpontjának neve.</span><span class="sxs-lookup"><span data-stu-id="3093d-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="3093d-124">Amikor az Azure portálon keresztül jön létre, a név az Azure-fájl megosztási hivatkozásának neve lesz.</span><span class="sxs-lookup"><span data-stu-id="3093d-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

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

### <span data-ttu-id="3093d-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3093d-125">-ParentObject</span></span>
<span data-ttu-id="3093d-126">SyncGroup objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="3093d-126">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="3093d-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3093d-127">-ParentResourceId</span></span>
<span data-ttu-id="3093d-128">A SyncGroup szülő erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3093d-128">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="3093d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3093d-129">-ResourceGroupName</span></span>
<span data-ttu-id="3093d-130">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="3093d-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="3093d-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3093d-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="3093d-132">Tárolási fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3093d-132">Storage Account Resource Id</span></span>

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

### <span data-ttu-id="3093d-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="3093d-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="3093d-134">Tárolási fiók bérlői azonosítója (vállalati címtár-azonosító)</span><span class="sxs-lookup"><span data-stu-id="3093d-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="3093d-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="3093d-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="3093d-136">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="3093d-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="3093d-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="3093d-137">-SyncGroupName</span></span>
<span data-ttu-id="3093d-138">A SyncGroup neve.</span><span class="sxs-lookup"><span data-stu-id="3093d-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="3093d-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3093d-139">-Confirm</span></span>
<span data-ttu-id="3093d-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3093d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3093d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3093d-141">-WhatIf</span></span>
<span data-ttu-id="3093d-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3093d-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3093d-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3093d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3093d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3093d-144">CommonParameters</span></span>
<span data-ttu-id="3093d-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3093d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3093d-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3093d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3093d-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3093d-147">INPUTS</span></span>

### <span data-ttu-id="3093d-148">Microsoft. Azure. Command. StorageSync. models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3093d-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="3093d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3093d-149">System.String</span></span>

## <span data-ttu-id="3093d-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3093d-150">OUTPUTS</span></span>

### <span data-ttu-id="3093d-151">Microsoft. Azure. Command. StorageSync. models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="3093d-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="3093d-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3093d-152">NOTES</span></span>

## <span data-ttu-id="3093d-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3093d-153">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: bd1665ee82dfad0bb6028252ad100e5c651d0c2d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839611"
---
# <span data-ttu-id="c622b-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="c622b-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="c622b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c622b-102">SYNOPSIS</span></span>
<span data-ttu-id="c622b-103">Ez a parancs felsorolja az összes olyan kiszolgálót, amely egy adott tárterület-szinkronizálási szolgáltatáshoz van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="c622b-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="c622b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c622b-104">SYNTAX</span></span>

### <span data-ttu-id="c622b-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c622b-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c622b-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c622b-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c622b-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c622b-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c622b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c622b-108">DESCRIPTION</span></span>
<span data-ttu-id="c622b-109">Ez a parancs felsorolja az összes olyan kiszolgálót, amely egy adott tárterület-szinkronizálási szolgáltatáshoz van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="c622b-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="c622b-110">Az egyes regisztrált kiszolgálók attribútumai is felhasználhatók.</span><span class="sxs-lookup"><span data-stu-id="c622b-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="c622b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c622b-111">EXAMPLES</span></span>

### <span data-ttu-id="c622b-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c622b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="c622b-113">Ez a parancs beilleszti az összes olyan kiszolgálót, amely egy adott tárterület-szinkronizáló szolgáltatáshoz van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="c622b-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="c622b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c622b-114">PARAMETERS</span></span>

### <span data-ttu-id="c622b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c622b-115">-DefaultProfile</span></span>
<span data-ttu-id="c622b-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c622b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c622b-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c622b-117">-ParentObject</span></span>
<span data-ttu-id="c622b-118">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="c622b-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c622b-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c622b-119">-ParentResourceId</span></span>
<span data-ttu-id="c622b-120">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="c622b-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c622b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c622b-121">-ResourceGroupName</span></span>
<span data-ttu-id="c622b-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c622b-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="c622b-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="c622b-123">-ServerId</span></span>
<span data-ttu-id="c622b-124">A RegisteredServer neve.</span><span class="sxs-lookup"><span data-stu-id="c622b-124">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: RegisteredServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c622b-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c622b-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="c622b-126">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="c622b-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c622b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c622b-127">CommonParameters</span></span>
<span data-ttu-id="c622b-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c622b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c622b-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c622b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c622b-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c622b-130">INPUTS</span></span>

### <span data-ttu-id="c622b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c622b-131">System.String</span></span>

### <span data-ttu-id="c622b-132">Microsoft. Azure. Command. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c622b-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="c622b-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c622b-133">System.Guid</span></span>

## <span data-ttu-id="c622b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c622b-134">OUTPUTS</span></span>

### <span data-ttu-id="c622b-135">Microsoft. Azure. Command. StorageSync. models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="c622b-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="c622b-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c622b-136">NOTES</span></span>

## <span data-ttu-id="c622b-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c622b-137">RELATED LINKS</span></span>

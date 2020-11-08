---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: ebee7b772fc4da3ef14d2273b79b089d57fa317f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180743"
---
# <span data-ttu-id="23d41-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="23d41-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="23d41-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23d41-102">SYNOPSIS</span></span>
<span data-ttu-id="23d41-103">Ez a parancs felsorolja az összes olyan kiszolgálót, amely egy adott tárterület-szinkronizálási szolgáltatáshoz van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="23d41-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="23d41-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23d41-104">SYNTAX</span></span>

### <span data-ttu-id="23d41-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23d41-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23d41-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23d41-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23d41-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="23d41-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23d41-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="23d41-108">DESCRIPTION</span></span>
<span data-ttu-id="23d41-109">Ez a parancs felsorolja az összes olyan kiszolgálót, amely egy adott tárterület-szinkronizálási szolgáltatáshoz van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="23d41-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="23d41-110">Az egyes regisztrált kiszolgálók attribútumai is felhasználhatók.</span><span class="sxs-lookup"><span data-stu-id="23d41-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="23d41-111">Példák</span><span class="sxs-lookup"><span data-stu-id="23d41-111">EXAMPLES</span></span>

### <span data-ttu-id="23d41-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="23d41-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="23d41-113">Ez a parancs beilleszti az összes olyan kiszolgálót, amely egy adott tárterület-szinkronizáló szolgáltatáshoz van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="23d41-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="23d41-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23d41-114">PARAMETERS</span></span>

### <span data-ttu-id="23d41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d41-115">-DefaultProfile</span></span>
<span data-ttu-id="23d41-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23d41-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23d41-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="23d41-117">-ParentObject</span></span>
<span data-ttu-id="23d41-118">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="23d41-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="23d41-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="23d41-119">-ParentResourceId</span></span>
<span data-ttu-id="23d41-120">StorageSyncService objektum, általában áthalad a paraméteren.</span><span class="sxs-lookup"><span data-stu-id="23d41-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="23d41-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d41-121">-ResourceGroupName</span></span>
<span data-ttu-id="23d41-122">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="23d41-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="23d41-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="23d41-123">-ServerId</span></span>
<span data-ttu-id="23d41-124">A RegisteredServer neve.</span><span class="sxs-lookup"><span data-stu-id="23d41-124">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="23d41-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="23d41-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="23d41-126">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="23d41-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="23d41-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d41-127">CommonParameters</span></span>
<span data-ttu-id="23d41-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23d41-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d41-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23d41-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d41-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23d41-130">INPUTS</span></span>

### <span data-ttu-id="23d41-131">System. String</span><span class="sxs-lookup"><span data-stu-id="23d41-131">System.String</span></span>

### <span data-ttu-id="23d41-132">Microsoft. Azure. Command. StorageSync. models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="23d41-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="23d41-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="23d41-133">System.Guid</span></span>

## <span data-ttu-id="23d41-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23d41-134">OUTPUTS</span></span>

### <span data-ttu-id="23d41-135">Microsoft. Azure. Command. StorageSync. models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="23d41-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="23d41-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23d41-136">NOTES</span></span>

## <span data-ttu-id="23d41-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23d41-137">RELATED LINKS</span></span>

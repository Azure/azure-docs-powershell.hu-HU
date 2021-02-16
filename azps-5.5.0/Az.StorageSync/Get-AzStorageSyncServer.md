---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: ebee7b772fc4da3ef14d2273b79b089d57fa317f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150338"
---
# <span data-ttu-id="3b726-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="3b726-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="3b726-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b726-102">SYNOPSIS</span></span>
<span data-ttu-id="3b726-103">Ez a parancs felsorolja az adott tárhelyszinkronizálási szolgáltatáshoz regisztrált összes kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="3b726-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="3b726-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3b726-104">SYNTAX</span></span>

### <span data-ttu-id="3b726-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3b726-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b726-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b726-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b726-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b726-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b726-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3b726-108">DESCRIPTION</span></span>
<span data-ttu-id="3b726-109">Ez a parancs felsorolja az adott tárhelyszinkronizálási szolgáltatáshoz regisztrált összes kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="3b726-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="3b726-110">Az egyes regisztrált kiszolgálók attribútumainak felsorolásához is használható.</span><span class="sxs-lookup"><span data-stu-id="3b726-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="3b726-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3b726-111">EXAMPLES</span></span>

### <span data-ttu-id="3b726-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="3b726-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="3b726-113">Ez a parancs az összes kiszolgálót egy adott tárhelyszinkronizálási szolgáltatásba regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="3b726-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="3b726-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b726-114">PARAMETERS</span></span>

### <span data-ttu-id="3b726-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b726-115">-DefaultProfile</span></span>
<span data-ttu-id="3b726-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b726-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b726-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3b726-117">-ParentObject</span></span>
<span data-ttu-id="3b726-118">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="3b726-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="3b726-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3b726-119">-ParentResourceId</span></span>
<span data-ttu-id="3b726-120">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="3b726-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="3b726-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b726-121">-ResourceGroupName</span></span>
<span data-ttu-id="3b726-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3b726-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="3b726-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="3b726-123">-ServerId</span></span>
<span data-ttu-id="3b726-124">A RegisteredServer neve.</span><span class="sxs-lookup"><span data-stu-id="3b726-124">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="3b726-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="3b726-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="3b726-126">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="3b726-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="3b726-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b726-127">CommonParameters</span></span>
<span data-ttu-id="3b726-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b726-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b726-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b726-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b726-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b726-130">INPUTS</span></span>

### <span data-ttu-id="3b726-131">System.String</span><span class="sxs-lookup"><span data-stu-id="3b726-131">System.String</span></span>

### <span data-ttu-id="3b726-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3b726-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="3b726-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="3b726-133">System.Guid</span></span>

## <span data-ttu-id="3b726-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b726-134">OUTPUTS</span></span>

### <span data-ttu-id="3b726-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="3b726-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="3b726-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3b726-136">NOTES</span></span>

## <span data-ttu-id="3b726-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b726-137">RELATED LINKS</span></span>

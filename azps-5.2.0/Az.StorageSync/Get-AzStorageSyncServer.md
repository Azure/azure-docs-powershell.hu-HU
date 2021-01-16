---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: ebee7b772fc4da3ef14d2273b79b089d57fa317f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366755"
---
# <span data-ttu-id="f9a62-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="f9a62-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="f9a62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9a62-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a62-103">Ez a parancs felsorolja az adott tárhelyszinkronizálási szolgáltatáshoz regisztrált összes kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="f9a62-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="f9a62-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f9a62-104">SYNTAX</span></span>

### <span data-ttu-id="f9a62-105">StringParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f9a62-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9a62-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9a62-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9a62-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9a62-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9a62-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f9a62-108">DESCRIPTION</span></span>
<span data-ttu-id="f9a62-109">Ez a parancs felsorolja az adott tárhelyszinkronizálási szolgáltatáshoz regisztrált összes kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="f9a62-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="f9a62-110">Az egyes regisztrált kiszolgálók attribútumainak felsorolásához is használható.</span><span class="sxs-lookup"><span data-stu-id="f9a62-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="f9a62-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f9a62-111">EXAMPLES</span></span>

### <span data-ttu-id="f9a62-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="f9a62-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="f9a62-113">Ez a parancs az összes kiszolgálót egy adott tárhelyszinkronizálási szolgáltatásba regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="f9a62-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="f9a62-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9a62-114">PARAMETERS</span></span>

### <span data-ttu-id="f9a62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a62-115">-DefaultProfile</span></span>
<span data-ttu-id="f9a62-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9a62-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9a62-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f9a62-117">-ParentObject</span></span>
<span data-ttu-id="f9a62-118">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="f9a62-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="f9a62-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f9a62-119">-ParentResourceId</span></span>
<span data-ttu-id="f9a62-120">StorageSyncService objektum, amely általában a paraméteren keresztül van átadva.</span><span class="sxs-lookup"><span data-stu-id="f9a62-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="f9a62-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9a62-121">-ResourceGroupName</span></span>
<span data-ttu-id="f9a62-122">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f9a62-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="f9a62-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="f9a62-123">-ServerId</span></span>
<span data-ttu-id="f9a62-124">A RegisteredServer neve.</span><span class="sxs-lookup"><span data-stu-id="f9a62-124">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="f9a62-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="f9a62-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="f9a62-126">A StorageSyncService neve.</span><span class="sxs-lookup"><span data-stu-id="f9a62-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="f9a62-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a62-127">CommonParameters</span></span>
<span data-ttu-id="f9a62-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a62-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a62-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a62-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a62-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9a62-130">INPUTS</span></span>

### <span data-ttu-id="f9a62-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f9a62-131">System.String</span></span>

### <span data-ttu-id="f9a62-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f9a62-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="f9a62-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f9a62-133">System.Guid</span></span>

## <span data-ttu-id="f9a62-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9a62-134">OUTPUTS</span></span>

### <span data-ttu-id="f9a62-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="f9a62-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="f9a62-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f9a62-136">NOTES</span></span>

## <span data-ttu-id="f9a62-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9a62-137">RELATED LINKS</span></span>

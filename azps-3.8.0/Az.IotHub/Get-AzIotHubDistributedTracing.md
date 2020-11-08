---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012993"
---
# <span data-ttu-id="7c090-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="7c090-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="7c090-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c090-102">SYNOPSIS</span></span>
<span data-ttu-id="7c090-103">Az adott eszközhöz tartozó elosztott nyomkövetési beállítások beszerzése</span><span class="sxs-lookup"><span data-stu-id="7c090-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="7c090-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c090-104">SYNTAX</span></span>

### <span data-ttu-id="7c090-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c090-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c090-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7c090-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c090-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7c090-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c090-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c090-108">DESCRIPTION</span></span>
<span data-ttu-id="7c090-109">Az adott eszközhöz tartozó elosztott nyomkövetési beállítások beszerzése</span><span class="sxs-lookup"><span data-stu-id="7c090-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="7c090-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7c090-110">EXAMPLES</span></span>

### <span data-ttu-id="7c090-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7c090-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="7c090-112">Az adott eszközhöz tartozó elosztott nyomkövetési beállítások beszerzése</span><span class="sxs-lookup"><span data-stu-id="7c090-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="7c090-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c090-113">PARAMETERS</span></span>

### <span data-ttu-id="7c090-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c090-114">-DefaultProfile</span></span>
<span data-ttu-id="7c090-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c090-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c090-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7c090-116">-DeviceId</span></span>
<span data-ttu-id="7c090-117">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="7c090-117">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c090-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c090-118">-InputObject</span></span>
<span data-ttu-id="7c090-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="7c090-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c090-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7c090-120">-IotHubName</span></span>
<span data-ttu-id="7c090-121">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="7c090-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c090-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c090-122">-ResourceGroupName</span></span>
<span data-ttu-id="7c090-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7c090-123">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c090-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c090-124">-ResourceId</span></span>
<span data-ttu-id="7c090-125">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="7c090-125">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c090-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c090-126">CommonParameters</span></span>
<span data-ttu-id="7c090-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c090-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c090-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c090-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c090-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c090-129">INPUTS</span></span>

### <span data-ttu-id="7c090-130">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7c090-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7c090-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7c090-131">System.String</span></span>

## <span data-ttu-id="7c090-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c090-132">OUTPUTS</span></span>

### <span data-ttu-id="7c090-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="7c090-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="7c090-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c090-134">NOTES</span></span>

## <span data-ttu-id="7c090-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c090-135">RELATED LINKS</span></span>

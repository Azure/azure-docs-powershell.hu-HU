---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152947"
---
# <span data-ttu-id="a72e0-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="a72e0-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="a72e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a72e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a72e0-103">Az eszközök elosztott nyomkövetési beállításainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="a72e0-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="a72e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a72e0-104">SYNTAX</span></span>

### <span data-ttu-id="a72e0-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a72e0-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a72e0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a72e0-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a72e0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a72e0-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a72e0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a72e0-108">DESCRIPTION</span></span>
<span data-ttu-id="a72e0-109">Az eszközök elosztott nyomkövetési beállításainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="a72e0-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="a72e0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a72e0-110">EXAMPLES</span></span>

### <span data-ttu-id="a72e0-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a72e0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="a72e0-112">Az eszközök elosztott nyomkövetési beállításainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="a72e0-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="a72e0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a72e0-113">PARAMETERS</span></span>

### <span data-ttu-id="a72e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a72e0-114">-DefaultProfile</span></span>
<span data-ttu-id="a72e0-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a72e0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a72e0-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a72e0-116">-DeviceId</span></span>
<span data-ttu-id="a72e0-117">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a72e0-117">Target Device Id.</span></span>

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

### <span data-ttu-id="a72e0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a72e0-118">-InputObject</span></span>
<span data-ttu-id="a72e0-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="a72e0-119">IotHub object</span></span>

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

### <span data-ttu-id="a72e0-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a72e0-120">-IotHubName</span></span>
<span data-ttu-id="a72e0-121">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="a72e0-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a72e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a72e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="a72e0-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a72e0-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a72e0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a72e0-124">-ResourceId</span></span>
<span data-ttu-id="a72e0-125">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="a72e0-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a72e0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a72e0-126">CommonParameters</span></span>
<span data-ttu-id="a72e0-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a72e0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a72e0-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a72e0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a72e0-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a72e0-129">INPUTS</span></span>

### <span data-ttu-id="a72e0-130">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a72e0-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a72e0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a72e0-131">System.String</span></span>

## <span data-ttu-id="a72e0-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a72e0-132">OUTPUTS</span></span>

### <span data-ttu-id="a72e0-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="a72e0-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="a72e0-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a72e0-134">NOTES</span></span>

## <span data-ttu-id="a72e0-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a72e0-135">RELATED LINKS</span></span>

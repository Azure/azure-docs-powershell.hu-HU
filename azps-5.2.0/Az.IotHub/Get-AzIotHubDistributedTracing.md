---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341454"
---
# <span data-ttu-id="7116e-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="7116e-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="7116e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7116e-102">SYNOPSIS</span></span>
<span data-ttu-id="7116e-103">Az eszközök elosztott nyomkövetési beállításainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="7116e-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="7116e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7116e-104">SYNTAX</span></span>

### <span data-ttu-id="7116e-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7116e-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7116e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7116e-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7116e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7116e-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7116e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7116e-108">DESCRIPTION</span></span>
<span data-ttu-id="7116e-109">Az eszközök elosztott nyomkövetési beállításainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="7116e-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="7116e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7116e-110">EXAMPLES</span></span>

### <span data-ttu-id="7116e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7116e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="7116e-112">Az eszközök elosztott nyomkövetési beállításainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="7116e-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="7116e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7116e-113">PARAMETERS</span></span>

### <span data-ttu-id="7116e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7116e-114">-DefaultProfile</span></span>
<span data-ttu-id="7116e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7116e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7116e-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7116e-116">-DeviceId</span></span>
<span data-ttu-id="7116e-117">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7116e-117">Target Device Id.</span></span>

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

### <span data-ttu-id="7116e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7116e-118">-InputObject</span></span>
<span data-ttu-id="7116e-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="7116e-119">IotHub object</span></span>

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

### <span data-ttu-id="7116e-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7116e-120">-IotHubName</span></span>
<span data-ttu-id="7116e-121">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="7116e-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7116e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7116e-122">-ResourceGroupName</span></span>
<span data-ttu-id="7116e-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7116e-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7116e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7116e-124">-ResourceId</span></span>
<span data-ttu-id="7116e-125">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="7116e-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7116e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7116e-126">CommonParameters</span></span>
<span data-ttu-id="7116e-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7116e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7116e-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7116e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7116e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7116e-129">INPUTS</span></span>

### <span data-ttu-id="7116e-130">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7116e-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7116e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7116e-131">System.String</span></span>

## <span data-ttu-id="7116e-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7116e-132">OUTPUTS</span></span>

### <span data-ttu-id="7116e-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="7116e-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="7116e-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7116e-134">NOTES</span></span>

## <span data-ttu-id="7116e-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7116e-135">RELATED LINKS</span></span>

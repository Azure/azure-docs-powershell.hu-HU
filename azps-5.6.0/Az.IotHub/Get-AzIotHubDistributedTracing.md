---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: 290b2ddcea6812b840b9c19ad2d44c4a0e461e64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936889"
---
# <span data-ttu-id="c64c1-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="c64c1-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="c64c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c64c1-102">SYNOPSIS</span></span>
<span data-ttu-id="c64c1-103">Az eszközök elosztott nyomkövetési beállításainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="c64c1-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="c64c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c64c1-104">SYNTAX</span></span>

### <span data-ttu-id="c64c1-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c64c1-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c64c1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c64c1-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c64c1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c64c1-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c64c1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c64c1-108">DESCRIPTION</span></span>
<span data-ttu-id="c64c1-109">Az eszközök elosztott nyomkövetési beállításainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="c64c1-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="c64c1-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c64c1-110">EXAMPLES</span></span>

### <span data-ttu-id="c64c1-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c64c1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="c64c1-112">Az eszközök elosztott nyomkövetési beállításainak lekérte.</span><span class="sxs-lookup"><span data-stu-id="c64c1-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="c64c1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c64c1-113">PARAMETERS</span></span>

### <span data-ttu-id="c64c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c64c1-114">-DefaultProfile</span></span>
<span data-ttu-id="c64c1-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c64c1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c64c1-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c64c1-116">-DeviceId</span></span>
<span data-ttu-id="c64c1-117">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c64c1-117">Target Device Id.</span></span>

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

### <span data-ttu-id="c64c1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c64c1-118">-InputObject</span></span>
<span data-ttu-id="c64c1-119">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="c64c1-119">IotHub object</span></span>

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

### <span data-ttu-id="c64c1-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c64c1-120">-IotHubName</span></span>
<span data-ttu-id="c64c1-121">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="c64c1-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c64c1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c64c1-122">-ResourceGroupName</span></span>
<span data-ttu-id="c64c1-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c64c1-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c64c1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c64c1-124">-ResourceId</span></span>
<span data-ttu-id="c64c1-125">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="c64c1-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c64c1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c64c1-126">CommonParameters</span></span>
<span data-ttu-id="c64c1-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c64c1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c64c1-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c64c1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c64c1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c64c1-129">INPUTS</span></span>

### <span data-ttu-id="c64c1-130">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c64c1-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c64c1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c64c1-131">System.String</span></span>

## <span data-ttu-id="c64c1-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c64c1-132">OUTPUTS</span></span>

### <span data-ttu-id="c64c1-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="c64c1-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="c64c1-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c64c1-134">NOTES</span></span>

## <span data-ttu-id="c64c1-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c64c1-135">RELATED LINKS</span></span>

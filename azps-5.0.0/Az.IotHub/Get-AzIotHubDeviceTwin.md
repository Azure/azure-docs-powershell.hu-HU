---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187749"
---
# <span data-ttu-id="55c96-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="55c96-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="55c96-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55c96-102">SYNOPSIS</span></span>
<span data-ttu-id="55c96-103">Különálló eszközt kap.</span><span class="sxs-lookup"><span data-stu-id="55c96-103">Gets a device twin.</span></span>

## <span data-ttu-id="55c96-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55c96-104">SYNTAX</span></span>

### <span data-ttu-id="55c96-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55c96-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55c96-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="55c96-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55c96-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="55c96-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55c96-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="55c96-108">DESCRIPTION</span></span>
<span data-ttu-id="55c96-109">Különálló eszközt kap.</span><span class="sxs-lookup"><span data-stu-id="55c96-109">Gets a device twin.</span></span> <span data-ttu-id="55c96-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twinsTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="55c96-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="55c96-111">Példák</span><span class="sxs-lookup"><span data-stu-id="55c96-111">EXAMPLES</span></span>

### <span data-ttu-id="55c96-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="55c96-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="55c96-113">Az Device Twin objektum értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="55c96-113">Returns the device twin object.</span></span>

## <span data-ttu-id="55c96-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55c96-114">PARAMETERS</span></span>

### <span data-ttu-id="55c96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c96-115">-DefaultProfile</span></span>
<span data-ttu-id="55c96-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55c96-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55c96-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="55c96-117">-DeviceId</span></span>
<span data-ttu-id="55c96-118">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="55c96-118">Target Device Id.</span></span>

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

### <span data-ttu-id="55c96-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55c96-119">-InputObject</span></span>
<span data-ttu-id="55c96-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="55c96-120">IotHub object</span></span>

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

### <span data-ttu-id="55c96-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="55c96-121">-IotHubName</span></span>
<span data-ttu-id="55c96-122">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="55c96-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="55c96-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55c96-123">-ResourceGroupName</span></span>
<span data-ttu-id="55c96-124">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="55c96-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="55c96-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55c96-125">-ResourceId</span></span>
<span data-ttu-id="55c96-126">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="55c96-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="55c96-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c96-127">CommonParameters</span></span>
<span data-ttu-id="55c96-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55c96-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c96-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55c96-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c96-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55c96-130">INPUTS</span></span>

### <span data-ttu-id="55c96-131">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="55c96-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="55c96-132">System. String</span><span class="sxs-lookup"><span data-stu-id="55c96-132">System.String</span></span>

## <span data-ttu-id="55c96-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55c96-133">OUTPUTS</span></span>

### <span data-ttu-id="55c96-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="55c96-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="55c96-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55c96-135">NOTES</span></span>

## <span data-ttu-id="55c96-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55c96-136">RELATED LINKS</span></span>
